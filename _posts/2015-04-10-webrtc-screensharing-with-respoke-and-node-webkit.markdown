---
layout: post
author: Tian Davis
title:  "WebRTC Screensharing With Respoke and Node-Webkit"
date:   2015-04-10 00:00:00
permalink: /thoughts/posts/webrtc-screensharing-with-respoke-and-node-webkit
---

![NodeWebkit](/images/node-webkit.png)

###The Code

I've been working with a lot of developers on WebRTC solutions. One, in particular, needed screensharing for their next-generating proctoring solution, so I built a proof-of-concept (PoC) screensharing app using node-webkit.

A typical video call with [Respoke](https://www.respoke.io/) starts with starting a call with another endpoint:

{% highlight js %}
var otherEndpoint = client.getEndpoint({
    id: theirName
});

otherEndpoint.startCall({
      onConnect: onConnect,
      onLocalMedia: onLocalVideo
});

To enable screensharing we just need to pass getUserMedia MediaStreamContraints:

var otherEndpoint = client.getEndpoint({
    id: theirName
  });

var constraints = {
      audio: false,
      video: {
            mandatory: {
              chromeMediaSource: 'screen',
              maxHeight: 2000,
              maxWidth: 2000
            },
            optional: []
      }
};

otherEndpoint.startCall({
    constraints: constraints,
      onConnect: onConnect,
      onLocalMedia: onLocalVideo
});
{% endhighlight %}

In addition, we need to enable usermedia screen capturing in node-webkit. To do this, we added the following chromium-args to our npm package.json file:

{% highlight js %}
{
  . . .
  "chromium-args": "--enable-usermedia-screen-capturing"
  . . .
}
{% endhighlight %}

The `--enable-usermedia-screen-capturing` chromium flag replaces the media transmitted with your screen instead of your camera input.

Our [Respoke screensharing demo](https://github.com/respoke/respoke-screen-sharing-node-webkit) is open source. To use it, head over to our Respoke Screensharing Node-Webkit GitHub repo. Then run the following commands from your terminal:

{% highlight bash %}
git clone https://github.com/respoke/respoke-screensharing-node-webkit.git

cd respoke-screensharing-node-webkit

npm install

Open Node Webkit Instance 1
./node_modules/nodewebkit/nodewebkit/node-webkit.app/Contents/MacOS/node-webkit .

Open Node Webkit Instance 2
./node_modules/nodewebkit/nodewebkit/node-webkit.app/Contents/MacOS/node-webkit .
{% endhighlight %}

Give it a try. If you find any issues, we welcome pull requests.

###Media Stream Constraints

To make screensharing work, we had to pass a MediaStreamContraint object literal. But, where does all this come from? It all starts with a w3 spec. When specs are not final, vendor implementation typically starts from a draft spec. In this case, the Media Capture and Streams working draft. There is no current consensus on what every constraints should be. The working drafts acts a starting point so vendors like Google can start implementing real examples of how constraints are used.

For example, the working draft specifies constraints like width, height, frameRate and aspectRatio. But the Chromium MediaConstraints source code specifies so much more available constraints like minAspectRatio, maxAspectRatio, minWidth, maxWidth, minHeight, maxHeight, minFrameRate and maxFrameRate:

{% highlight cpp %}
class MediaConstraintsInterface {
  public:
    . . .
    
    // Constraint keys used by a local video source.
    // Specified by draft-alvestrand-constraints-resolution-00b
    static const char kMinAspectRatio[]; // minAspectRatio
    static const char kMaxAspectRatio[]; // maxAspectRatio
    static const char kMaxWidth[]; // maxWidth
    static const char kMinWidth[]; // minWidth
    static const char kMaxHeight[]; // maxHeight
    static const char kMinHeight[]; // minHeight
    static const char kMaxFrameRate[]; // maxFrameRate
    static const char kMinFrameRate[]; // minFrameRate

    . . .
};
{% endhighlight %}

The Chromium MediaConstraints even go on to define other interesting experimental contraints like echoCancellation, noiseReduction and cpuOveruseDetection:

{% highlight cpp %}
class MediaConstraintsInterface {
  public:
    . . .
    // Constraint keys used by a local audio source.
    // These keys are google specific.
    static const char kEchoCancellation[]; // googEchoCancellation
   
    // Google-specific constraint keys for a local video source
    static const char kNoiseReduction[]; // googNoiseReduction
    
    . . .
    
    // googTemporalLayeredScreencast
    static const char kCpuOveruseDetection[];
};
{% endhighlight %}


Of course there is no guarantee that those features will make it to the final Media Capture and Streams spec.

Flags
We had to use Chromium command line flags to enable screensharing. Chromium command line flags are another interesting piece of the puzzle. 

For one they enable developers to take advantage of features not available to the general public. Another is peeking behind the covers is just really cool to see. Take for example the Chromium flag we used earlier: `--enable-usermedia-screen-capturing`.

It’s source code is defined in Chromium’s content_switches.h header file:

{% highlight cpp %}
// Defines all the "content" command-line switches.

. . .

namespace switches {
// All switches in alphabetical order. The switches should be documented
// alongside the definition of their values in the .cc file.
. . .

CONTENT_EXPORT extern const char kEnableUserMediaScreenCapturing[];
. . .
}
{% endhighlight %}

And implemented in Chromium’s content_switches.cc file:

{% highlight cpp %}
#include "content/public/common/content_switches.h"

#include "base/command_line.h"

namespace switches {
. . .

// Enable screen capturing support for MediaStream API.
const char kEnableUserMediaScreenCapturing[] =
    "enable-usermedia-screen-capturing";
    
. . .
}
{% endhighlight %}

We then use those flags as chromium-args in our node-webkit apps. You can pass chromium flags to chrome directly as well. On Mac OS X, you’d use:

`open -a "Google Chrome" --args --enable-usermedia-screen-capturing`

On Windows, something like:
`chrome.exe --args --enable-usermedia-screen-capturing`

I hope you’re as excited about the future of WebRTC as we are. It’s a great time to be a developer. Fork our demo screensharing app using Respoke and Node-Webkit. Play around and if you like it, share it with your friends. 
