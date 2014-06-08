---
layout: post
title:  "JavaScript and The Monomyth"
date:   2014-06-08 00:00:00
permalink: posts/javascript-and-the-monomyth
---

![The Hero's Journey][1]

In his seminal work, "The Hero with a Thousand Faces", Joseph Campbell put forth the idea of [The Monomyth][33]. The idea is based on the observation that a common pattern exists beneath the narrative elements of most great myths, regardless of their origin or time of creation.

Simply put, all of mankind's myriad myths are but variations of a single great story. This is the monomyth and is most commonly expressed as a hero's journey.

In this journey, the hero begins in the ordinary world, and receives a call to enter an unknown world of strange powers and events. The hero who accepts the call to enter this strange world must face tasks and trials, either alone or with assistance. In the most intense versions of the narrative, the hero must survive a severe challenge, often with help. 

If the hero survives, he may achieve a great gift or "boon." The hero must then decide whether to return to the ordinary world with this boon. If the hero does decide to return, he or she often faces challenges on the return journey. If the hero returns successfully, the boon or gift may be used to improve the world.

The Monomyth has three arcs: The Departure, The Initiation and The Return. Each arc has several sub arcs.

I want to stop here for a second because I want you to think about your favorite movie. Is it Frank Herbert's Dune? Or Star Wars? Or The Highlander? Is it Braveheart? Or The Matrix? Or maybe even Quentin Tarantino's Django?

These are all but variations of a single story. JavaScript is no different.

The story of JavaScript and how it came to be is an amazing story. But the people who gave it life and continue to nurture its growth are but actors in a greater story. 

Even in the telling of this story, you and I, experience the psychic unity of mankind. A unity that binds us to the craft. JavaScript is the hero here. This is its journey.


##The 17 Stages of the Monomyth

###The Departure

In a monomyth, the hero begins in the ordinary world, and receives a call to enter an unknown world of strange powers and events. The hero who accepts the call to enter this strange world must face tasks and trials, either alone or with assistance.

Collectively, mankind faced the beginnings of the strangest and most powerful of worlds it had ever created - The Internet. So sets the stage for our hero and the birth of a language...


####The Call to Adventure
*In the Call to Adventure, the hero begins in a mundane situation of normality from which some information is received that acts as a call to head off into the unknown.*

Early April 1995, Brendan Eich is recruited to Netscape with the promise of "doing Scheme" in the browser. Netscape recruited him because he could hack quickly and in part because he had some language chops. 

Explained Brendan, "I was 'that guy', not in any brag-worthy sense, just the only person who was in the position to do the deed, with (barely) enough skills to pull it off." 

Brendan goes on to explain, "Many hackers could have done a better job with more time, or perhaps a better job had they been in my shoes. Who knows? But no one at Netscape could have, and the opportunity was there and then", Brendan on the [Origins of JavaScript][10].

The opportunity was there and then and he took it. What a lot of folks don't know is Brendan worked for Netscape's founder's previous company Silicon Graphics Incorporated (SGI); That's how he was recruited to Netscape. 

SGI was a high performance computer designer/manufacturer. Think Alienware for business. SGI are also the folks that wrote and open sourced the C++ standard template library (STL). 

STL was an early standard library for C++ without which you'd have to write your own base data structures like lists, hashes, queues and the like. In his own words, his experience at SGI made him a "C/Unix fanboy". "I knew the C grammer by heart", he would later explain.

Things seldom go according to plan and little did he know both Scheme and C would play heavy on his design of JavaScript.


####Refusal of the Call
*Often when the call is given, the future hero first refuses to heed it. This may be from a sense of duty or obligation, fear, insecurity, a sense of inadequacy, or any of a range of reasons that work to hold the person in his or her current circumstances.*

Brendan never did put Scheme in the browser. Instead, he created a new language called JavaScript. As he remembers it, "[t]he diktat from upper engineering management was that the language [must 'look like Java'][2]."

After partnering with Sun Microsystems, the creators of Java, Netscape management was firm that whatever language created should be "Java's kid brother". 

The plan was to bring Java to the Netscape browser in the form of Java Applets. Then use JavaScript to tie everything together. The Netscape/Sun deal was to make Java for "professional" developers and JavaScript, well, for everyone else. The express goal was to embed that programming language in the source HTML of Netscape Navigator.

Management only cared about two things. First, the new language look like Java. Finally, the new language have objects without classes. In their mind, a dumbed down version of Java. In Brendan's mind, challenge accepted...

Following a subversive agenda, Brendan borrowed closures and first-class functions from Scheme. Then, he borrowed the concept of prototypical inheritance from Self. Whereas Scheme was a dialect of Lisp, Self was a dialect of Smalltalk. Finally, he borrowed the look-and-feel of the language from C/C++.

In class-based object oriented languages, classes define the properties and behaviors of objects. Object instances are then particular manifestations of a class. 

In Self, however, one makes a copy of an existing object and then adds additional specific properties and behaviors. Code which uses the existing objects are not changed.

These would form the necessary ingredients for creating JavaScript, but it would take an act of God to birth the language into existence. In the software development industry, we call these acts of god a release.


####Supernatural Aid
*Once the hero has committed to the quest, consciously or unconsciously, his guide and magical helper appears or becomes known. More often than not, this supernatural mentor will present the hero with one or more talismans or artifacts that will aid them later in their quest.*

Netscape 2.0 Beta's [extremely tight release schedule of March 1996][12] forced Brendan to complete the first version of JavaScript in only [ten days][13]. Management at Netscape was sure Microsoft was gunning for them, after turning down a low ball offer to buy Netscape earlier that year. 

What's the old saying, "Just because you're paranoid doesn't mean they aren't after you." In this case, Microsoft was out for Netscape and the killer was to be VBScript in Internet Explorer. Things were about to get real - real fast...!

Though still the market leader in web browsers, Netscape speed up its release of Netscape 2.0. I like to think of that release as a crucible. In went Brendan Eich, his experiences with Scheme, Self, Java and C; his marching orders for the language to "look like Java" and "have objects without classes". 

Those things were the raw [Tamahagane][11]. 

Through those inhomogeneous mixtures of concepts and directives a finer language would reveal itself. Through the crucible, out came what would be one of the most popular programming languages in the world.

And once the soot was removed and the steel polished, JavaScript was born.


####Crossing the Threshold
*This is the point where the person actually crosses into the field of adventure, leaving the known limits of his or her world and venturing into an unknown and dangerous realm where the rules and limits are not known.*

During the Fall of 1996, Brendan [rewrote the JavaScript language][14] and built the first-ever JavaScript engine. This engine is code named SpiderMonkey and is later released as open source. JavaScript is finally decoupled from the Netscape browser. JavaScript is standardized as ECMA-262 specification called EMCAScript.

Microsoft implements JavaScript for the first time in Internet Explorer 3.0 in August 1996 - Here, it is called JScript. As explained by JavaScript guru Douglas Crockford in his talk titled The JavaScript Programming Language on YUI Theater,

[Microsoft] did not want to deal with Sun about the trademark issue, and so they called their implementation JScript. A lot of people think that JScript and JavaScript are different but similar languages. That's not the case. They are just different names for the same language, and the reason the names are different was to get around trademark issues.

Today, ["JavaScript" is a trademark of Oracle Corporation][9]. It is used under license for technology invented and implemented by Netscape Communications and current entities such as the Mozilla Foundation.

Around this time in 1997, a fork of SpiderMonkey is developed at Netscape called [Rhino][15]. Where SpiderMokey is written in C, Rhino is developed entirely in Java. At the time, Netscape was planning to produce a version of Netscape Navigator written fully in Java and so it needed an implementation of JavaScript written in Java.

Of course Rhino could be embedded into any Java application to provide scripting to end users. Say for example you wanted to build a version of Excel running on top the JVM. And say your wanted to provide scripting capabilities in Excel similar to VBA. 

How would you do it? Well, you could use Rhino and voila your Excel-ish application can provide users with scripting abilities written in JavaScript.

From here on out, JavaScript would be free from confinement to any one single browser. Yet future funding of this open source language was still confined to a handful of proprietary, nominally closed source companies. Something had to give...

The gods must have seen the irony because it wouldn't be too long before this situation came to a head.



####Belly of the Whale
*The belly of the whale represents the final separation from the hero's known world and self. By entering this stage, the person shows willingness to undergo a metamorphosis.*

Early 1998, Netscape along with Brendan found the Mozilla Project. Named after the original code name of the Netscape Navigator browser which is a blending of "Mosaic and Godzilla".

The Mozilla Project is meant to manage open-source contributions to SpiderMonkey and  Netscape's Mozilla Suite - an open source browser and email client combined. A small group of Netscape employees were tasked with coordination of the new community. Brendan serves as the group's first chief architect.

That same year whispers begin that AOL plans to buyout Netscape and shutdown the Netscape browser. A year later in 1999, AOL does buy Netscape. However, the shutdown doesn't come for another four years. 

Then in July 2003, AOL officially shuts down its Netscape browser unit. That same month, Brendan helped create the Mozilla Foundation as the legal steward the Mozilla Project. 

Soon after, the Mozilla Project deprecated the Mozilla Suite in favor of creating independent applications for web browsing and email. The Firefox web browser and the Thunderbird email client were born.

This way, the SpiderMonkey JavaScript Engine found a new home in Mozilla's Firefox web browser. Later in 2005, Brendan becomes the CTO of the for-profit arm of the Mozilla Foundation - the Mozilla Corporation. 

JavaScript was now on the golden path. In addition to not being tied to a single browser, now it would be funded, indefinitely by a foundation dedicated to its future and the future of us all.


###The Initiation

In the most intense versions of the narrative, the hero must survive a severe challenge, often with help. If the hero survives, he may achieve a great gift or "boon."

When Java applets failed, JavaScript became the de-facto language of the Web.

With a growing number of browser vendors, the future of JavaScript laid on the foundation of inconsistent implementations and frustrated developers.

Yet, with a little help, the promise of JavaScript everywhere had a very real chance to succeed. But, it wasn't easy...


####The Road of Trials
*The road of trials is a series of tests, tasks, or ordeals that the person must undergo to begin the transformation. Often the person fails one or more of these tests, which often occur in threes.*

Luke Skywalker had his Lightsaber training with Obi-Wan Kanobi. Neo his sparring with Morpheus. They had it easy...

Had they faced learning JavaScript, in what was our stone age, they would have failed like so many of us. Between 2003 and 2005, three major factors played a pivotal role for JavaScript as a development language and they didn't work in its favor. 

First, the number of web browser vendors was growing. Then the Document Object Model (DOM) was a mess. Finally, JavaScript organization was an improbability.

As far as web browser vendors, there was Netscape of course, but then there was also Internet Explorer (Windows and Mac OSX). There was the burgeoning Firefox and growing in popularity was Safari and Opera. 

Each implemented the spec in their own slightly different vision. Some were worse than others - I'm looking at you Microsoft. The implementation of some JavaScript objects were radically different across browser vendors. 

Some browser vendors didn't implement certain objects at all or implemented them with another name and slightly different responsibility. Those were the best cases. At the worse end, you had browsers like Internet Explorer (IE) which implemented its own proprietary extensions and functionality. 

What that meant is if you wrote your code against IE first, your goose was pretty much cooked. A lot of enterprise companies realized this far far to late and carte blanche told developers to write code against IE and IE only. 

Most developers either didn't know the self-defeating result of such policies or simply didn't care. For the craftsman, however, it would be years until they could stand against such tyranny with both competence and a following. 

Until then, supporting as many browsers as possible would continue to be an uphill battle. Later, we would find that each browsers Document Object Model (DOM) implementation was just as bad - if not worse...!

The [DOM][16] was a also mess. CSS selectors were inconsistent. DOM modification from JavaScript was inconsistent. Event management was downright agonizing. 

Even the most widely used DOM method - getElementById - returned inconsistent results from every browser. But it wasn't just that method, nearly every DOM method was broken in some way, in some browser. 

Moral of the story was if there's a DOM method, there's probably a problem with it somewhere, in some capacity. All of this was compounded by the growing popularity of JavaScript and its frenzied, almost barbarian integration to come.

[Dynamic HTML][17] (DHTML) techniques had grown in popularity. It wasn't long before developers took to JavaScript like a fat kid to cake. JavaScript was all over there place like spaghetti with a toddler. 

By the time most of us joined a team, JavaScript was scattered inline throughout HTML. There were monstrous JavaScript files. Sometime so many they would make you dizzy. 

I once showed up to a client to find JavaScript stored in database tables and spewed out to the user like a bad burrito. Those were the times when you prayed to the Gods. It was monstrous to the point of culpability. JavaScript organization was without reason. More crime than art. 

Too many browsers, the DOM was a mess and JavaScript organization was a thing unheard of. Yet, all this insanity was sort of, well - beautiful. Beautiful because it showed developers identified with JavaScript. It showed a willingness to push the language further than anyone thought possible. 

It was this willingness to go beyond that would form a fundamental cornerstone of the JavaScript community. And with such a large elephant, we began to eat it piece by delicious piece.


####The Meeting with the Goddess
*This is the point when the person experiences a love that has the power and significance of the all-powerful, all encompassing, unconditional love that a fortunate infant may experience with his or her mother. This is a very important step in the process and is often represented by the person finding the other person that he or she loves most completely.*

January 2006, John Resig released [jQuery at BarCamp NYC][18]. jQuery opens the door for JavaScript to run consistently in every browser. Up until now, no one had taken on the challenge to reconciled JavaScript behavior across disparate browser vendors.

The promise was simple - write your JavaScript against jQuery and your code was guaranteed to run in every browser. Now, it is common place to use jQuery. But, back then, not many people stopped to wonder what it could be to have JavaScript just work.

Not surprising when you think about it because most code was server-side. In fact, ajax techniques had just barely started to become known. All this meant was folks simply didn't care about the frontend. All that changed with jQuery. Because of jQuery developers started to wake up and start noticing JavaScript.

Now, clearly John is not a Goddess and neither is he a God. It funny because The Matrix had the Oracle and the Oracle was able to see a person's destiny. Well, I felt like John is our Oracle and he saw not just what JavaScript was, but what it could be.

Because of John and jQuery, collectively, we realized the dream of cross-browser development. We had finally normalized JavaScript development and laid a solid foundation for innovation. During this time, John taught us about the DOM in all its shabby self.

Non-Obtrusive JavaScript (no inline JavaScript) started to become a very real possibility. JavaScript code organization would still remain a mess for quite some time unfortunately. But, at least it worked as expected. 

It wouldn't be long before jQuery became synonymous with cross-browser JavaScript development, but it didn't get there without challenges.


####Temptation away from the true path
*In this step, the hero faces those temptations, often of a physical or pleasurable nature, that may lead him or her to abandon or stray from his or her quest.*

You don't have to wonder where JavaScript would be without jQuery. For me, the answer is clear...Nowhere! Without cross-browser compatibility, JavaScript would have been of very little use. 

So, for but a moment, I dare you to imagine a world without jQuery. What if I told you that was almost the case? It was...

With jQuery and the dream of cross-browser development in its infancy, many developers were courted by and tempted away by other JavaScript frameworks like MooTools, Prototype and ExtJS. So began The Framework Wars...

In hindsight, all three brought classical object oriented programming to JavaScript. Genius really...But its hard to say whether the larger development community were ready for these concepts at the frontend. 

It wasn't like today where domain logic is steadily moving frontward. Back then, domain logic was firmly planted server-side and most developers were struggling with object oriented concepts even there, much less in a prototypical environment. For these early frameworks, classical OOP turned to be a deadly weakness in spite of its overall strength. 

You see, most JavaScript consumers at the time really had no idea the history of the language or how powerful it could be. To them it was a scripting language and "everyone" knew you didn't do heavy lifting with those things. So hitting them with classes and design patterns right off the bat was like opening a first date with, "So...I met this amazing wedding planner." It was simply too much. 

Not bad in and of itself - just too much too fast. Besides, most developers didn't come for code organization and design patterns, they came for the plugins - calendars, accordion menus and the like were all the rage...

In the beginning, jQuery looked really promising but the plugins were ugly. MooTools had some really beautiful plugins, but the Community believed you should only use one JavaScript framework and they weren't budging. ExtJS simply felt too heavy.

No one knows how the war started. As with all wars, the issue was about assets and who would go on to own the dollar ($) alias. It seems silly now, but folks risked mixing multiple frameworks to use widgets they liked from each.

Developers were used to mixing widget libraries from the DHTML days. Now, they were just happy these widgets would work in multiple browsers. But as with things too good to be true, there was a catch...


####Atonement with the Father
*In this step the person must confront and be initiated by whatever holds the ultimate power in his or her life. In many myths and stories this is the father, or a father figure who has life and death power. This is the center point of the journey. All the previous steps have been moving into this place, all that follow will move out from it.*

Around May 2008, almost two years after the initial release of jQuery, The Framework Wars peaked. But with developers firmly in either camp, this war would be won with converts.

As integral as the dollar ($) alias was, no framework wanted to change their use of the dollar ($) alias just to suit "some other framework".

This made it difficult to mix and match components from different frameworks without them clobbering each other. This was the turning point for the future of JavaScript and its proliferation to the masses.

Then came jQuery.noConflict()...

Using jQuery.noConfict() John and the jQuery team allowed developers to continue to use jQuery's dollar ($) sign while still allowing other frameworks to work properly.

What John Resig and the jQuery Core Team realized was that people used the dollar ($) alias for [efficiency not identity][31]. So why not let other frameworks use the $ alias and give jQuery developers the best of both worlds.

As a result, jQuery developers didn't have to choose efficiency over flexibility. While the other frameworks pandered, "One Framework to Rule Them ALL", jQuery introduced jQuery.noConflict(), played it's hand and moved aside.

After trying jQuery, many developers never went back to either MooTools, Prototype or ExtJS. Instead, they opted to rewrite their most favorite plugins in jQuery. What came next was the Golden Age of jQuery.


####Apotheosis (becoming god-like)
*This step is a god-like phase where the hero earns a period of rest, peace and fulfillment before the hero begins the return.*

May 2008, Douglas Crockford published his seminal book "[JavaScript: The Good Parts][19]". 

Here, Crockford identified the abundance of good ideas that make JavaScript an outstanding object-oriented programming language-ideas such as functions, loose typing, dynamic objects, and an expressive object literal notation.

Later that year, in September 2008, Microsoft switches out its own [AJAX library for jQuery][3] and ships jQuery with Visual Studio. Two years later, in March 2011, the popular Ruby web framework, Ruby on Rails, switched out [Prototype for jQuery][4].

As JavaScript had become the de-facto programming language of the web, jQuery had become the de-facto JavaScript normalization framework of the web.


####The Ultimate Boon
*The ultimate boon is the achievement of the goal of the quest. It is what the person went on the journey to get. All the previous steps serve to prepare and purify the person for this step, since in many myths the boon is something transcendent like the elixir of life itself, or a plant that supplies immortality, or the holy grail.*

jQuery opened cross-browser JavaScript development to all developers. Later libraries either made jQuery the foundation for interacting with the browser or implemented a compatible (sometimes identical) API.

JavaScript was becoming a language for "real" developers. Consistent behavior in every browser was our version of the elixir of life...It was our holy grail and led to many innovations.

JSON or [JavaScript Object Notation][20] became the standard for transmitting objects between a server and web application using Ajax. 

The brainchild of Douglas Crockford, JSON uses human-readable text to transmit data objects consisting of attribute–value pairs. It is used primarily to transmit data between a server and web application and steadily became an alternative to XML.

Libraries like [Raphael][21] show us we never needed flash for beautiful interactive graphics. It also showed us what a commitment to cross-browser consistently can yield. 

Raphael is a cross-browser JavaScript library that draws Vector graphics for web sites. It will use SVG for most browsers, but will use VML for older versions of Internet Explorer. 

Though the DOM remained a mess, JavaScript normalization libraries like jQuery shield us from its quirks. However, JavaScript code organization remained messy for some time. Yet, as innovation grew, so grew the potential for sane JavaScript with it.


###The Return

The hero must then decide whether to return to the ordinary world with this boon. If the hero does decide to return, he or she often faces challenges on the return journey. If the hero returns successfully, the boon or gift may be used to improve the world.


####Refusal of the Return
*Having found bliss and enlightenment in the other world, the hero may not want to return to the ordinary world to bestow the boon onto his fellow man.*

John leaves the Mozilla Corporation, and work on jQuery, to join the Khan Academy. The project is left in the hands of a core group of developers. 

JavaScript is now cross-browser, but code organization is still a mess and often turns into spaghetti code. Lighter weight versions of jQuery, optimized for mobile devices show up like Zepto, but they only support IE10+.

But something else was brewing under the covers. Something very few people saw coming. The very way some started to write JavaScript changed entirely. The age of the Designer Language began...

####The Magic Flight
*Sometimes the hero must escape with the boon, if it is something that the gods have been jealously guarding. It can be just as adventurous and dangerous returning from the journey as it was to go on it.*

A [Designer Language][6] is a programming language created to avoid the perceived shortcomings of an existing language, usually by creating a superset of the existing language by modifying syntax or modifying programming constructs.

In late 2009, Jeremy Ashkenas, quietly committed [CoffeeScript][22] to the JavaScript world. CoffeeScript was a programming language that [transcompiled][23] to JavaScript. It was also the first designer language to bring back the concept of class based programming to JavaScript. In a short two years, CoffeeScript managed to influence legions of developers.

Eventually, CoffeeScript made its way to Brendan Eich - The Creator of JavaScript - inevitably influencing the future of the language.

Inspired by Ruby, Python and Haskell, CoffeeScript went on to become the default JavaScript language in the popular Ruby on Rails web framework. 

With those results, CoffeeScript is (arguably), the most successful designer language ever released. But that was just the beginning of JavaScript's designer languages.

Google Web Toolkit or GWT attempted to transpile Java to JavaScript (Oh how the mighty had fallen). Dart, GWT's predecessor, was Google's attempt to make GWT more like JavaScript. Effectively, Dart was Google's answer to CoffeeScript.

Later, Microsoft would attempt to answer CoffeeScript with there own language called TypeScript. Both TypeScript and Dart would attempt to bring static typing to JavaScript.

ClosureScript transpiled Closure, a dialect of LISP written for the JVM, to JavaScript. Objective-J, though short lived, had identical syntax to Objective-C and transpiled to JavaScript as well.

What's interesting is most designer languages still allowed you to use all your favorite frontend frameworks like jQuery. Though some like GWT and Objective-J do not because they provide their own underlying framework.

Times were changing rapidly. The grassroots investment in JavaScript by the development community didn't go unnoticed. JavaScript became the [most popular language used on GitHub][24].
 

####Rescue from Without
*Just as the hero may need guides and assistants to set out on the quest, oftentimes he or she must have powerful guides and rescuers to bring them back to everyday life, especially if the person has been wounded or weakened by the experience.*

Around this time, [Apple dropped support for Flash][25] on its new iPhone in favor of more open standards like HTML5, CSS and JavaScript. In subsequent years, [Adobe itself would drop support for Flash][8] on mobile devices all together. 

Microsoft drops support for IE6 as the [countdown][26] to the death of IE6 continued. jQuery would later create a project fork that drops support for IE6 as to decrease the libraries bloat.


####The Crossing of the Return Threshold
*The trick in returning is to retain the wisdom gained on the quest, to integrate that wisdom into a human life, and then maybe figure out how to share the wisdom with the rest of the world.*

[Micro MVC libraries][7] arise to offer JavaScript code organization along with jQuery integration. Some of those libraries include Backbone, KnockOut, Spine and JavaScriptMVC (CanJS). 

Backbone, written by the creator of CoffeeScript - Jeremy Ashkenas, is a JavaScript library with a RESTful JSON interface and is based on the model–view–presenter (MVP) design pattern. 

Backbone is lightweight and its only hard dependency is Underscore - also written by Jeremy. Underscore is a JavaScript library which provides utility functions for common programming tasks and delegates to native browser implementations when present or a compatible version when absent.

KnockOut, Spine and JavaScriptMVC (CanJS) all aimed to organize JavaScript as Backbone did, but with each its own unique approaches. 

Around this time, Google open sources its V8 engine. Like its ancestor, SpiderMonkey, V8 is an open source JavaScript engine. V8 is the JavaScript engine behind Google's Chrome web browser.

Later, projects like [NodeJS][27] use the V8 engine to turn JavaScript into a legitimate server-side language. This was the first server-side JavaScript runtime. But it was the first to realize a thriving ecosystem. 

Node gave us real-time, two-way connections using the HTML5 WebSocket protocol. The primary method to take advantage of HTML5 WebSockets was through [Socket.IO][28].

Socket.IO is a JavaScript library for realtime web applications. It has two parts: a client-side library that runs in the browser, and a server-side library for NodeJS. Both components have a nearly identical API. Like NodeJS, it is event-driven.

Socket.IO primarily uses the HTML5 WebSocket protocol, but if needed can fallback on multiple other methods, such as Adobe Flash sockets, JSONP polling, and AJAX long polling, while providing the same interface.

Socket.IO normalized WebSockets across disparate browsers. Using Socket.IO, you can guarantee WebSocket consistently across all the major browsers. Socket.IO is to HTML5 WebSockets as jQuery was to JavaScript.

What's interesting about this is as the HTML5 spec grew nearer to completion, micro libraries grew to fill the consistency gap as browser vendors normalized functionality.

JavaScript begins to show up in microcontrollers like Raspberry PI and Arduino. JavaScript starts showing up in flight drones like the AR Drone and Parrot as its programming language. Even object databases like MongoDB store objects as JSON.

It was starting to become clear to everyone that JavaScript was now simply everywhere...


####Master of Two Worlds
*Mastering two worlds is usually represented by a transcendental hero like Jesus or Buddha. The person has become comfortable and competent in both the inner and outer worlds.*

With the advent of NodeJS, it was now possible to use JavaScript throughout the entire application stack. JavaScript had mastered the server-side and the frontend as well. Core business logic moved from the server to the frontend.

Essentially, the server becomes just another API which is consumed by various frontends. So the Single Page Application (SPA) arose. Now the debate isn't which server-side web application framework do I use, instead many developers ask what frontend framework do I use to organize my code? 

Frontend MVC frameworks like Ember and Angular arise to answer that question. [Ember][29] provides an opinionated framework with coverage for common uses cases and is unobstructive with jQuery integration. Ember is the Rails of JavaScript.

[Angular][30] has elements of inline JavaScript called directives. Most common scenarios must be implemented by the developer. But its not really inline JavaScript, just custom Angular properties embedded in HTML. If jQuery is not present in your script path, Angular falls back to its own implementation of a subset of jQuery Google calls jQLite.

The major competition to both Ember and Angular is the micro MVC library Backbone. Most developers combine Ember for code organization with jQuery for DOM manipulation. 

Some developers mix in a designer language like CoffeeScript, TypeScript or Dart. However, the majority of developers continue to use and refine their knowledge of JavaScript.

JavaScript and how best to use it is now a central analysis for custom web applications. Much thought was now needed to make sound engineering decisions. 

JavaScript was now for serious engineers...


####Freedom to Live
*Mastery leads to freedom from the fear of death, which in turn is the freedom to live. This is sometimes referred to as living in the moment, neither anticipating the future nor regretting the past.*

Frontend development is now a legitimate software profession. Developers get to choose whether to focus on frontend development or server-side development. No longer is frontend development a nice-to-have with server-side being core.


JavaScript is now the most popular programming language on the planet. But, where do we go from here?

That I leave to you...



##Common Mythic Elements

There are [common mythic elements][32] in all monomyths. Here's how JavaScript compares to Star Wars and The Matrix:

Campbell                                                                     | Star Wars                                                                                                               | The Matrix                                                                          | JavaScript                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
Two Worlds (mundane and special)                                             | Planetside vs. The Death Star                                                                                           | Reality vs. The Matrix                                                              | Server-side vs Frontend                                                                            
The Mentor                                                                   | Obi-Wan Kenobi                                                                                                          | Morpheus                                                                            | Douglas Crockford                                                                                  
The Oracle                                                                   | Yoda                                                                                                                    | The Oracle                                                                          | John Resig                                                                                         
The Prophecy                                                                 | Luke will overthrow the Emperor                                                                                         | Morpheus will find (and Trinity will fall for) "The One"                            | JavaScript will run everywhere                                                                     
Failed Hero                                                                  | Biggs                                                                                                                   | In an early version of the script, Morpheus once believed that Cypher was "The One" | MooTools, Prototype                                                                                
Wearing Enemy's Skin                                                         | Luke and Han wear stormtrooper outfits                                                                                  | Neo jumps into agent's skin                                                         | GWT uses Java to write frontend code                                                               
Shapeshifter (the Hero isn't sure if he can trust this character)            | Han Solo                                                                                                                | Cypher                                                                              | CoffeeScript (Designer Languages generally)                                                        
Animal familiar                                                              | R2-D2, Chewbacca                                                                                                        | N/A                                                                                 | SpiderMonkey                                                                                       
Chasing a lone animal into the enchanted wood (the animal usually gets away) | Luke follows R2 into the Jundland Wastes; The Millennium Falcon follows a lone TIE fighter into range of the Death Star | Neo "follows the white rabbit" to the nightclub where he meets Trinity              | Brendan Eich joins Netscape to create scheme for the browser, where he invents JavaScript instead. 







[1]: /images/new-chart-of-history.jpg  "The Hero's Journey"
[2]: https://brendaneich.com/2008/04/popularity/
[3]: http://blog.jquery.com/2008/09/28/jquery-microsoft-nokia/
[4]: https://twitter.com/dhh/statuses/45923430608023552
[6]: http://techoctave.com/c7/posts/90-designer-languages
[7]: http://blog.stevensanderson.com/2012/08/01/rich-javascript-applications-the-seven-frameworks-throne-of-js-2012/
[8]: https://forums.adobe.com/message/4580870
[9]: http://tsdr.uspto.gov/#caseNumber=75026640&caseType=SERIAL_NO&searchType=statusSearch
[10]: https://news.ycombinator.com/item?id=2783060
[11]: http://en.wikipedia.org/wiki/Japanese_swordsmithing#Metallurgy
[12]: http://www.jwz.org/gruntle/nscpdorm.html
[13]: http://www.jwz.org/blog/2010/10/every-day-i-learn-something-new-and-stupid/#comment-1048
[14]: https://brendaneich.com/2011/06/new-javascript-engine-module-owner/
[15]: http://en.wikipedia.org/wiki/Rhino_(JavaScript_engine)
[16]: http://ejohn.org/blog/the-dom-is-a-mess/
[17]: http://en.wikipedia.org/wiki/Dynamic_HTML
[18]: http://ejohn.org/blog/bar-camp-nyc/
[19]: http://www.amazon.com/JavaScript-Good-Parts-Douglas-Crockford/dp/0596517742
[20]: http://en.wikipedia.org/wiki/JSON
[21]: http://raphaeljs.com/
[22]: http://coffeescript.org/
[23]: http://en.wikipedia.org/wiki/Source-to-source_compiler
[24]: http://redmonk.com/dberkholz/2014/05/02/github-language-trends-and-the-fragmenting-landscape/
[25]: http://www.apple.com/hotnews/thoughts-on-flash/
[26]: http://www.modern.ie/en-us/ie6countdown
[27]: http://nodejs.org/
[28]: http://socket.io/
[29]: http://emberjs.com/
[30]: https://angularjs.org/
[31]: http://tiandavis.com/posts/rails-3-and-the-jquery-effect/
[32]: http://www.moongadget.com/origins/myth.html
[33]: http://en.wikipedia.org/wiki/The_Hero_with_a_Thousand_Faces
