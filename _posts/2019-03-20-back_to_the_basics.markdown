---
layout: post
title:      "Back to the Basics"
date:       2019-03-20 21:22:05 +0000
permalink:  back_to_the_basics
---


I spent much of yesterday nervously anticipating 9:00 PM when I was to hold my first study group.  I signed up to host the "Intro to Ruby" session which seemed like the best option for my big debut.  I chose this group for two main reasons. The first being that I wanted to feel extremely confident in the material since I was not feeling all that confident in regards to how I was going to run the session.  The second reason was that I was excited by the challenge of helping students understand the foundational concepts of Ruby and programming in general.  

In preparation for the evening, I set up a powerpoint presentation that went over basic concepts and definitions, provided examples and posed questions about the material.  I was undoubtedly overprepared, especially considering that only two students had RSVP'd to the group, but I wanted to be sure that I would be able to answer any and all questions that came my way.  Just before 9:00PM I started the Zoom meeting and waited for students to join the call. At 9:15PM when no students had joined I felt that I could reasonably assume that no one would be attending the session and I closed out of Zoom.  I immediately began to second guess myself and rejoined the meeting. After all, the study group was listed as an hour long and who is to say that someone would join late? 

Well, no one ever joined my study group and since it was at 9:00PM I cannot say I blame them!  Despite feeling a bit disappointed, I have no regrets about the time and energy I put into getting ready for the study group.  On top of the preparation, I continued to review fundamental Ruby concepts as I waited for someone (anyone!) to join the meeting.  I thought that I would feel rusty but reviewing these basic concepts actually reminded me of how much I know and understand.  One way I prepared for the study group was by redoing some of the labs from the early lessons.  I was amazed at how quickly and easily I was able to complete what I had previously considered so challenging.  

One of the labs that I took on was a CLI Tic-Tac-Toe application.  In this application, an instance of the `TicTacToe` class initializes with  `@board = [" ", " ", " ", " ", " ", " ", " ", " ", " "]`. When a move is made, the `@board` array is updated to have an "X" or an "O" at the index specified by the player.  The lesson called for a `turn_count` method which would return the number of turns that had been played based on the `@board` array.  When I first completed this lab a full year ago in March 2018, my `turn_count` method looked like this:

`def turn_count
  counter = 0
  @board.each do |turns|
     if turns == "X" || turns == "O"
       counter += 1
     end
  end
  return counter
end`

Although this code works just fine, it is quite wordy.  When I rewrote the code in my application yesterday, I chose not to look at my previous version until afterwards because I wanted to start with a blank slate.  My new `turn_count` looks like this:

`def turn_count
    @board.count{|spot| spot != " "}
  end`
	
Although a clear and concise one-line method body is clearly preferable to a long-winded and messy seven-line one, I am more interested in how my thought process has changed over the past year.  This time, using a counter variable and an `each` iteration never even crossed my mind.  When I wrote the original method, I played it safe and forced the familiar `each` method to work with an `if` statement and a `counter` variable to get the desired outcome.  Although the `select` method is hardly a daring choice, this time my first instinct was to find the *best* solution that I could instead of settling for what I thought was the *easiest* solution.  

One of the best things about coding is that a single line of code can almost always be written in any number of ways while producing essentially the same result.  I by no means believe that I always, or even usually, choose the most efficient way to write something, especially my first time through.  Although it would be silly to make an argument that less efficient code is ever better than efficient code, I do think that there is value in the mindset of "let's just get this thing to work even if it's not pretty".  I may not have realized it at the time, but writing ugly and inefficient methods forced me to gain a deeper understanding of the concepts and techniques that I was using.  Had I been aware of `count` prior to my first attempt at the `turn_count` method, I probably would not have understood how `each` iterations, `if` statements and `counter` variables work quite as well as I do now.  

In order to retain a position where you can produce effective outcomes in an efficient timeline, you must know how you got there in the first place.  The mini refresher course that I gave myself yesterday gave me a look at the building blocks that have gotten me to this point.  I feel like I have a sturdy foundation and I am ready to keep building!
	
	
