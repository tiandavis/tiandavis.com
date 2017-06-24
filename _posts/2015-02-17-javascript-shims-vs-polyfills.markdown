---
layout: post
author: Tian Davis
title:  "JavaScript Shims Versus Polyfills"
date:   2015-02-17 00:00:00
permalink: /thoughts/posts/javascript-shims-versus-polyfills
---

![Polyfilla](/images/polyfilla.jpg)


I'm currently working on a conference talk about WebRTC. One of the foundations of any WebRTC library is some form of Google's original [adapter.js](https://code.google.com/p/webrtc/source/browse/trunk/samples/js/base/adapter.js?r=3905), which seeks to normalize the WebRTC API across various browsers. As I was about to build this particular slide, one question started to whisper in my ear, "Is adapter.js a shim or a polyfill?" Eventually, the whisper grew louder and I had to find the answer.

As a JavaScript developer, you've no doubt ran across an [HTML5 library](https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-browser-Polyfills) and thought the same thing, "Is it really a shim, or is it really a polyfill?" If you're like me, you stopped, looked at both terms, and then scratched your head… In this article I'll clarify the definition of a JavaScript shim and a JavaScript polyfill so that you can be an informed developer. Knowing the difference will allow you to better choose the libraries you use.

Back in 2010, Remy Sharp coined the term [JavaScript Polyfill](https://remysharp.com/2010/10/08/what-is-a-polyfill):

> A polyfill is a piece of code (or plugin) that provides the technology that you, the developer, expect[s] the browser to provide natively. Flattening the API landscape if you will.

If the library determines a feature doesn't natively exist in your browser, it will provide that functionality by any means necessary. That could mean replicating the functionality using any combination of JavaScript, NPAPI, ActiveX and Flash (or anything for that matter). More importantly, you won't even know the polyfill is there because you're still using the native JavaScript code.

Remy went on to share his understanding of a JavaScript Shim:

> Shim, to me, meant a piece of code that you could add that would fix some functionality, but it would most often have it's own API.  

This was a good start. Over the last few years, we've seen the JavaScript ecosystem evolve. One thing I've noticed is that we tend to think of shims as some smaller piece of code, whereas polyfills tend to be larger, more complex pieces of code. But there are other differences and similarities as well.

I decided to list out those similarities and differences to give myself a better understanding of a shim versus a polyfill. Here's what I've found so far:


### Similarities Between Polyfill and Shim

`- Both seek to normalize functionality across browsers`

`- Both tend to extend native methods, opting for their own implementation when the native method does not exist.`


### Differences Between Polyfill and Shim`

`- Shims tend to be written in a single language`

`-Polyfills tend to use multiple language platforms to achieve the aim of cross-browser normalization`

Polyfills often have to use multiple language platforms because sometimes a particular JavaScript API doesn't exist in that browser at all. I believe that's the pivotal point here.

[Sime Vidas](https://twitter.com/simevidas) goes on to share his thoughts on shims vs polyfills on this [Stack Overflow](https://stackoverflow.com/questions/6599815/what-is-the-difference-between-a-shim-and-a-polyfill/17331540#17331540) question on the topic:

> From what I understand:
> A polyfill is code that detects if a certain "expected" API is missing and manually implements it. E.g.

> `if (!Function.prototype.bind) {`

> `Function.prototype.bind = ...;`

> `}`

A shim is code that intercepts existing API calls and implements different behavior. The idea here is to normalize certain APIs across different environments. So, if two browsers implement the same API differently, you could intercept the API calls in one of those browsers and make its behavior align with the other browser. Or, if a browser has a bug in one of its APIs, you could again intercept calls to that API, and then circumvent the bug.
I think this is the most clear definition I've seen of the two so far. Vidas mentions the shim "intercepting" the API call. This creates a clearer visual than Sharp's "fix" definition.

It also helps validate some of the differences I've noticed over the years. Namely, shims appear to be written in JavaScript only because the JavaScript API already exists (it just needs some smoothing to normalize behaviors across browsers). Whereas polyfills often have to use multiple language platforms because the JavaScript API does not exist at all.


### Shim and Polyfill Real-World Parallels

In the real world a shim is a wedge-shaped piece of wood. "Polyfilla" is the name of a [spackling paste from LePage](https://www.lepageproducts.com/ProductDetail.aspx?pid=101). You'd typically use a shim to level off a leaning stove or other appliance. On the other hand, spackling paste would be used to fill a hole in a wall or other crevice. Notice the stove has to exist in order to use the shim at all. Whereas the polyfill (spackling paste) is used to fill a gap in the wall. The polyfill itself isn't exactly the same as the wall, but it acts close enough to the real thing to make it work.


#### Examples of JavaScript Polyfills

In particular, take a look at the available transports is Socket.IO. There is websocket, htmlfile, xhr-polling, jsonp-polling and flashsocket. Yes - Flash. Socket.IO is a great example of a JavaScript polyfill that manually implements WebSockets in older browsers by any means necessary. Falling back to flash allowed Socket.IO to approximate WebSockets in older browsers like IE 8 and IE 9 during a time when they held noticeable marketshare. This would not have been possible with a pure JavaScript implementation only.

Today, the flashsocket transport is disabled by default in Socket.IO and will not activate on Chrome or other browsers that fully support WebSockets, even if flashsocket is specified as the only transport. To test flashsocket, you have to use IE 8 or IE 9, or other browsers that don't natively support WebSockets. Had Socket.IO been designed as a shim, it simply would not have worked in older versions of IE at all because shims don't implement features that don't exist.

There are many other examples of great JavaScript polyfills that use a multitude of technologies in addition to JavaScrip to achieve cross-browser compatibility. Raphael falls back to VML in older versions of IE that don't support SVG. Store.js falls back to ActiveX and IE's non-standard userData in IE 6 and IE 7 where localStorage does not exist. Video.js falls back to Flash in older versions of IE that don't support the HTML5 video element. I could go on all day…

The point is that shims only normalize browser behavior, whereas polyfills both normalize browser behavior and implement functionality where it does not exist.


### Shim vs Polyfill Checklist

So as a developer, here's a quick checklist to figure out if you're developing a shim or a polyfill:

**`1.Does your library normalize a JavaScript API across the major browsers?`**

**`2. Does the JavaScript API exist in some major browsers?`**

**`3.Does your library implement the JavaScript API where it does not exist?`**

Here's a flow diagram of the decision tree:

![Shim Polyfill Decision Tree](/images/shim-polyfill-decision-tree.png)


### So is Google's Adapter.js a Shim or a Polyfill?

Let's use our decision framework to figure out the answer to the question:

**`1. Does adapter.js normalize a JavaScript API across the major browsers?`**

Yes. Adapter.js normalizes the WebRTC API.

**`2. Does the WebRTC API exist in some major browsers?`**

Yes. Currently, the WebRTC API exists in Chrome, Firefox and Opera.

**`3. Does adapter.js implement the WebRTC API where it does not exist?`**

No. Google's adapter.js library does not implement the WebRTC API in either IE or Safari.

Based on our Shim versus Polyfill guide, Google's adapter.js is definitely a shim because it does normalize the Web RTC API, but stops short of implementing it in either IE or Safari.


### Why Does it Matter?

I wrote this article because over the years using both terms has grown rather confusing. Some even go so far as to say [shim is synonymous to polyfill](https://books.google.com/books?id=qkd-yBhZokUC&pg=PA155&lpg=PA155&dq=javascript+shim+polyfill+synonymous&source=bl&ots=P0hQTVgtoK&sig=mhLt7IrbuyPz7_HT_huQIcqmuwk&hl=en&sa=X&ei=Et3bVMatF4LngwSxsIRI&ved=0CC4Q6AEwAg#v=onepage&q=javascript%20shim%20polyfill%20synonymous&f=false). That's simply not the case, nor should it be. There is both a place and a need for each term in the craft.

This may all seem like semantics, but it's not. Understanding the difference between a shim and a polyfill is the difference between your app working in some browsers and your app working in all browsers. If you're like me, you go for all browsers or you die trying. Knowing your shims from your polyfills is key to getting you there.
