---
title: Yet Another Yoga Timer
author: abishek
type: post
date: 2015-06-10T02:21:36+00:00
url: /yet-another-yoga-timer/
categories:
  - Idea
tags:
  - app
  - exercise
  - idea
  - ios
  - iphone
  - startup
  - tech
  - timer
  - yoga

---
I wrote about needing a good exercise timer [here][1]. I am using the yoga timer app that I downloaded and am reasonably happy with it. I hate quite a few things about that app. I could give feedback and make it better, but the app has a paid version. So chances are the paid version has these fixed already. Besides, it doesn&#8217;t do many things it claims to. So am quite unhappy with it.

I am not willing to spend more time hunting for another app. So I made the  decision to write my own. Of course, I know that costs me USD99 to do this. But heck, I&#8217;ll do it now. I want to build an app that does exactly what I want it to do. Nothing less, nothing more.

For the initial prototype, I plan to do the following:

  * Voice commands to start and stop the timer
  * Audio feedback on timer start and expire
  * No configurability &#8211; When timer starts, it expires after 30s
  * Of course, there will be a way to touch the screen to start and stop the timer as needed.

The second version &#8211; assuming the first one works on the phone &#8211; would have the following additional features

  * Basic configuration &#8211; have multiple timers of different intervals. Limit to 10 timers at max. I don&#8217;t want to write super general code either.
  * Share configurations &#8211; import and export json/xmls
  * Logs stored in local datastore or icloud that can then be used to analyze how we are doing on time. This part is more for analysis and collection.

That&#8217;s about it. No big deal. Only two versions. Only three features per version. Hopefully bug free and simple to use. And hopefully I can afford keeping it free.

 [1]: http://www.rohabini.com/abishek/excercise-timer/