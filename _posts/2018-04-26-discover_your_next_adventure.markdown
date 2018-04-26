---
layout: post
title:      "Discover Your Next Adventure!"
date:       2018-04-26 15:03:37 +0000
permalink:  discover_your_next_adventure
---


Are you in need of a vacation but don't know where to go? Look no further than my CLI Application gem "destinations" which is published on RubyGems at `https://rubygems.org/gems/destinations`.  The application produces a list of four categorized "Best of Travel" lists from Lonely Planet. Then, in response to user input, the application produces a list of ten destinations.  From there, the user can ask for more information about that destination or return to the main menu.

I am very happy with the final product, but the road I took to get there was winding and bumpy!  

I eagerly read through the CLI Data Gem Project ReadMe. The very first instruction is "Watch this video walkthrough of building a CLI Gem called Daily Deal before you begin".  I open the video and see that it is over an hour long.  Do I really need to watch this whole video? What if I just watch the beginning to get started? Surely if I look at the example gems I can figure it out on my own from there!  Right? WRONG.  

In the few minutes that I did watch of the video, the importance of careful planning and organization was made quite clear.  Did that stop me from diving into my application without planning or organizing? Of course not!  I worked quickly, moving back and forth between the CLI class, the scraper class and the destinations class, and I had a fully functioning application within a few hours.  Was it really that easy? Of course not!  Upon revisiting the example gems I realized that my destinations class was not actually creating and storing instances.  Instead, the class was essentially just a home for various methods that produced the scraped information.  

What do I do now? How do I fix this without completely starting over?  For starters, I went back and watched the entire, incredibly informative, video.  I then returned to the example gems with a new understanding of what I was trying to do. From there I was able to restructure my code so that I was utilizing my classes properly.  That is not to say that I reworked my application quickly from there.  Oh no, I still had some struggles along the way!

At this point, I vowed to thoroughly read (or watch) all future instructions so that I could truly understand what steps I should take to execute a project.  However, I was still skipping a key step in the gem-creation process: planning ahead.  Rewatching the video taught me how to create *a* gem, but it did not tell me how to create *my* gem.

Since I was stubbornly clinging to the code I had written the first go-around, I never took a step back to map out the specific classes or methods that I would use.  What continued to trip me up was that I was scraping from five different webpages. I had already decided that I would have three classes: the CLI class, the destinations class and the web scraper class.  Did this mean I needed five scraper classes? Or should I have another class that has "list" instances? After much deliberation, I realized that I was trying to fit a square peg in a round hole.  My gem is not the same as the example gems, so why am I trying to structure it as if it were?

It was a long journey, but I eventually arrived at my destination - pun intended - and it was worth the wait!  Although I would have saved a lot of time and energy had I read/watched the instructions and come up with a detailed plan from the onset of the project, I am glad that I took the long way to get there.  I would likely have the same level of understanding of the gem making process either way, but I would not have been reminded of two very important lessons: 

1. You cannot run before you can walk
2. The shortest distance between point A and point B is a straight line

You cannot create an application (running) before you have a deep understanding of what you are trying to produce and how you will produce it (walking).  The most efficient way to get from an idea for an application (point A) to a functioning application (point B) is to start with a solid foundation so that you do not have to overcompensate later for weaknesses is the applications general structure.

Planning ahead is an integral part writing code.  How can you write the best and most efficient code if you only have a vague idea of what you are trying to make?  In the future, I will ALWAYS have an organized and detailed outline before starting a project so that I can spend more time making - and learning from - mistakes in my actual code rather than in my planning!

Lesson Learned!


