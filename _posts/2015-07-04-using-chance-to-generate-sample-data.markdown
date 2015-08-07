---
layout: post
title:  "Using Chance.js To Generate Sample Data"
date:   2015-07-04 00:00:00
permalink: posts/using-chance-to-generate-sample-data
---

![Chance.js](/images/chancejs.png)

It's not like writing sample data is hard per se. I just always felt like it was unnecessary. Most of the time you're trying to deliver business value. 

You're certainly not trying to build the world's greatest random number generator. And you're definitely not trying to build the world's greatest random email generator either. Unless you're [chance.js](http://chancejs.com/#gender) that is.

###What is Chance

Chance is a JavaScript micro library, narrowly focused on generating random data. That data could be as general as a random number or random string. Or Chance can be as specific as a random last name or a random phone number. 

Chance comes in great during automated testing, but it is also incredibly useful when working with peer-to-peer WebRTC apps as well because it helps you generate random conference rooms and other data.

###How to use Chance

####Generating Random User Data

For example, say you're working with a new instance of [Respoke](https://www.respoke.io/):

{% highlight js %}
var client = new respoke.Client({
    appId: '918e31a3-34aa-40f8-aa4c-b5409f9e4053',
    developmentMode: true
});
{% endhighlight %}

When connecting, you'd supply Respoke with a unique endpointId identifying the person connecting:

{% highlight js %}
client.connect({
    endpointId: endpointId
});
{% endhighlight %}

Think of your endpointId as a unique username or email address or some other unique data point. Using Chance, we have a few good options to work with.

First, we could use Chance to generate a random email address:

{% highlight js %}
client.connect({
    endpointId: chance.email()
});
{% endhighlight %}

If you need to use a particular domain, you could set that using Chance as well:

{% highlight js %}
client.connect({
    endpointId: chance.email({domain: 'respoke.io'})
});
{% endhighlight %}

Another potential use here is to generate a random Twitter username:

{% highlight js %}
client.connect({
    endpointId: chance.twitter()
});
{% endhighlight %}

The great part is you didn't have to write a single utility function.

####Generating Random Room Data

Once connected to Respoke, you'd want to then create a new group or join an existing group. Here, you could use Chance to generate a random group name.

You could use Chance to generate a random Black Berry Pin:

{% highlight js %}
client.listen('connect', function() {
  client.join({
      id: chance.bb_pin() //'985de771'
  });
});
{% endhighlight %}

Or you could you use Chance to generate a random Facebook Id:

{% highlight js %}
client.listen('connect', function() {
  client.join({
      id: chance.fbid() //'1000039460258605'
  });
});
{% endhighlight %}

Or you could you use Chance to generate a random Unix timestamp:

{% highlight js %}
client.listen('connect', function() {
  client.join({
      id: chance.hammertime() //2273327300317
  });
});
{% endhighlight %}

My personal favorite is the hammertime method. How could you not love a library with a method called hammertime?

According to startup lore, Hammertime was coined by a startup whose founder had an interesting interaction with M.C. Hammer. There was no name given to "Unix time with milliseconds" and while brainstorming ideas (because Unix time with milliseconds is a confusing mouthful), someone suggested Hammertime and it stuck.

Chance is a pretty neat library for generating lots of random data. Data you would have otherwise had to craft yourself. Give it a chance...See what I did there? ;)