---
layout: post
title:      "Post-Grad React-ions"
date:       2019-03-15 21:48:32 +0000
permalink:  post-grad_react-ions
---


After graduating from Flatiron School in the middle of December, I wanted to throw myself right into the job search without pause.   I was presented with the opportunity to work part-time as a Tech Coach at Flatiron, supporting students in the online program that I had just completed.  This was a blessing for so many reasons.  One reason being that I have had an amazing experience helping students while simultaneously sharpening my own skills.  Another reason being that I have had time to reflect on what parts of coding come more naturally to me and what parts take more work.  

During these two months as a Tech Coach, I have been spending some of my free time working through challenges on HackerRank and Codewars and working to improve the applications that I made during my time at Flatiron.  The majority of the questions that students ask are about Ruby, RoR, or basic JS concepts so I feel fairly comfortable in those areas. There are other concepts, frameworks and libraries where I have been feeling a bit rusty.  This week I have been working to refresh my memory on React and Redux and sharpen those skills.  

I created a React-Redux application during my time at Flatiron and I thought that looking at a functioning application would remind me how all the different pieces should fit together.  Unfortunately, my application was not fully functioning so instead of easing back into it, I dove headfirst into fixing mode.  The issue was in my "Delete" action. I had originally been calling my "Fetch" action after deleting an item so to update the state. The last time I worked on my application, I knew that I wanted to delete an item and update the state in one fell swoop so I had removed the call to my "Fetch" action but I never wrote the necessary code.

My first stab at updating my "Delete" action was extremely messy and I sent a lot of unneccessary data to my reducer. Instead of sending the deleted item, I send the response of the delete action:

` .then(responseJSON => {return responseJSON})`
` .then(groceryItem => { dispatch({ type: 'DELETE_GROCERY_ITEM', payload: groceryItem })})`


In order to return the new state without the deleted item, I was using the filter method and returning all items that did not have the id of my deleted item. With the mess of data that I sent, this filter method looked like this:

`state.groceryList.filter(item => item.id !== parseInt(action.payload.url.split("/").pop()))`

Why was I even passing all of that unnecessary data? Why couldn't I just pass in the item that I was deleting and use that items id? Well, it turns out I coud do that! My mistake was trying to mimic my "Add" action where I turn the resonse to json and then send that data to the reducer. But I don't even really care about that response! Instead, I just needed to tell it to send the item that I deleted to the reducer like so:

`.then(response => dispatch({ type: 'DELETE_GROCERY_ITEM', payload: groceryItem }));`

Which means that my filter method can be much cleaner:

`state.groceryList.filter(item => item.id !== action.payload.id)`

Much prettier!  

Although it is nice to do things right the first time, there is often a lot to be learned when taking the long way! Since my first attempt made my application work, I considered leaving it how it was even though I knew there had to be a better way.  Through use of "debugger" and multiple google searches, I had an epiphany.  I realized what was actually happening in my original code, how to fix it, and why/how my new code is an improvement.  

I now feel much more confident revisiting concepts and even taking on new ones.  I am already looking for the next challenge!
