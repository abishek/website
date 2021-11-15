---
title: Note Taking
author: abishek
type: post
date: 2020-11-22T13:20:10+00:00
url: /note-taking/
ct_tracks_last_updated:
  - default
categories:
  - Life
tags:
  - discipline
  - notes
  - tools

---
I am terrible at taking notes. I guess I never learnt the skill properly. Until two days back, I had 6 note taking apps on my device, each having a copy of all the projects I am working on, status, todo list (unchecked), and thoughts and action items for each. Each of these has some overlap, so they aren&#8217;t imported around. I spent last morning cleaning up every one of them, copying them to two main tools and deleting every thing else. The two tools are &#8211; org-mode on my emacs and another app called Agenda.

My emacs is always open. So org-mode makes it easy to capture notes with. But it doesn&#8217;t look all the good. Well, visually pleasing should never be the reason to do anything important, right? You see the problem &#8211; I seem to need the tool to be inviting enough for me to write notes into. That&#8217;s why there is Agenda. Its a visually pleasing tool. It&#8217;s not without its problems though. Here is what I am going to write about: My problem with org-mode; My problem with Agenda; Trying to form a f*king discipline and pick a default tool; The real reason I believe I am bad at all this. So, here goes.

## My problem with org-mode

[Org-mode][1] is perhaps the most talked-about note-taking tool. It is actually incredible in what you can do with simple flat text files. I think the simplicity in its design is what really stands out to me &#8211; being the dev that I am. But I just happen to like some visual aesthetic. Mind you, org-mode is infinitely customisable. I am sure it is possible to make it look like Agenda. But as much as I know what I want, I can&#8217;t really set it up that way. It takes time and even in web development that feeds me, CSS is what I hate the most.

But the real problem I have with org-mode is not related to org-mode at all. I code Django for the most part. Django syntax linting is not the best in emacs. Or at least, I couldn&#8217;t get it to work reliably. So I was forced to move to a different environment. Besides, I use angular for all frontend (I can hear the why, but I just don&#8217;t want to learn another framework). Emacs support for editing angular isn&#8217;t really there. Again, I shouldn&#8217;t blame emacs. The fact of it is that I am unable to set it up the way I want. My benchmark for angular is VSCode. So setting up emacs to do for angular what VSCode does is a bit far fetched for my expertise with elisp code. So I moved to PyCharm.

It is extremely unlike me to even use a Java-based tool. It&#8217;s just a mental prejudice against Java which is inexplicable. I guess that qualifies me as a racist. But PyCharm delivers. Its linting for my Django work is pretty good and it does a slightly better job than even VSCode for angular. There are a few pain points, but my overall developer time has improved a lot since investing in PyCharm. It&#8217;s entirely possible that I find It good because I paid for it. But who cares.

The most interesting use case for org-mode is to capture thoughts and fixes that occur in the middle of a coding session. You have this brilliant org-capture that captures the note without ever moving out of the current buffer and bookmarks the exact line of code for the note. This is simply amazing, especially for people like me. But moving out of emacs kinda makes this not-so-straightforward. 

## My problem with Agenda

[Agenda][2] is a beautiful tool. Its best for capturing meeting notes and following up. But I use it primarily to capture long-form thoughts and ideas. To effectively use it for meeting notes, I might need to purchase a license, but I hate meetings altogether. So it serves my purpose reasonably.

Most of the reason I need notes is because I am trying to understand some math problem, or construct a math equation or the like. Agenda does not have a math-mode built into it. So I can&#8217;t type any equations at all. So I maintain them in my physical note book. So a big part of what I am trying to capture doesn&#8217;t go into this tool. But for everything else, this one is really there. 

The other big issue I have is this &#8211; Note needs a title and that&#8217;s just a tonne of cognitive load for me. I want to capture something, don&#8217;t ask me up front to give it a name!

## Forming a Discipline

I tried multiple tools for many years. I usually have two physical notebooks which are my last fallback and usually the most utilized. I tried One Note for a while. I basically love this tool for the simple reason that it doesn&#8217;t even enforce a spatial hierarchy on the note itself. Just click someplace and start writing. The only other tool that does this is [milanote][3] &#8211; but that&#8217;s for creatives. The problem I face with One Note is simple &#8211; I have to decide what notebook my current thought goes into. 

The other untold fact here is that I am just as terrible at organizing stuff. My digital footprint is as though someone puked into the downloads and documents folder. When I set up the system, I have created a lot of intuitive folders. After 3 years, most of them are empty and every damn thing is inside either the downloads folder or the documents folder. The fact that searching for files is efficient certainly doesn&#8217;t help my handicap. So choosing the folder to put the note in is a decision that paralyses me.

I tried Evernote. Same thing happened. And then it became so heavy that I got rid of the app.

I tried [bear][4] notes. Another visually beautiful tool. The biggest advantage was it used standard markdown. But the downside was it wouldn&#8217;t sync to my phone unless I pay for it. Well, not yet. Agenda is a little more beautiful and syncs to my phone. But now that I look at it again, maybe its better than agenda in some ways?

Then I tried [Notion][5]. This was the most advertised and probably the app that took everyone by storm. For me, though, it fell flat. I just can&#8217;t seem to even get started. Right off the bat, I need to make choices and boy there are so many to choose from. Its built for people who are organized. It gives such people a big shot in the arm. For chaotic monkeys like myself, its just a tool to shoot myself with. I didn&#8217;t do much with notion, so it was the easiest to delete.

Recently [Roam][6] became the goto note of choice. Especially with all the Zetteltasken related theories. I figured two things reading about this.

  1. I am terrible at taking notes. [Zetteltasken][7] is how you should probably take notes. I can&#8217;t even imagine doing something like that. It takes discipline.
  2. Roam works if you take a tonne of notes. And these notes are all over the place. Somewhat ideal for what I am facing. But I&#8217;ll need to pay for it. 10 apps have failed me so far. I ain&#8217;t gonna pay for this one yet.

So I found [obsidian][8]. Its just like Roam but gets you started for free. Except after a month of usage, I found that I didn&#8217;t write all that much. And most of what I wrote didn&#8217;t yet connect back to the other notes. So there were no backlinks or graphs to from or navigate. It look pretty darned depressing. So I copied over everything to org-mode and got rid of it.

Lastly, Apple Notes. It&#8217;s right there and does most of what the other tools do. My biggest problem, here again, is where does the note go. But if you looked at my notes app, you&#8217;d see how chaotic it is. But I keep all the critical stuff here &#8211; firstly because it&#8217;s available on the device and secondly it gets backed up to icloud. And that stuff is pretty badly organized too. It doesn&#8217;t support math mode either. The solution I am considering to try is to pick a basic iPad and use it to capture handwritten notes &#8211; a replacement for my physical notebooks. That way, I don&#8217;t need to worry about math mode per se. Besides, handwriting recognition of my scribbles works on my son&#8217;s iPad. So that seems like a good thing to do. Frankly, though, I don&#8217;t want to spend $15 on an app that promises more. This one offsets me by $500!

## The real problem

Note taking works perfectly for my wife. She&#8217;s a One Note power user. And I feel like I am entering a shrine when I look at her notes. But she&#8217;s just wired better for this. And she takes extensive notes. I, on the other hand, cannot decide what to note down. I usually note down somewhat inconsequential stuff. When I analysed this pattern yesterday, I think I figured out the problem.

  1. I tend to remember most things I come across. Clutter and abuse of memory, but that&#8217;s just how I am. I can, almost always, narrate extensive details of a scene that happened a whole bunch of years back. And this applies to stuff I read, stuff I listen to and stuff I watch. I just seem to know what to lookup when I need it. Now most people will call this a blessing. To me, though, this means I cannot decide what to note down. So I note down stuff that am ok to forget: the inconsequential stuff! This will become a problem as I go into my 40s and 50s when I start hitting the limits of my memory. Or perhaps, I&#8217;ll learn to write good notes when my memory starts failing me &#8211; though, I am not sure I can learn anything at that point..
  2. I can&#8217;t use anything that forces me into a structure. If I have to pick a folder or a hierarchy, I decide its easier to just remember the damn thing and move on. Or I just write it into my physical notebook and move on. That&#8217;s why org-mode was perfect. I didn&#8217;t enforce much. I usually picked a project and captured the note into that project&#8217;s file. Everything about the project goes into the same file. The file itself is terribly structured so most people will judge me if I showed them my notes! On the other hand, I am pretty lazy. Unless am thinking and writing something &#8211; which usually is long form, like this post &#8211; I hate to have to type it out. I would really like to dictate that stuff. But dictation integration is unknown frontier for org-mode. Dictating to Siri will create a new note everytime increasing my headaches.

So, what choice do I have? One thing am willing to try is attend a proper 4-6 week course on note taking. Note taking for studying, for meetings, for blogging, for capturing code TODO and everything else in between. If I learn this one skill and replace all my physical notebooks into one tool, then I guess am ready to do better things.

 [1]: https://orgmode.org
 [2]: https://www.agenda.com
 [3]: https://milanote.com
 [4]: https://bear.app
 [5]: https://www.notion.so
 [6]: https://roamresearch.com
 [7]: https://en.wikipedia.org/wiki/Zettelkasten
 [8]: https://obsidian.md