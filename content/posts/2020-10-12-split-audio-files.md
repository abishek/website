---
title: Split Audio Files
author: abishek
type: post
date: 2020-10-12T08:59:43+00:00
excerpt: pydub is an excellent library for manipulating audio files. Especially when you have ffmpeg installed!
url: /split-audio-files/
ct_tracks_last_updated:
  - default
categories:
  - Tech
tags:
  - audio
  - automation
  - editing
  - python

---
So we had to transcribe a bunch of interviews we did earlier. One of the sessions was a good 45 minute long and had a tonne of details. It&#8217;s quite difficult to manually transcribe this. But hey, we gotta do this. And then we have to do a bunch more later. The wife was in charge of doing this and she was trying to do manually. Then she had a &#8220;eureka&#8221; moment and tried to use One Note&#8217;s speech-to-text function. But there were tonnes of limitations &#8211; the laptop doesn&#8217;t hear itself and the phone seems to freeze for a long audio block. 

I thought to myself &#8211; I study so much about ML and NLP in all my free time and here I am not even wondering how best to solve this problem. So, like the good dev that I am, I googled for solutions. Bingo! [Office 365 does it for us][1]. And it&#8217;s apparently quite good and comes with our subscription. So I pointed her to the right menu items and said &#8211; &#8220;Here, this should save you time and effort.&#8221;

If only life were that simple. Office 365 decides that, after 2o minutes of transcribing, it is done. And who is to contest this? So she&#8217;s back to me &#8211; dude, this thing threw up after 20 minutes. What else can we do? Simple &#8211; split the file into a few minute chunks each and that should work. Audacity is your friend. So she goes with that. Only, the file we have is an m4a file and Audacity needs another half a dozen libraries to get started. Well, frankly, at this point neither of us have the patience. It seems like transcribing it manually would be faster. So I take the file from her and start to download audacity on my mac. Well, *nixes sure do behave differently. Besides, &#8220;[FFmpeg][2]&#8221; is the master of all decoders right?

But then maybe there is a better way? So I searched google for audio libraries for python. And there really is one &#8211; [pydub][3]. And they have a brilliant set of examples to do just my job. Cool, innit? Here is the final code that got me running in a few minutes:

<div class="wp-block-syntaxhighlighter-code ">
  <pre class="brush: python; title: ; notranslate" title="">
from pydub import AudioSegment
input_m4a = AudioSegment.from_file('input.m4a')
for i, chunk in enumerate(audio&#91;::900000]):  # 15 minute chunks
    with open('output_{0}.mp3'.format(i), 'wb') as output:
        chunk.export(output, format="mp3")
</pre>
</div>

And voila, it was done. Of course, I needed to have ffmpeg installed in my machine &#8211; which btw, is highly recommended!

 [1]: https://support.microsoft.com/en-us/office/transcribe-your-recordings-7fc2efec-245e-45f0-b053-2a97531ecf57
 [2]: https://ffmpeg.org
 [3]: https://github.com/jiaaro/pydub