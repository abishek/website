---
title: Word Permutations
author: abishek
type: post
date: 2014-05-12T00:08:50+00:00
url: /word-permutations/
ct_tracks_last_updated:
  - default
categories:
  - Tech
tags:
  - python
  - tech

---
We were discussing something yesterday and it came up for us to arrive at all the possible words with at least 3 letters using the letters in the word &#8216;football&#8217;. We started out with a&nbsp; paper and pencil and came up with about 2 dozens when it struck me that I could do this with python.

The pseudo code in my mind was this:

1) generate all permutations/combinations of the letters in the word

2) check against a dictionary to see if what you generate is valid

3) uniquify

I have checked in my snippet in [github][1]. Feel free to point out the errors.

 [1]: https://github.com/abishek/python-snippets/blob/master/wordlist.py