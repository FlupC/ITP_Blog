---
path: CADMidterrm
date: 2021-03-18T01:20:59.859Z
title: "CAD For Virtual and Reality: Midterm - 4 Bar Linkage"
description: Midterm for CAD for Virtual and Reality - Ben light, Spring 2021
---
# Bottle Opener

Initially, I set out to build a 4-bar linkage that would turn the page of a book. The pattern I devised looks like this:

PATTERN

This is well and good, I think that the actual path is fine, but I ended up having to change my idea for a reason I will explain later.

### Initial Issues

While I was starting this project, I had a lot of issues with making the linkage work. Whenever I would dimension the piece, it would get very stuck on the bottom.

VIDEO OF THAT

It turns out that this occurs because when dimensioning, I actually dimensioned relative to the floor. Once Ben pointed that out, I was able to fix the issue.

I then ran into some trouble with the shape. Basically, I couldn't make the end effector follow the path. This was because I got a little lost in how the shape would be. Many of the in class examples had the connector between points A and D, but mine was off in its own area. This meant I needed to add more geometry in order to fix the issue. I added triangle BFE and it all worked.

### Impossible Movement

After I made slots and extruded them, then connected all of the joints, I ran the motion.

`vimeo: https://vimeo.com/525280970`

As you can see from the video, there is clipping 

IMAGE

Hi, i know this iis not done yet. Should have it done tonorrow morning. hopefully this is sufficient. 