---
title: For the love of pubsub
author: abishek
type: post
date: 2015-09-19T05:23:03+00:00
url: /pubsub-love/
categories:
  - Tech
tags:
  - c
  - django
  - GAE
  - humor
  - idea
  - learning
  - motivation
  - mqtt
  - PAM
  - php
  - programming
  - pubsub
  - python
  - redis
  - tech
  - thoughts
  - web

---
I have fancied publish-subscribe middleware(pubsub) architectures for quite sometime. When we were still very new in CTS, I came up with a wild suggestion to try this for getting a data dump from a legacy system into our moodle instance. I was quite clueless about what this would entail in terms of development effort, but I could create a PoC setup within a few days which made me quite confident of being able to pull this off.

In fact, I had enough spare time in hand to actually implement a PHP module that would talk to an IBM MQTT server over pubsub protocol. I should have written about this experience because it was one of those times where I really perfected my mallocs and frees! The other instance was when I wrote a PAM module for authenticating against AD. Now there are many supported libraries to do this, but when I started out there wasn&#8217;t much. OpenSUSE had some customizations of the LDAP login module to support AD. Most of us in the team were pro-Fedora and hated OpenSUSE because we thought it made Linux look like Windows. In fact, I was pro-Debian and hated most rpm distributions. I still do in spite of the fact that I learned to use a Linux machine on a RedHat distribution! And I still hate Ubuntu for similar reasons. _Too many digressions!_

Yeah, PHP was quite pedagogic about my code. I abandoned the module because I was not clear about the licensing terms for using the C API from IBM. Perhaps the code is still lying around in one of those machines we used back in the day. And I didn&#8217;t want to bug my manager&#8217;s time to pursue the required clarifications. I am not even sure he knows about this.

So, yes, I fancied pubsub architectures ever since. If I had a chance, I might have used it in my MS thesis as well. Then I moved into Semicon jobs and haven&#8217;t really had a chance or reason to get back to this topic. My next fascination is the Arduino. About a year or two back, a bunch of people came up with mqtt implementations for Arduino. I guess it is pitted to be one of the contenders for IoT implementations. This rekindled my interest in the topic and I started reading up again. Toying around with the libraries isn&#8217;t going very far. I needed a concrete premise to play around with.

I am good at web development. I prefer to use python and am reasonably stuck with django as the framework of choice &#8211; even if all I want is a todo list. I am no django-expert, but I can swim around with reasonable ease. This also helps because I still haven&#8217;t gotten my head around any sort of nosql concepts. I briefly dabbled with the idea on GAE and pissed off a mentor! So I pretty much stick to mysql/sqlite with django which suits the biggest of what I have ever done in this platform. Nope, not a todo list, a proper report generation tool for a friend. _Wait, that reminds me, I should see if I can get some inputs from him for my portfolio!_

Middleware is usually a server stack component. Which means I need to figure out a way for apache to talk to some mqtt server. There are a bunch of ideas around this. But I have come too far without much learning in this direction and I don&#8217;t know if I have enough enthusiasm to learn everything I missed along the way. So I shifted gears and started looking for some options that would ease my trouble. That is how I hit upon websockets. I have read about websockets a long while back. But I don&#8217;t think I ever gave it much thought. If my memory serves it right, opera was one of the first browsers to do something with this. I think now many modern browsers have some level of support. And given my aversion to javascript &#8211; another concept that is extremely elusive to me &#8211; ajax was not the best alternative. So I thought I&#8217;ll see what websockets can do for me.

More searching lead me to redis. I don&#8217;t know enough to talk about redis, but somewhere redis seems like the perfect solution &#8211; _especially because someone figured out how to use python with_ redis_,_ django_, and websockets and not die halfway wondering what we started out to do. Oh! I have a premise as well._

I&#8217;ll abruptly stop this post here. I&#8217;ll continue talking about this experiment and my learnings in a future post. Of course, I&#8217;ll talk about the premise as well there.