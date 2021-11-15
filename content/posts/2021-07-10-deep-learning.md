---
title: Deep Learning
author: abishek
type: post
date: 2021-07-10T10:17:19+00:00
excerpt: I see a few paths for me, going forward. I try to articulate them. I also try to justify to myself why I like some of them better than the others.
url: /deep-learning/
ct_tracks_last_updated:
  - default
categories:
  - Life
  - Tech
tags:
  - build2learn
  - career
  - deep learning
  - machine learning
  - next steps
  - nlp

---
I&#8217;ll be 40 in a year or two. 

I distinctly remember feeling a stomach churn and completely unprepared when I turned 30. I had just finished my MS thesis and joined Atheros. I had a long way to go to have something I could call a career. It was very unsettling at that time. But then things happened and here I am, almost ten years later, still embarked on a journey to identify the problems I really want to solve.

In the last year, I started studying a whole bunch of things: cryptocurrency, blockchains, machine learning, natural language processing, NFTs, marketing, and project management. As I said, I am still unsure where I fit the best. I know I am best at solving problems. But at what level? And what problems do I find interesting? I managed to round them down to three main areas that I&#8217;ll try and focus on going forward: product management, marketing, and natural language processing. That&#8217;s a very oddly specific set of things to do. Let me explain,

I love writing. And I figured I have a knack for telling some types of stories. I started putting this to use at my work early this year. While I wouldn&#8217;t claim a lot of success, I know I enjoy the process. Besides my intuitive plan for content marketing was spot on comparing with a plan that the social media and content marketing consultant we hired for this. That was a big shot in the arm. So I feel there is something there that I should nurture and take forward.

Product management is something I do day in/day out at work. I do it to push back and shape the product to ensure it aligns with the stories I write on the blog. It is a constant fight with the rest of the team to shape the product in a certain direction. There are places I lose and compromise and there are places I win and have my way. Since I lead the development efforts anyway, it all boils down to my effort either way. Along the way, though, I figured I enjoy this activity as much or sometimes even more than writing actual code. I am far from being a product manager, I think. I know I am not good at project management: I am quite terrible at estimation and planning, even worse at keeping a team functioning. I am, though, very good at hiring a team that will deliver because I assess really well who I want to work with 😉

Before I explain the natural language processing part, let me explain why the others got dropped out. Crypto, NFTs, and blockchains are all branches of the same medium. But I couldn&#8217;t wrap my head around the entire concept. I can, for what it is worth, explain a blockchain to you. But I cannot grasp, at the very least, why anyone needs one. Yes, I understand the power of decentralization, yada yada. I am unsure I get the idea in its full glory. And I know I cannot sell something I either don&#8217;t understand or do not believe in. For what its worth, I am yet to buy a single NFT or DeFi coin inspite of creating a couple of wallets and following them quite regularly. Someday I am sure I&#8217;ll understand what this movement is really all about. But until then, this is really not my cup of tea.

I was initially drawn to Natural Language Processing about 5 years back. I bugged my mentor [Dr. Ramaseshan][1] to initiate me into this field. He spent quite some time and taught me the basics &#8212; enough to get me started. Then he released the [course he teaches as a MOOC on the nptel platform][2]. It&#8217;s a super elaborate series on natural language processing. It has tonnes of information &#8212; so much that, after two iterations, I still have many lectures I don&#8217;t fully grasp and keep going back every now and then. Then I did a whole bunch of free courses on multiple platforms. Then I figured I missed a few things: I missed some discipline to actually practice this skill; I missed a few basics around machine learning; more importantly, I missed being able to get started quickly. In most courses, outside the sample dataset, very little actually works if you tried to collect the data. It always turned out a nightmare when I tried repeating the course stuff with other data. For example, if we took text cleanup, courses give you a nice set of regexes to get you through. But when you collect your own data, you have a lot more decisions to make &#8211; what about numbers, what about emojis, punctuations like exclamation, names, and more commonly hyphenated words!

I signed up and completed [Andrew Ng&#8217;s Machine Learning][3] course. A pretty fab course that teaches you the fundamentals very well. But then I really got stuck taking it forward. For instance, I couldn&#8217;t &#8212; without a lot of effort &#8212; map the linear regression concepts from the course to, say, scikit-learn. When you google, you get tonnes of references using pytorch or tensor flow. Beyond the fact that one is Google-funded and the other a Facebook-funded library, I have no idea what they can do for me. Or how they work (or how to simply start using them). The roadblock is worse if you consider the fact that I cannot commit to something until I get a basic grasp of what it is &#8212; the same reason as to why I am staying away from anything blockchain.

Early this year, again, I joined [a tech forum][4] that helps you learn (as a community) to see if I have enough elasticity to learn something. It is run by [Dorai Thodla][5], someone I regularly follow for good resources on most things tech. Besides staying in a community of like-minded folks and some mentorship should do me some good. Right? Mostly. I found a good project to work on and a couple of people agreed to mentor as well. Then I got stuck in the same loop &#8212; how do I get started when the problem looks like a mountain!? I got some pointers. But here is the thing: a whole lot of people are super comfortable working with completely unfamiliar stuff. I am myself too, except I cannot work with complete unfamiliarity. I need to go some way &#8211; 20-30% understanding is enough for me to get started. But even getting there with deep learning, machine learning or NLP seems like a tough nut to crack. The problem is slightly different. I can hold an intelligent conversation on each of these topics, but I cannot implement a simple model and teach it to do something. And that&#8217;s the roadblock that&#8217;s really difficult at the moment.

As part of the [build2learn project][6], I started reading some good articles that used deep learning to do some niche NLP stuff. There is a related paper as well. It put me in my old MS research ambiance and I really am able to read through stuff and understand what the authors are talking about. I am even able to park aside some concepts as black boxes that I&#8217;ll eventually understand fully. In one such article, I got introduced to [fastai][7]. I started doing the MOOC there alongside reading [Jeremy&#8217;s book][8] on the same subject. I cannot begin to thank them for making this available. It gets you started in such a simple manner and helps you keep the black boxes as is while you work towards an understanding starting from the periphery. I&#8217;ve done just two lectures and two chapters of the book and today I managed to train a deep learning model and get it to categorize images as &#8216;squares&#8217;, &#8216;triangles&#8217;, or &#8216;circles&#8217;. And it works quite well too. I wrote a quick [fastapi][9] app to upload an image and predict the geometry based on the above. No, it is not published on the internet yet and I&#8217;ll make my code available on GitHub really soon. The best part is that I could pick up a dataset on [kaggle][10] to help train my model. I used the training code, as is and as a black box, from the fastai course. It does feel good to have some results to gloat over while you are still very novice at the game.

All that said, the reason I think I am attracted to machine learning and natural language processing over, say, cryptos is that this appeals to my math inclination better than the other. I was never fascinated with cryptography. It was just too complex for my liking. In spite of not being too good at statistics, its a subject I have always revisited every few years. If only had I known that the lone chapter in high school math on &#8220;curve-fitting&#8221; would be a fork in my path some 20 years later, I would have listened to the teacher with a little more interest and attention. Hey, I remember the terms at the least and I don&#8217;t feel intimidated by what I see 🙂

_PS: the topic is a pun on the phrase &#8220;deep learning&#8221; and has almost nothing to do with deep learning techniques that are so ubiquitous today. I can hear your knives, but let us choose peace. I&#8217;ll buy you coffee when this is all over._

 [1]: https://twitter.com/ramaseshan
 [2]: https://nptel.ac.in/courses/106/106/106106211/
 [3]: https://www.coursera.org/learn/machine-learning
 [4]: http://www.build2learn.in
 [5]: https://twitter.com/dorait
 [6]: https://github.com/abishek/code-finder/wiki
 [7]: https://www.fast.ai
 [8]: https://www.amazon.sg/Deep-Learning-Coders-fastai-PyTorch/dp/1492045527/ref=sr_1_1?dchild=1&keywords=deep+learning+for+coders&qid=1625909540&sr=8-1
 [9]: https://fastapi.tiangolo.com
 [10]: https://www.kaggle.com/cactus3/basicshapes