---
id: 131
title: There is No Such Thing as Too Complex
date: 2011-08-12T16:07:54+00:00
author: George Beech
layout: revision
guid: http://brokenhaze.com/blog/2011/08/12/61-revision/
permalink: /2011/08/12/61-revision/
---
This is a crazy idea, but it's true there really is no such thing as too complex in an IT environment. If you take a moment to think about it, everything we do is incredibly complex. Really, just take a moment to think about it. There is not one thing that you do as a Systems  Administrator that isn't complex. 

You still don't believe me do you? Fine. Lets take a look at a very simple operation. We are going to monitor a single box via SNMP. We are going to assume that you already have a central monitoring box already setup. 

1. You configure your box-to-be-monitored with SNMP, configuring the proper access controls 
2. You add any extra scripts that you need to call via SNMP
3. You open the firewall on the box to allow SNMP traffic
4. You configure your monitoring server to query the box-to-b-monitored via SNMP
5. You check the results

And, THAT is the simplified version of events. In reality there is a lot more that goes into just the simple process of monitoring ONE machine. That really is complex, and it's not a bad thing. 

<a href="http://brokenhaze.dreamhosters.com/blog/wp-content/uploads/2011/08/complexity.jpg"><img src="http://brokenhaze.dreamhosters.com/blog/wp-content/uploads/2011/08/complexity-300x225.jpg" alt="" title="complexity" width="300" height="225" class="alignnone size-medium wp-image-64" /></a>

Now having said this:
> There _is_ such a thing as **BAD** complexity. 

Bad complexity is complexity for the sake of making something more complex, or the inverse: making something less complex for the sake of being *not* complex. What you want to do is create a system that is of the **correct** complexity. That is you want to create a system that is neither too simple, nor too complex. 

The problem that you run into with either end of the complexity spectrum is this: either you have a system that is too basic and cannot be scaled properly as the need arises *or* you have a system that is unmaintainable, and cannot scale because there are too many pieces meshed together.

When you are designing a system, you really will never achieve the perfect amount of complexity. There will always be trade-offs you have to make, based on past design decisions, future configuration considerations, and application constraints. However what you can do is make every decision in a thoughtful way that tries to strike a balance between the two extremes of complexity. And that, is one of the true zen things when you are a sysadmin. You achieve this beautify nearly perfect level of complexity system, and you sit back and smile. Then you go run to put out the next fire.