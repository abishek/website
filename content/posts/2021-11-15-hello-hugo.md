---
title: Move to Hugo
author: abishek
type: post
date: 2021-11-15T15:15:06+08:00
excerpt: Wordpress has become unmanageable for my personal blog. I decided to move to something that is inline with the nerd that I am. Ideally, I should picked a static site generator based on python, but hugo is pretty popular and honestly, I like the theme options. Read on, to know more.
url: /hello-hugo/
featured_image:
    'https://images.unsplash.com/photo-1602140993159-0667b11ec4a1?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2831&q=80'
ct_tracks_last_updated:
  - default
categories:
  - Tech
tags:
  - thoughts
  - life
  - wordpress
  - hugo
---
## Hello Hugo!

Today I moved my blog to [hugo][1]. Frankly it doesn't make intuitive sense to run a blog on a static site generator. But when I think about it again, my blog is my expression of ideas. I rarely engage on the comments section. And the best way to let me know your thoughts is still to tweet at me. Given these, it makes sufficient sense to run the blog as a static site. And the site is now stupidly simple. I found a fabulous theme, and am editing the site using markdown on my emacs. This is actually faster than editing on wordpress editor :-)

### Why Hugo?

I considered a few before landing on hugo. First choice, of course, was [hyde][2] because it is written in python. But I didn't find much info on themes. Besides, I already had a tonne of content on wordpress and am not about to write my own exporter. There were a few articles, but it didn't seem like the most popular direction. Second choice was [jekyll][3]. Jekyll is probably the grandparent in this static site generation deal. There are tonnes of examples and a lot of people have had great success. But Jekyll is in Ruby. While I don't have anything for or against ruby, I don't quite get the language. Then I saw some links talking about hugo in the results. Now, I have a thing for [go][4]. Its the new C, in my head and I loved C. And easily go is likely to have the fastest performance over ruby or python. And in my case, this task should be the easiest with the least load on my machine. And frankly, I loved this particular theme that am running now. So, while its not entirely rational, I picked hugo for this job. I should say, the initial impression is very good. It took me all of 30 mins to migrate from wordpress, setup the theme and create a build. I haven't setup a pipeline to autopublish yet, but this is already a very good start.

### Why not Wordpress?
I recently wrote about how [my wordpress got hacked][5] and really ruined my weekend. It repeated again last weekend. I just pulled down my website to think this over. On the one side, my website has nothing of value to steal from. It doesn't have the kind of traffic to be interesting for anyone. The only reason it got hacked is that the wordpress default security model seems terribly flawed. It sets you up for failure, if you stuck to the defaults. And there are half a dozen paid plugins that can keep you safe. I spent some time reading up on a bunch of blogs on how to secure the worpress site. After a couple of posts, it is very clear that wordpress is probably not very secure. So use a WAF or use a firewall plugin, malware scanner and so on. In some sense, it is understandable. If you want to keep it user upgradable at runtime, then you do open yourself up for some level of threats.

While playing catchup on the second weekend to secure my site was fun, I don't want to do this for my personal site that's just my thought dump. I'd just do this over google docs and share it. So I am doing the next best thing: static site generation.

## Next Steps

I need to setup a deploy pipeline. There are a lot of good recommendations in hugo documentation. I am hosting this on S3 + CDN with hugo CLI managing the deploy. The files themselves are checked into a private repo on github. I need to hook up my emacs or git hooks to automate the build and deploy. I'll probably share my snippets once they start working properly.

[1]: https://gohugo.io
[2]: https://hyde.github.io
[3]: https://jekyllrb.com
[4]: https://golang.org
[5]: /wordpress-compromised/
