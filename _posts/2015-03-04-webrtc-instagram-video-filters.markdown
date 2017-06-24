---
layout: post
author: Tian Davis
title:  "WebRTC Instagram Video Filters"
date:   2015-03-04 00:00:00
permalink: /thoughts/posts/webrtc-instagram-video-filters
---

![Instagram](/images/instagram-2.jpg)

<p>With more than a $1 Billion valuation and over 75 million daily users, <a href="https://instagram.com/digium/">Instagram</a> is arguably one of the most popular social networks today. Did you know more than 55 million photos are posted daily on Instagram? Or that the platform sees over 8,500 likes per second?</p>

<p>I&rsquo;ve always had a small love affair with image processing. So I figured let&rsquo;s have some fun with WebRTC and find out, &ldquo;Can you apply Instagram filters to a live WebRTC video stream?&rdquo; To be brutally honest, the question had been burning me for months, so I finally set out to find the answer.</p>

<p>What I found is indeed you can add Instagram, or rather Instagram-ish, filters to your live WebRTC video stream. Here&rsquo;s a <a href="https://tiandavis.github.io/webrtc-instagram-video-filters/">live demo</a> I put together of the concept (Pro Tip: Use Chrome or <a href="https://caniuse.com/#feat=css-filters">FF 35+</a>). This is the story of how I went about getting it done. You can follow along as I break it down step-by-step. </p>

<p>First, we need a little HTML to hang our video element and controls: </p>

{% highlight html %}
<script src="respoke.js"></script>
. . .

<div class="video-streams">
  <video id="localVideo"></video>
  <video id="remoteVideo"></video>
</div>

<p>Instagram Filters:</p>
  
<ul id="filters">
  <li id="NoFilter">#NoFilter</li>
  <li id="Willow">#Willow</li>
  <li id="Earlybird">#Earlybird</li>
  <li id="Mayfair">#Mayfair</li>
  <li id="Amaro">#Amaro</li>
</ul>
{% endhighlight %}

<p>Here, I included Google&rsquo;s <a href="http://blog.respoke.io/post/111278536998/javascript-shim-vs-polyfill">adapter.js shim</a> to normalize WebRTC behavior across Chrome, Firefox and Opera. Then, I included a simple video tag. We&rsquo;ll use that video tag to display the video stream coming from our web camera. We&rsquo;ll also use that same video tag to apply our image filters against. Lastly, I created an unordered list of Instagram filters and a #NoFilter control to remove all filters from the video element. Interesting to note, #NoFilter is the <a href="https://www.buzzfeed.com/javim2/23-interesting-facts-about-instagram-bw9q#.vbRNlYMy5b">most popular filter on Instagram</a>. Now for the actual filters.</p>

<p>Laying the foundation for the Instagram filters are <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/filter">CSS3 filters</a>. Thankfully, Nick Georgiou of Design Pieces already did a fantastic job recreating <a href="https://designpieces.com/2014/09/instagram-filters-css3-effects/">every single Instagram filter using CSS3 filters</a>. Here are a few we&rsquo;ll use for this experiment:</p>

{% highlight css %}
.ig-willow {
  -webkit-filter: saturate(0.02) contrast(0.85) brightness(1.2) sepia(0.02);
  filter: saturate(0.02) contrast(0.85) brightness(1.2) sepia(0.02);
}

.ig-earlybird {
  -webkit-filter: sepia(0.4) saturate(1.6) contrast(1.1) brightness(0.9) hue-rotate(-10deg);
  filter: sepia(0.4) saturate(1.6) contrast(1.1) brightness(0.9) hue-rotate(-10deg);
}

.ig-mayfair {
  -webkit-filter: saturate(1.4) contrast(1.1);
  filter: saturate(1.4) contrast(1.1);
}

.ig-amaro {
  -webkit-filter: hue-rotate(-10deg) contrast(0.9) brightness(1.1) saturate(1.5);
  filter: hue-rotate(-10deg) contrast(0.9) brightness(1.1) saturate(1.5);
}
{% endhighlight %}

<p>Using a combination of CSS3 filters: sepia, saturate, contrast, brightness and hue-rotate; we&rsquo;re able to approximate Instagram&rsquo;s Willow, Earlybird, Mayfair and Amaro filters. Now for the really fun part: bringing the app to life with a little JavaScript.</p>

<p>To do this we&rsquo;ll leverage the camera access feature of WebRTC and then apply the CSS3 filters as we see fit. First, let&rsquo;s take a look at how we access the camera:</p>

{% highlight js %}
var constraints = {
  video: true, 
  audio: true
};

getUserMedia(
  constraints, 
  onMediaStream, 
  noMediaStream
);

function onMediaStream(stream) {
  localVideo = document.getElementById("localVideo");
  
  attachMediaStream(localVideo, stream);
  
  localVideo.play();
}

function noMediaStream (error) {
  console.log("No media stream for us.", error);
}
{% endhighlight %}

<p>Here, we call getUserMedia and pass it three parameters. The first is a constraints object listing which devices to access, in this case, both the video camera and the mic. The last two parameters are callbacks. We use the first callback for when we successfully get a stream from our camera. We use the second callback if accessing the camera stream fails.</p>

<p>Once we have the camera stream, we can then get the video element. Next, we attach the camera stream to the video element. We&rsquo;ll need to call play on the video element, if we don&rsquo;t then we&rsquo;ll just see a camera still shot. Now that we have our video playing, we&rsquo;ll want to implement a way to apply our Instagram filters to the video element.</p>

<p>To accomplish this, we&rsquo;ll need to setup an event to apply each filter. Let&rsquo;s take a look at the JavaScript code to implement this:</p>

{% highlight js %}
var ul = document.getElementById("filters"); 

ul.addEventListener("click", function(e) {
  var filter = e.target.id;
  
  var filters = {
    "NoFilter": function() {
      localVideo.className = "";
    },
    
    "Willow": function() {
      localVideo.className = "ig-willow";
    },
    
    "Earlybird": function() {
      localVideo.className = "ig-earlybird";
    },
    
    "Mayfair": function() {
      localVideo.className = "ig-mayfair";
    },
    
    "Amaro": function() {
      localVideo.className = "ig-amaro";
    }
  }[filter]();
});
{% endhighlight %}

<p>Here, we add an event listener to the list of Instagram filters. When a filter is clicked, we&rsquo;ll get its corresponding filter id. Once we have the filter id, it&rsquo;s an easy transition to apply the corresponding CSS3 filter to the video element. When we&rsquo;re ready to remove all filters, we just remove all CSS3 class filters from the video element.</p>

<p>I went ahead and pushed my <a href="https://github.com/tiandavis/webrtc-instagram-video-filters">webrtc video filter code</a> to GitHub in its entirety. The instructions to run it locally are in the README. Git clone and you&rsquo;ll be up and running in 30 seconds.</p>

<p>So that&rsquo;s my WebRTC project. As you can see, the video element is a first class HTML5 element. That means you can manipulate it in JavaScript and style it in CSS to your hearts delight. I just think it&rsquo;s so cool you can manipulate the look and feel of a live video stream.</p>

<p>I&rsquo;ve heard #Mayfair is one of the top Instagram filters. Which one did you like best? I hope you had as much fun as I did and now you can add Instagram filters to your WebRTC video too.</p>
