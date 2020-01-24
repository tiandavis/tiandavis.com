---
layout: resume
title:  "Software Engineer"
date:   2010-07-01 00:00:00
permalink: /resume/
---

Michelangelo never saw a lump of marble.

He saw the [Pieta] and he would later write in his diaries about releasing the image inside. I do the same thing with JavaScript. JavaScript is the raw material, the medium that could become great software. I don’t see eccentricities or quirks. I see the new Basecamp, Hubot and Slack.

Over the last fifteen years, as a Front-End Developer and Tech Lead, I’ve done everything from lead a Fortune 500 development team through an agile transformation to writing some of the best JavaScript of my life at distributed startups. I'm a seasoned Software Engineer.

![Capabilities][capabilities-1]

<br>


## Strong Engineering Skills

Currently, I wax poetic with Ember.js and Node as a software developer on the BrowZine [Front-End Engineering Team][browzine]. BrowZine is a remote distributed startup in the academic and commercial research space.

Previously, I shipped critical components on both Respoke's Community Team and Respoke's Front-End Team. At its height, Respoke was a remote distributed startup in the telecommunication space, specifically WebRTC and Asterisk.

Prior to that, I shipped as a Tech Lead at Nationwide and as a consultant in various industries from banking to education to medical to military simulation and training.

<br>

## BrowZine

I've been fortunate, really fortunate, that my startup experience has been shaped with some of the most talented engineers and business leaders I've ever worked with.

![ember-responsive acceptance tests](/images/ember-responsive-acceptance-tests-4.png)

![Capabilities][capabilities-3]

#### <i>BrowZine.com: Mobile Responsive</i>

Worked with a talented team of co-founders and engineers, leading the [retrofitting][browzine-subjects] of our existing Ember.js desktop web application with a mobile responsive UI/UX. Resize your browser to try it out live. :)

BrowZine is built using Ember CLI, Sass and QUnit for testing on the frontend, running atop a Node Express JSON API spec and Mocha for testing on the backend with CircleCI for continuous integration.

![ember-responsive acceptance tests](/images/subjects-search.png)

![ember-responsive acceptance tests](/images/subject-details.png)

![ember-responsive acceptance tests](/images/journal-toc.png)

Automated acceptance tests are challenging for desktop layouts alone and they are exponentially challenging for responsive layouts, but we've succeeded in running our existing automated acceptance tests against our new mobile responsive user interface. Learn more about how we got our [responsive user interface under test](/thoughts/posts/ember-responsive-acceptance-tests) using our existing, mature Ember acceptance tests.

#### <i>Discovery Service Adapters</i>

In the academic and commercial research space, students and scientists use a variety of tools and discovery services to stay connected with new research findings, follow journals and discover research articles that may impact their work. One of the cool things BrowZine does is enhance those various discovery service platforms to provide a better research experience.

I play my part by leading BrowZine's software integration into various third-party, primarily Angular 1.x based, discovery services, of which there are many. Today, the [browzine-discovery-service-adapters][browzine-discovery-service-adapters] collection of adapters integrate with Primo, Summon and EJP.

![browzine-discovery-service-adapters screenshot](/images/browzine-discovery-service-adapters-2.png)

The most exciting aspect of this project was working with the [MutationObserver](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver) browser interface. The MutationObserver interface provides the ability to watch for changes being made to the DOM tree. Using MutationObserver allowed us to build adapters that could operate independent of the discovery service's framework.

The result is we're able to add links to Journals, Articles and Article PDF downloads in BrowZine, as well as enhance search results with BrowZine Journal Covers. The project is open source and well tested using the Karma test runner and Jasmine for [Unit and Acceptance Tests](https://github.com/thirdiron/browzine-discovery-service-adapters/tree/develop/tests) to guard against regressions. This project also integrates with CircleCI for continuous integration.

#### <i>Nomad Chrome Extension</i>

LibKey [Nomad](https://chrome.google.com/webstore/detail/libkey-nomad/lkoeejijapdihgbegpljiehpnlkadljb) is a Chrome extension that helps academic researchers quickly identify and download the PDF of research journal articles. Nomad provides one-click access to millions of scholarly articles and is supported by over 725 libraries in more than 30 countries!

![chrome browser extension screenshot](/images/chrome-browser-extension-1.png)

LibKey Nomad is a React based Chrome extension, leveraging Puppeteer and Mocha for automated acceptance test coverage. Nomad proved to academic researchers that journal article PDFs accessed through their library could be both fast and reliable.

#### <i>Ember CLI Upgrades</i>

One of the most frustrating pieces of Ember is upgrading to the latest versions of ember-cli. Lead the BrowZine upgrade to Ember 2.10.0 (Glimmer 2) and Ember 2.12.0 LTS. Additionally, lead the Ember Grand Testing Unification migration, the async/await updates and the upgrade plan to Ember 2.18.0 LTS, including the plan to refactor private API use out of our Acceptance Tests.


#### <i>Open Source Contributions (OSS)</i>

While working through the BrowZine Discovery Service Adapters deployment strategy, we realized we'd want to make the TTL for each adapter configurable.

We were already using a library called deploy-web-to-s3 to deploy the adapters to S3, but the library didn't expose a method to make the S3 Cache-Control header configurable. So went ahead and created a PR to expose the Cache-Control header using an environment variable called AWS_CACHE_CONTROL.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://github.com/revisohq/deploy-web-to-s3/pull/6">revisohq/deploy-web-to-s3</a></h4><p>A tool for easily recursively uploading a directory with client-side files to S3</p></blockquote>


During an ember-cli upgrade for BrowZine, found a critical bug in a major ember addon called ember-component-css. Analyzed the bug and submitted a PR to fix the same. We found the root cause to be in a dependency of ember-component-css called ember-cli-saas, but this PR helped folks make progress until we could get a fix upstream.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://github.com/ebryn/ember-component-css/pull/132">ebryn/ember-component-css</a></h4><p>An Ember CLI addon which allows you to specify styles for individual components</p></blockquote>


<br>

## Apollo HD

Sometimes you get the chance to write the best code of your life when you least expect it. I got that chance at [Respoke], a communication PaaS startup built on WebRTC.

![Apollo][apollo-dark]

As a JavaScript Engineer on the Respoke team, I helped developers see how easily we can add secure video, voice and data communication to our own apps using the power of WebRTC.

We used some of the most innovative front-end technologies of the day, including HTML5, CSS3 (LESS), Jade, Gulp, Bootstrap, JavaScript, ES6, Babel, jQuery, Angular, NodeWebkit, Jasmine, Sinon, SuperTest and Phantom:

![Capabilities][capabilities-2]

And with these, we built [Apollo](https://www.apollohd.com/) - A powerful Slack competitor that enables team collaboration with chat, screen sharing, live video and voice.


#### <i>Respoke Server Libraries</i>

Wrote Respoke PHP and Respoke Java server-side libraries.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://github.com/respoke/respoke-php/commits?author=tiandavis">respoke/respoke-php</a></h4><p>respoke-php - PHP serverside library for the Respoke REST API</p></blockquote>


<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://github.com/respoke/respoke-java/commits?author=tiandavis">respoke/respoke-java</a></h4><p>respoke-java - Java serverside library for the Respoke REST API</p></blockquote>


#### <i>Open Source Contributions (OSS)</i>

Contributed a critical bug fix to Respoke.js which prevented screen sharing from working in Firefox and Chrome.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://github.com/respoke/respoke/commits?author=tiandavis">respoke/respoke</a></h4><p>respoke - Respoke JavaScript Browser/Client Library</p></blockquote>


Contributed fixes to the respective browser plugins.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://github.com/respoke/respoke-firefox-screen-sharing-extension/commits?author=tiandavis">respoke/respoke-firefox-screen-sharing-extension</a></h4><p>respoke-firefox-screen-sharing-extension - A base Firefox extension for enabling screen sharing from your domain using respoke</p></blockquote>

<br>

Lead the reorganization and documentation of the Respoke docs to what you see today.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://github.com/respoke/docs/commits?author=tiandavis">respoke/docs</a></h4><p>Contribute to docs development by creating an account on GitHub.</p></blockquote>


<br>

Extracted Caramel from a Respoke internal tool I built to facilitate cross-platform rendering of Respoke's responsive transactional emails in the various email clients (Gmail, Outlook, Yahoo, Mobile, etc).

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://github.com/tiandavis/caramel">tiandavis/caramel</a></h4><p>caramel - Caramel: A responsive HTML email framework</p></blockquote>


<br>

Contributed Yahoo email client fixes upstream to Salted which eventually became the baseline for Respoke's and Caramel's responsive email framework.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://github.com/rodriguezcommaj/salted/commits?author=tiandavis">rodriguezcommaj/salted</a></h4><p>salted - Salted: A responsive email template</p></blockquote>



<br>
<br>

## Community Leadership

I believe in servant leadership and have always served the developer community first and my interests second.

<br>

### Community Contributions

Demonstrated both patience and empathy while managing external contributors to both Respoke's open source chan_respoke library and developer documentation.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://github.com/respoke/chan_respoke/pull/9">Added Channel Variables and AMI Event for Respoke Session by gcareri · Pull Request #9 · respoke/chan_respoke</a></h4><p>Added two new features: Set of Asterisk Channel Variables related to the Respoke Session AMI (Asterisk Manager Interface) new Event 'respoke_session' in order to show the Respoke Session informat...</p></blockquote>


<br>


### Developer Talks

Toured the east coast, introducing developers to WebRTC - a powerful HTML5 API for encrypted peer-to-peer Voice, Video and Data communications.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://speakerdeck.com/tiandavis/webrtc-unicorns-narwhals-and-the-real-time-web">WebRTC: Unicorns, Narwhals and The Real-Time Web</a></h4><p>You probably don't know WebRTC as much as you think. I'm not surprised. WebRTC is both amazing and terrifying. No real standards exist between browser vendors. How to integrate WebRTC the right way? WebRTC is but one ingredient to a successful real-time web recipe.</p></blockquote>


<script async class="speakerdeck-embed" data-id="b4a4e41f878b4955bb72c976329f1db7" data-ratio="1.77777777777778" src="//speakerdeck.com/assets/embed.js"></script>

Along with the talk, distributed a small sample signaling app using Node, Socket.IO showing developers how to get started with WebRTC quickly.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://github.com/tiandavis/native-webrtc-node-socket.io-signaling">tiandavis/native-webrtc-node-socket.io-signaling</a></h4><p>native-webrtc-node-socket.io-signaling - Sample app showing how to use the HTML5 WebRTC API</p></blockquote>




<br>

Another talk focused on the story of JavaScript as seen through the eyes of the Hero's Journey itself.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://speakerdeck.com/tiandavis/javascript-and-the-monomyth">JavaScript and The Monomyth</a></h4><p>JavaScript and The Monomyth explores the story of JavaScript as you've never seen before. Learn more about The Monomyth. Dig deeper into the story of JavaScript: https://tiandavis.com/thoughts/posts/javascript-and-the-monomyth</p></blockquote>


<script async class="speakerdeck-embed" data-id="6697f7a03472013238ed56e996df704e" data-ratio="1.77777777777778" src="//speakerdeck.com/assets/embed.js"></script>


<br>
<br>

## Strong technical writing skills

Take a look at a few screencasts and blog posts I produced along the way.


### Screencasts

Technical screencast on my favorite uses of the setInterval and setTimeout JavaScript timers.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://www.youtube.com/watch?v=BjgWfQ4UaHU">HTTP Polling Using JavaScript and jQuery</a></h4><p>Quick screencast on a few JavaScript polling techniques</p></blockquote>


<iframe width="100%" height="461" src="https://www.youtube.com/embed/BjgWfQ4UaHU" frameborder="0" allowfullscreen></iframe>

<br>


### Articles

Thought leadership technical blog post on blog.respoke.io discussing whether Google's WebRTC adapter.js is a shim or a polyfill and creating a framework for other developers to determine whether a JavaScript library is a shim or a polyfill.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="http://blog.respoke.io/post/111278536998/javascript-shim-vs-polyfill">JavaScript: Shim vs Polyfill</a></h4><p>I'm currently working on a conference talk about WebRTC. One of the foundations of any WebRTC library is some form of Google's original adapter.js, which seeks to normalize the WebRTC API across various browsers. As I was about to build this particular slide, one question started to whisper in my ear, "Is adapter.js a shim or a polyfill?"</p></blockquote>


Results?

Google search result rank number three for the topic.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://imgur.com/rFmqzLH"></a></h4><p></p></blockquote>


"@corgrath: The best article I have read so far regarding the shim vs polyfill terminology. Thanks :-)"

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://imgur.com/zteGlFL"></a></h4><p></p></blockquote>



<br>

Fun technical blog post written for blog.respoke.io mashing up two popular concepts: WebRTC and Instagram Filters.

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="http://blog.respoke.io/post/112690645356/webrtc-instagram-video-filters">WebRTC Instagram Video Filters</a></h4><p>With more than a $1 Billion valuation and over 75 million daily users, Instagram is arguably one of the most popular social networks today. Did you know more than 55 million photos are posted daily on Instagram? Or that the platform sees over 8,500 likes per second?</p></blockquote>


<br>

Thought leadership piece discussing the story of JavaScript told through the eyes of Joseph Campbell's "Hero's Journey".

<blockquote class="embedly-card" data-card-key="db853905f7da46498006d870b8bcb67c" data-card-controls="0"><h4><a href="https://tiandavis.com/thoughts/posts/javascript-and-the-monomyth">JavaScript and The Monomyth</a></h4><p>In his seminal work, "The Hero with a Thousand Faces", Joseph Campbell put forth the idea of The Monomyth. The idea is based on the observation that a common pattern exists beneath the narrative elements of most great myths, regardless of their origin or time of creation. Simply put, all of mankind's myriad myths are but variations of a single great story. This is the monomyth and is most commonly expressed as a hero's journey....</p></blockquote>


<br>
<br>

## What's next exactly...?

I'd love to learn more about the position, the team and the company. Go ahead, email me and we'll continue the conversation.






[Pieta]: https://en.wikipedia.org/wiki/Piet%C3%A0_(Michelangelo)
[code samples]: https://github.com/tiandavis
[8-Bit Hustler]: https://tiandavis.com/thoughts/posts/javascript-and-the-monomyth
[GitHub]: https://github.com/tiandavis
[Twitter]: https://twitter.com/tiandavis
[Columbus Code Camp]: https://columbuscodecamp.com/
[capabilities-1]: /images/capabilities-1.png "Core Capabilities"
[capabilities-2]: /images/capabilities-2.png "Core Capabilities"
[capabilities-3]: /images/capabilities-3.png "Core Capabilities"
[respoke-logo]: /images/respoke.png "Respoke"
[respoke]: https://www.respoke.io/ "Respoke Url"

[apollo-dark]: /images/apollo-dark.png "Apollo Dark"
[apollo-light]: /images/apollo-light.png "Apollo Light"
[apollo-group-conference]: /images/apollo-group-conference.png "Apollo Group Conference"
[apollo]: https://app.apollohd.com/#/ "Apollo"
[caramel]: https://github.com/tiandavis/caramel "Caramel"
[caramel-screenshot]: /images/caramel.png "Caramel"
[respoke-emails]: /images/respoke-emails.png "Respoke Emails"

[nationwide]: /images/nationwide.png "Nationwide"

[galileo-screenshot]: /images/galileo-screenshot.png "Galileo"

[galileo]: https://github.com/tiandavis/galileo "Galileo"

[companies]: /images/companies.png "Companies"

[browzine]: https://browzine.com/libraries/222/subjects

[browzine-subjects]: https://browzine.com/libraries/222/subjects/60?sort=rank

[browzine-discovery-service-adapters]: https://github.com/thirdiron/browzine-discovery-service-adapters

[Summon]: http://msulibrariestest.summon.serialssolutions.com/#!/search?ho=t&l=en&q=new%20england%20journal%20of%20medicine

[browzine-discovery-service-adapters acceptance tests]: https://github.com/thirdiron/browzine-discovery-service-adapters/blob/develop/tests/acceptance/browzine-summon-adapter-test.js

[browzine-discovery-service-adapters-tests]: https://github.com/thirdiron/browzine-discovery-service-adapters/tree/develop/tests
