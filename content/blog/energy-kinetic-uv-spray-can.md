---
path: energy-kinetic
date: 2021-03-16T02:25:23.457Z
title: "Energy: Kinetic - UV Spray Can"
description: Kinetic Assignment, Spring 2021
---
# Kinetic: UV Spray Can

FINAL VIDEO:

### Concept

When thinking of kinetic energy, a lot of ideas that come to mind involve rotation. But, I didn't really love the idea of spinning or cranking some sort of motor to produce electricity. 

So, I decided to iterate on the idea of a shake-light. These lights use magnetic induction, which gets stored in (usually) a battery and then discharged when the light is switched on. 

The motion of shaking got me thinking about spray cans, which you have to shake in order to 'power' the mechanism to shoot out paint. 

I thought about how you could really do that same motion to charge a capacitor, but how could you paint?

After doing some research, I came across some UV reactive acrylic that "glows" when you shine UV light on it. And thus, my project was born. 

### Prototype

The first thing I did was order a shake light and a UV laser pointer-esque device on amazon. Then, I was able to break down and reconstruct the piece into a working prototype:

* Took apart a laser pointer and stole the diode

![Pointer Stripdown](/../assets/energy/kinetic/stripdown.jpg)

* tested the diode in circuit

![Diode in Circuit w 33ioT](/../assets/energy/kinetic/inCircuit.jpg)

* Ripped apart a shake light
* Pull out the contents, desoldered the original LED, soldered wires and the laser diode on

![Solder](/../assets/energy/kinetic/capacitor.jpg)

![Prototype](/../assets/energy/kinetic/prototype.JPG)

* Tested the laser reactive vinyl

`vimeo: https://vimeo.com/518353250`

This prototype was actually all I was able to do for some time.

I wasn't able to easily produce enough light from the diode in order to actual achieve anything interesting.

The shake-light came with a NiMH (nickel metal hybrid) battery that could supply 3.5V when fully charged. This was not actually functioning well.

Initially, I was under the impression that I was not able to supply enough voltage for the light to work. I wasn't able to measure much energy at all from my shake light, and the current I was able to produce was even less measurable.

For some time, I thought I was completely out of luck. I even ended up spending more than I'd like to admit on copper wire spools to generate more electricity. Then, I learned about an Oscilloscope. 

### Understanding Magnetic Induction

![Oscilloscope Setup](/../assets/energy/kinetic/Oscope.jpg)

The first thing I was able to learn in office hours is that I am not really able to visualize what is happening with either my coil and magnet, nor my capacitor without an oscilloscope. 

So, I started to take a look. The largest issue with my circuit was simply that it takes a lot more shaking than I initially thought. Additionally, without a capacitor to discharge my stored power quickly, there just wasn't going to be enough light from the LED. 

The reason making bigger coils didn't work is because the size of the magnet and the size of the coil length should be similar and the magnet should have the ability to move all the way in and out of the coil.

### Completing the Circuit

![Circuit](/../assets/energy/kinetic/circuit.jpg)

The actual circuit for this piece is quite simple, actually. The magnet passes through the coil, which sends electricity to a full-bridge rectifier, which charges the capacitor. When the switch is closed, it will discharge the capacitor and turn the LED on. 

I was able to harvest my prototype, remove the original battery, and set up a new working skeleton for my final piece. 

![Skeleton of SprayCan](/../assets/energy/kinetic/skeleton.jpg)

The fact that this single body worked right out of the box influenced me to make it the center for the rest of the project.

`vimeo: https://vimeo.com/524081002`

### Fabrication

Here is the fabrication process I took for this assignment. There had to be some iterations of certain elements, but they were minor. 

#### CAD

`vimeo: https://vimeo.com/524090302`

#### Printed Parts

![Bottom piece](/../assets/energy/kinetic/1.jpg)

![Secured Skeleton](/../assets/energy/kinetic/2.jpg)

![Top + Bottom](/../assets/energy/kinetic/3.jpg)

![Circuit Board Holder](/../assets/energy/kinetic/4.jpg)

![Put Together](/../assets/energy/kinetic/5.jpg)

### Next Steps

Unfortunately, this project requires up to 20 minutes of shaking for very short periods of light. This makes it largely impractical for almost all applications. 

I want to iterate on this further. 

Right now, I am using 2 small screws on the bottom of my can to supercharge the capacitor, so that I can actually paint with the device. Ideally, I can combine techniques to boost voltage with a larger, more powerful magnet to create a spray can that actually gives me the feedback I want it to. 