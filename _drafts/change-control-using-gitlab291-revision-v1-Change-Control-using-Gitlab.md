---
id: 326
title: Change Control using Git(lab)
date: 2016-02-10T17:49:54+00:00
author: George Beech
layout: revision
guid: http://brokenhaze.com/blog/2016/02/10/291-revision-v1/
permalink: /2016/02/10/291-revision-v1/
---
<h1> Pre-amble and thoughts on Change Control</h1>
<i>If you just want the cool details you can skip to the good stuff</i>

I am a strong believer in change control. It allows for many good things to be done with a well run IT organization. The top three things that come to mind are accountability, reliability and review-ability (I think i'm making that last word up). 

There are all good things to have. Many people have come before me to praise change control and that is not what I want this post to be about. I want to talk about the change control process that we are starting to use at Stack Exchange. A process that I believe addresses some of the most common complaints and push back on  implementing a change control system I hear. 

A good place to start would be to lay out exactly what those common complaints are. 

<h2>But, Change Control is too complicated!</h2>
I hear this a lot, and this particular complaint tends to break down into two different categories. The first is that there is so much process that you can't get any actual <b>WORK</b> done. The second major complaint in the category is that it slows everything down, making it harder to get awesome things done. 

I'm not going to argue with either of the characterizations. In fact the express purpose of a change control system is to put a speed bump in the way. To make you slow down a bit and think through the implications of what you are doing, to have someone else double check your work. We are not infallible, we make mistakes and that is ok. The goal here is to minimize the number of mistakes that make it into production and to minimize the times that they get there at all. 

<h2>It's just bureaucracy, busy work, an annoyance</h2>
I've met a good number of people that have this attitude. They want to be able to just log in as the administrative user and change whatever they want, whenever they want. Personally, I have given up on trying to convince these people that change control is a good thing. 

<h1>Design a process that is a speed bump</h1>
I spent a good deal of time trying to come up with a better change control system. The system should be <i>easy to use, low impact, and accessible to anyone</i> on the team. One of my over-arching design goals is to simply create a <b>speed bump</b> not a <b>road block</b>. 

I spent a good deal of time thinking about what tools we use day to day. Looking at the ones that people complained about, the ones people liked, and the ones nobody said anything about. After thinking for a while I realized that the one tool that everyone used, and there were few complaints about was our DVCS (recently moved to git). It's just about a perfect fit for a light weight change control system. 

<h2>The workflow</h2>

 You don't need anything special to get up and running with version control as the back to your change control system. The glue that brings everything together is a simple python script that does most of the heavy lifting for you. The script - called <code>robocopy.py</code> - takes the name of the system, and the risk of change and from that creates a new merge request from a template. The merge request is pretty light weight. We want all the detail to be in the actual commits and commit messages.

The basic workflow we use is to create a branch, then create a merge request based on that branch, have the change reviewed and then finally have the review merge the branch into master once the change is complete.

That's it. One long sentence to define out entire change control workflow. 

This is a very simple workflow that accomplishes all of the goals I have for a change control system. To make life even easier for people I wrote a small python script that creates the branch, copies some templates into place for you and then creates the merge request. All you have to do at this point is fill out the details and get someone to review it. 

<h1> The future</h1>
This is just v1 of the our change control system. In the future we will be adding web hooks to automatically send out notification, add calendar entries. Basically the goal is to automate all of the boring manual stuff as much as we can. 

You can get the code we use on <a href=https://github.com/gabeech/changecontrol/>GitHub</a>