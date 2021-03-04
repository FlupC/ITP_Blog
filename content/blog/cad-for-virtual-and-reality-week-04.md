---
path: CADWeek4
date: 2021-03-04T00:24:31.073Z
title: CAD For Virtual and Reality Week 04
description: Assignment for Week 4
---
# Connector Assignment

For my connector assignment, I really really did not want to make a box with two threads in it. I was struggling to come up with an idea when my friend sent me one of my [favorite videos](https://www.youtube.com/watch?v=LDU_Txk06tM&ab_channel=MonstercatInstinct).

Here is what I made to represent the crabs in that video:

![Final Output](/../assets/cad/week04/ConnectorFullBody.PNG)

Here is the sketch. As you can see, it is just a couple of paths and lines.
![sketch](/../assets/cad/week04/connectorSketch.PNG)

The majority of the design comes from actually sweeping the paths, then lofting to offset planes. You can see the timeline here:

![Timeline for Connector](/../assets/cad/week04/connectorTimeline.PNG)

I chose not to add fillets, but I am not 100% confident in that decision. I tried them and they needed to be tight so they wouldn't create an impossible object. Sometimes it looked good and other times not so much, so I left it as is. 

# McMaster Carr Component

For some reason, I am enjoying designing lamps and lights right now. I don't think they're all that compelling or interesting yet (the last one was pretty much a glorified google home now that I look), but I want to get better at it. 

Here is my final output, with some screenshots of the individual components. I used a "Lamp" Component, with other child components for the whole project. Made working a lot easier and more effective. Probs won't do much more body modeling like we have been. 

![lamp Full](/../assets/cad/week04/lampFull.PNG)

![lamp base](/../assets/cad/week04/base.PNG)

![lamp rod](/../assets/cad/week04/rod.PNG)

![lamp light](/../assets/cad/week04/light.PNG)


### Component

The component I used here is the [Zinc-Plated Steel Ring-Grip Quick-Release Pin](https://www.mcmaster.com/98320A135/). I chose this piece because I thought it could be a cool mechanism to turn on and off the lamp. I'd probably create some sort of stopper for it so it never comes out. 

I implemented it by creating a hole in the rod, stretching it long enough, then aligning the component to the hole (but then I had to rotate it too).

![McMaster Component](/../assets/cad/week04/McMasterComponent.PNG)

