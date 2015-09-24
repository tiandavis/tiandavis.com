---
layout: post
author: Tian Davis
title:  "The History of The PSTN"
date:   2014-11-21 00:00:00
permalink: /thoughts/posts/the-history-of-the-pstn
---


![pstn-2](/images/pstn-2.jpg)

###SUMMARY

[Respoke](https://www.respoke.io/) gives you the power to build the next Skype in the browser, on your smartphone and even on your desktop. It's all possible because of the [Public Switch Telephone Network](http://community.respoke.io/t/sign-up-now-for-our-pstn-beta/65) (PSTN). Here's a look at where the PSTN has been and where we're taking it...


###HISTORY OF THE PSTN

The history of the public switched telephone network (PSTN) is the history of American Bell and AT&T. In 1875 Alexander Bell formed the American Bell Telephone Company. A year later in 1876, Alexander Bell patented the first [improvement in telegraphy](http://www.google.com/patents/US174465) and made the first ever voice transmission over wire. It was hardly what we can imagine today.

The first voice transmission used what is called a ring-down circuit. What that means is there were no dialing of numbers; No ringing of headsets. Instead, an actual physical wire connected two devices. Remember when you were a kid and you'd play tin can telephone. What did you do? You connected two tin cans by wire. Then you could here your friend talk on the other end. A ring-down circuit is a lot like playing tin can telephone, just over a greater distance.

Initially, telephone users had to whistle into the phone to attract the attention of another telephone user. Within a year of Alexandar's patent, he added a calling bell to make signaling easier.

Over time, this simple design evolved from a one-way voice transmission, by which only one user could speak, to a bi-directional voice transmission, whereby both users could speak. Things started to get a little more complicated at this point. 

Moving the voices across the wire required a carbon microphone, a battery, an electromagnet, and an iron diaphragm. The concept of dialing a number to reach a destination still didn't exist. The also process required a physical cable between each location that the user wanted to call. Clearly this does not scale...

Placing a physical cable between every household that required access to a telephone was neither cost effective  or feasible. Bell developed another method that could map any phone to another phone without a direct connection. Bell patented the device and called it a [switch](http://www.google.com/patents/US911968). 

With a switch telephone, users only needed connection to a centralized office. Then that centralized office could coordinate connected the call to its final destination.

Imagine a pair of copper wires running from every phone to a central exchange in your town. At the exchange, the operator had a big switchboard. The switchboard had a 2 pin connection socket - called a jack socket - for every pair of wires entering the exchange.

When you wanted to talk to another person, you would ring the operator and give the name or number of the other party. Then the operator would connect a patch cord ( a 2 wire cable with a jack plug on each end ) between the two phones and the two people could communicate. Using a patch cord - a two wire cable with a jack plug on each end - the operator would connect each party's jack socket. Then the receiving party's telephone bell would ring and the two parties could communicate.

Believe it or not, the [first operators were teenage boys](http://www.telcomhistory.org/operators.shtml). Surprising - I know - but they often engaged in horseplay and foul language:

![pstn-2](/images/pstn-1.jpg)

Telephone companies soon began hiring young women in order to present a more civilized image to customers: 

![pstn-2](/images/pstn-2.jpg)

Women would go on to dominate the switchboard profession. Operators were well trained in switchboard technique and in deportment, before starting work on the switchboards. Here are a group training in switchboard technique and in deportment before starting work on the switchboard. Denver, Colorado 1910:

![pstn-2](/images/pstn-3.jpg)

Here's another group of operators at a switchboard in Santa Fe, New Mexico 1921:

![pstn-2](/images/pstn-4.jpg)

Bundles of wires called trunks ran between exchanges, forming proto-networks. Networks connected together until they connected countries across the world. This was the beginning of the PSTN.

At first the telephone operator acted as a switch. Fast forward 100 years - give or take a decade - and the electronic switch replaced the human switch.


###THE PSTN TODAY

What started as direct home to home connections, evolved into home to central switch connections. Human powered switches we called operators evolved into [analog switches](http://www.voip-sip.org/analog-telephony/) and then into electronic switches. A lot also changed along the way.

![pstn-2](/images/pstn-5.jpg)

Analog voice signals carried across the wire with amplifiers evolved into digital signals carried across the globe with repeaters. Repeater simply repeat whatever binary data it receives. If the repeater received 010101, it passed on 010101.

All digital meant cleaner sound quality travelled over longer and longer distances. It also meant the PSTN could release new features faster. Features like call waiting and call forwarding and conference calling were now built into the PSTN message driven network.

As technology progressed, the telephony industry found an alternative to message formats and during the dawn of the Internet a new transport format was invented - packets. This formed the foundation of what would become a separate data network.

Instead of being transmitted over a circuit-switched network, the digital information is packetized, and transmission occurs as IP packets over a packet-switched network. These packet-switched networks form the foundation of the [Voice Over IP](http://en.wikipedia.org/wiki/Voice_over_IP) (VOIP) technology we know today.

Now we live in a world of two networks; One circuit-switched and the other packet-switched. When those worlds interoperate, they do so using protocols that enable packet-switched digital data to communicated with circuit-switched digital data. Those protocols include, but are not limited to: H.264, V8, H.232, H.323, SIP, MGCP and others.

Currently H.323 is the most widely deployed VoIP call-control protocol. H.323, however, is not widely seen as a protocol that is robust enough for PSTN networks. For these networks, other protocols such as Media Gateway Control Protocol (MGCP) and Session Initiation Protocol (SIP) are being developed.


PHONE NUMBERS

Phone numbers in particular are fascinating. Phone numbers are simply different across the globe. To bring the point home, take a look at a few numbers across locales:

**USA (NANP): +1 (555) 555-5555**

**India: +91 22 555 5555**

**London: +44 20 5555 5555**

The [North American Numbering Plan](http://www.nanpa.com/) (NANP) is an integrated telephone numbering plan serving 20 North American countries that share its resources. These countries include the United States and its territories, Canada, Bermuda, Anguilla, Antigua & Barbuda, the Bahamas, Barbados, the British Virgin Islands, the Cayman Islands, Dominica, the Dominican Republic, Grenada, Jamaica, Montserrat, Saint Maarten, St. Kitts and Nevis, St. Lucia, St. Vincent and the Grenadines, Trinidad and Tobago, and Turks & Caicos.

Regulatory authorities in each participating country have plenary authority over numbering resources, but the participating countries share numbering resources cooperatively.

AT&T developed the North American Numbering Plan in 1947 to simplify and facilitate direct dialing of long distance calls. Implementation of the plan began in 1951.

The [International Telecommunications Union](http://www.itu.int/en/Pages/default.aspx) (ITU) assigned country code "1" to the NANP area. The NANP conforms with ITU Recommendation E.164, the international standard for telephone numbering plans.

NANP numbers are ten-digit numbers consisting of a three-digit Numbering Plan Area (NPA) code, commonly called an area code, followed by a seven-digit local number. The format is usually represented as:

+1 NXX-NXX-XXXX

where N is any digit from 2 through 9 and X is any digit from 0 through 9. Routing calls requires multiple switching offices. The phone number itself is a coded map for routing the call. 

In the NANP countries, for example, we have 10-digit phone numbers:
- The first three digits are the area code or national destination code (NDC), which helps route the call to the right regional switching station.

** The next three digits are the exchange, which represents the smallest amount of circuits that can be bundled on the same switch. In other words, when you make a call to another user in your same exchange - maybe a neighbor around the corner - the call doesn't have to be routed onto another switch.**

** The last four digits of the phone number represent the subscriber number, which is tied to your specific address and phone lines.**

Within a company or larger organization, each employee or department might have its own extension. Extensions from the main phone number are routed through something called a private branch exchange (PBX) that operates on the premises. To make an international call requires further instructions. 

The call needs to be routed through your long-distance phone carrier to another country's long-distance phone carrier. To signal such a switch, you have to dial two separate numbers, your country's exit code (or international access code) and the corresponding country code of the place you're calling.

Almost all [exit codes are either 00 or 011](http://electronics.howstuffworks.com/telephone-country-codes1.htm), although there are a few exceptions like Cuba (119) and Nigeria (009). Country codes are one - to three-digit prefixes that are assigned to specific countries or groups of countries. 

For example, the country code for the United States is 1, but the United States shares that country code with Canada and several smaller island nations like Jamaica, Puerto Rico and Guam.


###PBX

No doubt you've heard the term PBX before. A PBX or Private Branch Exchange is a small telephone switch - think of it as a mini exchange.  

Businesses install PBXs to reduce the number of phone lines they need to lease from the telephone company. Imagine that without a PBX, you would have to to rent one telephone line for every employee with a phone.

With a PBX system, you only need to rent as many lines from your telephone provider as the maximum number of staff making external calls at one time. In most businesses this is only about [10-12% of the workforce](http://www.techsoup.org/support/articles-and-how-tos/phone-systems-on-a-shoestring).

What you didn't know is before the [tangled mess of PBX](http://cypressnorth.com/technology/setting-up-a-small-office-or-home-office-voip-system-with-asterisk-pbx-part-1/)'s gone by:

![pstn-2](/images/pstn-6.jpg)

There were [human powered switchboard operators](http://www.ohmreunion.com/memorabilia/pbx.htm) in businesses, government and large commercial buildings:

![pstn-2](/images/pstn-7.jpg)


Of course, not even remotely as large as your local switchboard would be. Here there were usually anywhere from 2-4 people at most:

![pstn-2](/images/pstn-8.jpg)

In the PBX system, every telephone in a business location is wired to the PBX, using either standard cables or more recently Cat 5 ethernet cabling. When a member of staff picks up their phone and dials the outside access code (usually 9), the PBX connects that person to an outside line, and onto the PSTN.

PBX solutions themselves have gone from a consortium of wires and frames to a single commodity hardware or higher grade application running open source software that allows you to create a [virtual PBX](http://www.asterisk.org/).

Open source software like Asterisk is an example of this paradigm shift. With Asterisk you can create a PBX, an IVR system, a conference bridge and virtually any other communications app you can imagine. Asterisk was one of the first open source PBX software packages.

Asterisk supports a wide range of Voice over IP protocols, including the Session Initiation Protocol (SIP), the Media Gateway Control Protocol (MGCP), and H.323. Asterisk can interoperate with most SIP telephones, acting both as registrar and as a gateway between IP phones and the PSTN.


###PSTN AT RESPOKE

The PBX has gone from a tangled mess of wires to software running on commodity boxes to a [hosted PBX](http://www.digium.com/en/products/switchvox-cloud) in the cloud. The web was only the natural progression.

You can use Respoke to [make phone calls and receive phone calls](https://docs-int.respoke.io/tutorials/calling-to-and-from-a-phone.html) from phones on the PSTN as well as other Respoke client endpoints. It's easy...

{% highlight javascript %}
// here's the App ID value from the portal:
var appid = "DD90A374-0C06-456F-9D4F-E8038E6523D2";

// create a client object using the App ID value
var client = respoke.createClient({
    appId: appid,
    developmentMode: true
});

// listen for the 'connect' event
client.listen('connect', function () {
    console.log("Connected to Respoke!");
});

//Now all you have to do is make a call
client.startPhoneCall({
    number: "+15558675309"
});

//Attach listener to receive calls
client.listen('call', function (event) {
    if (event.call.fromType === 'did') {
        // We got a call from a phone number!
    }

    if (!event.call.caller) {
        event.call.answer();
    }
});
{% endhighlight %}

Using a combination of WebRTC media channel and good 'ol fashioned ingenuity, Respoke takes your IP based voice data and converts it into digital SIP data which can be consumed by regular phone devices.

If you're talking to someone on the web or VOIP device, your voice data stays on the packet-switched network - just like a regular VOIP call. If you're talking to someone on a cellphone carrier or landline, Respoke takes care of the details to communicate with that person's circuit-switched network.

Of course you can do a lot of other things with Respoke as well. Like video, voice and text communications. Now you have access to the PSTN network as well. Sky's the limit from here on out.