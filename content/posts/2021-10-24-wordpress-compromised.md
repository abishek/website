---
title: WordPress Compromised
author: abishek
type: post
date: 2021-10-24T06:17:38+00:00
excerpt: My Wordpress instance was compromised recently. My learnings from this failure, and some reflections.
url: /wordpress-compromised/
featured_image: 'https://images.unsplash.com/photo-1610337673044-720471f83677?ixid=MnwyMTYxMTd8MHwxfGFsbHx8fHx8fHx8fDE2MzQ5ODA2Nzg&ixlib=rb-1.2.1&fm=jpg&q=85&fit=crop&w=2560&h=1924'
ct_tracks_last_updated:
  - default
categories:
  - Tech
tags:
  - security
  - tech
  - thoughts
  - wordpress

---
I, accidentally, noticed that my WordPress instance was compromised. Of course, I would be the person to blame for this. It&#8217;s not a commercial thing, so I don&#8217;t nearly spend enough time looking under the hood. This cost me a couple of hours yesterday fixing and cleaning up the mess. I&#8217;ve taken some precautions to ensure I won&#8217;t need to look under the hood too frequently but also ensure I don&#8217;t sponsor some botnet or click-fraud elsewhere on the tubes.

I host my instance on my own EC2 instance. It is not that I don&#8217;t want to pay godaddy or any of the other hosting providers out there. I was anyway paying Amazon for running some cloud machines to support my hobby. Repurposing them to host a WordPress site didn&#8217;t sound like a difficult thing to do. Except, I thought wrong. Installing, setting up, importing and presenting a WordPress site is definitely amongst the easiest things to do. If you are familiar with the stuff, it takes about 30 mins to be up and running &#8211; all the way from launching a VM to connecting up the domain. But the real mistake is thinking it ends there. WordPress is so popular, that it is a target for all kinds of hackers. I think the big ones won&#8217;t bother, but all newbies learning their trade will probably start here. And we generally make easy targets. Let me explain.

### WordPress is a target

Have you seen the number of times WordPress core gets updated? As someone who manages a few WordPress instances (personally and at work), it is one of those systems that seem to have an update every day. Minimally, there will be a plugin update every day. It is one thing to have that many updates when I run an application &#8211; say woo-commerce &#8211; on top of my WordPress. Applications evolve and maybe they just evolve faster in this case. But I use the core and some basic plugins to support blogging. That&#8217;s about everything I need it to do. In fact, blogging is 101 for software development. It mustn&#8217;t be any effort to maintain a blogging software because this stuff should have been stabilised like a decade ago, right? Turns out, it isn&#8217;t like that.

So, just the number of update you see on WordPress core is an indication of how targeted the platform is. WordPress does a fabulous job at many things, so for a commercial installation, spending the effort in securing it is probably worth it. For muggles who just want to blog, this whole security updates is a nightmare not worth having to deal with. That said, I don&#8217;t see much other options unless am willing to just pay up $5 to WordPress to host my blog. I currently have it virtually free and maybe I just have to move to keep this up.

### My issues with WordPress

I have had the (mis)fortune of looking under the hood of WordPress code multiple times. I&#8217;ve even had to meddle with the database a couple of times ad have had my share of disasters. I, frankly, hate the way the code is written. Maybe that&#8217;s what makes is so scalable, but I just feel they abuse the built-in serialisation from PHP. I tend to abuse JSON the same way, so maybe I need to learn to sympathise with their decision. My biggest gripe is how you cannot just edit the database to fix something quickly. For any database driven application, there should be a class of things you can just fix by editing the database? Perhaps, am not the right kind of user that WordPress is looking to attract and retain.

But the issues go beyond their architecture. I&#8217;ve done software development long enough to ignore a working code&#8217;s choices. I&#8217;ll never deny what WordPress has achieved and I do have huge respect for that. I just don&#8217;t think its cloud ready. Let me explain.

I host WordPress on EC2. One of the primary tenets of doing anything on EC2 is to assume that the instance will get terminated and re-spawn at random. I&#8217;ve had this happen to me a couple of times. This is part of the understanding of running on the cloud. This also means, I cannot have the files for WordPress on the instance. In this case, I&#8217;ll need to create AMIs with the WordPress code and spin up a machine with the AMI to ensure I can have the same codebase even upon re-spawn. The only way this can happen is, if I figure out a WordPress update event and have my EC2 build a machine image of itself upon successful update and update the auto launch script to use the latest image. Its already quite complicated for a hobby setup.

So what I do is to run the file system on a EBS. For a hobby machine, this is a good workaround. Because I really don&#8217;t need it to run multiple availability zones or regions. On a work setup, I cannot do this because I need it minimally to work across availability zones. So I use EFS there, instead. But QoS of EFS and EBS aren&#8217;t really the same. Plugin updates tend to timeout a lot and am sure something similar happens with WordPress core updates as well. And WordPress is not really suited to be run as a docker instance for the exact same reasons &#8211; there is no way to ensure the core and plugins stay updated. If they have a release cycle and if the security issues aren&#8217;t that big between the releases, any of these options are good. But for their current frequency of updates, this is simply not sustainable unless you have a dedicated admin managing this stuff.

Lastly, the main reason my instance was compromised is almost very very stupid. WordPress has a flag to enable updates &#8211; a boolean flag, configured in code! And it defaults to false! I mean what kind of rationale allows for that choice is really beyond me. And I didn&#8217;t know about this flag until recently. I enabled it and I hope it will take care of the security problems going forward. But this choice is simply unacceptable. Imagine all those people who have no idea about this flag. The setup is so simple these days, any newb coder will just get started with a custom instance. But if you don&#8217;t update regularly, maybe you are just a part of a much larger botnet that you don&#8217;t even know exists.

### This should be simple, right?

Blogging is increasingly becoming front and centre for most businesses. And WordPress is really the tool of choice for most such businesses. It is safe to say that unless you have a dedicated IT team that manages the updates and infra, it is better to just pay and run the site on WordPress.com. Maybe this should change?