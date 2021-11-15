---
title: Redeeming the old MBA2,1
author: abishek
type: post
date: 2017-05-07T04:45:31+00:00
url: /redeeming-the-old-mba21/
medium_post:
  - 'O:11:"Medium_Post":11:{s:16:"author_image_url";s:69:"https://cdn-images-1.medium.com/fit/c/200/200/0*LfHC1cgdpbsibDbt.jpeg";s:10:"author_url";s:31:"https://medium.com/@abishekgoda";s:11:"byline_name";N;s:12:"byline_email";N;s:10:"cross_link";s:3:"yes";s:2:"id";s:12:"d1e5f50f0836";s:21:"follower_notification";s:3:"yes";s:7:"license";s:19:"all-rights-reserved";s:14:"publication_id";s:2:"-1";s:6:"status";s:8:"unlisted";s:3:"url";s:69:"https://medium.com/@abishekgoda/redeeming-the-old-mba2-1-d1e5f50f0836";}'
categories:
  - Tech
tags:
  - battery
  - broadcom
  - kali
  - linux
  - macbookair
  - nvram
  - smc
  - wireless
  - woes

---
We have this mid 2009 model Macbook Air (MacbookAir2,1) that has been idle for quite a while. I made the mistake of upgrading it to El Capitan a couple of years back which made it a functional brick. It would boot, but would take a tonne of time doing that. And then anything you click would take 5-10 minutes to happen. I tried all the usual stuff. I threw the DVDs that came with the device, so I can&#8217;t so much as roll it back to its good self. I tried finding snow leopard or lion online, but mostly you get fake downloads for 3G that either don&#8217;t finish downloading or are useless post downloading! Trust me, I wasted quite some bandwidth doing just that. This was in late 2015. I briefly tried to get debian working on it. But I didn&#8217;t have too much patience to figure out the EFI stuff so everytime I reset my NVRAM or SMC, I&#8217;d promptly be back in an unusable MAC that would boot El Capitan and have no disk space. Then I destroyed all debian on that machine and reset it to stay El Capitan, put the device in the attic and tried to believe it doesn&#8217;t exist any more.

This was a perfect way to use that machine, until recently. We had to shuffle around things and I saw this MBA lying around doing nothing. I have half a dozen functional machines (including a RPi and a BBB), but hey, another X64 machine should be interesting. So I set out to get debian working all over again. I downloaded a bunch of CD1 ISOs, burnt them on a few CDs, loaned an external optical drive from my sister and earmarked this weekend to get this booting. After reading a lot about this combination, I figured a few people managed to got this MBA2,1 working with debian and they used a library call rEFIt to make this happen. The catch is, rEFIt is no longer maintained. So I have to use rEFInd. I would assume they are similar but for whatever reason, it just wouldn&#8217;t work on my machine.  After restarting the mac about 6-7 times, I figured this isn&#8217;t going anywhere. Time to look for alternatives.

That&#8217;s when I landed on Kali linux page which promised to work with EFI devices from the word &#8220;go&#8221;. Isn&#8217;t that cool. Besides, I recently finished two seasons of Mr Robot on Prime. They kept referring to Kali Linux everywhere. Cool, let me try to get this one then: If it works with EFI,  I don&#8217;t have to trouble myself with the EFI details and hey, if its good for hackers, it could be good for me. I am not sec analyst, and I heard pentesting only in Mr Robot, so what can go wrong? Turns out, not much. I had to go through a bunch of NVRAM resets ( I think the MBA battery is dying ) but Kali just installed smooth. And it boots every other time. When it does fail, all I need to do is an NVRAM reset. This time I was bold enough to remove all the MAC partitions, so NVRAM reset doesn&#8217;t get me back to a dysfunctional El Capitan. And I took my chance install grub on /dev/sda. It takes a little extra while to boot to grub, but who cares. At least the machine is functional.

Well, not exactly functional. I need to use the ethernet cable to keep it functional at the moment. Its not any secret that brcm doesn&#8217;t way very well with linux. It used to be that way when I was actively working with linux installations. Since this device is from the same era, I didn&#8217;t expect it to just work. Besides, AAPL does a lot of stuff that makes the device pathetic from a non OSX point of view. So I expect to need a bunch more weekends to ensure that the wlan can work. Until such a time, I guess Kali on my MBA2,1 is not such a bad idea at all. It is fast, the browser loads. And there is a functional terminal and comes pre-installed with python3. That&#8217;s about everything I care for on that box 🙂

Perhaps, once I get the wlan to work, I might try to learn one or more of those hundred odd tools that comes installed with the distro. At the moment, I don&#8217;t want to do anything stupid and get myself into a situtation.

> A big lesson learnt is this: don&#8217;t buy a mac you cannot expand the RAM for. We picked this MBA out of sheer enamour. I also picked a unibody white Macbook around the same time as the MBA. That was still an expandable device and is able to run El Capitan (after I expanded the RAM). That device is another story for another day.