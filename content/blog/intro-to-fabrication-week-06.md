---
path: fab-week6
date: 2021-05-06T03:26:20.433Z
title: "Intro to Fabrication: Week 06"
description: Motor Mounting
---
# TikTok Scroller

For this week, I wanted to make a piece that automated scrolling through TikTok. Ideally, this would be wirelessly connected such that one could put the phone anywhere in the room and use a button to scroll from wherever they were.

I also wanted it to look sleek and like a single, unified piece, that flows nicely. To achieve this, I chose to use acrylic and bend it into the complex pieces.

`vimeo: https://vimeo.com/545323785`

# Code: Part 1

Before starting this, I wanted to understand the technology that would be required from a pComp perspective. I understand that Ben cares more about the P than the Comp, but I felt it necessary to document this.

`vimeo: https://vimeo.com/545323770`

The way that this circuit works is quite simple really. I used a continuous rotation servo to spin 1 time in 360 degree rotation. There is definitely some weird play with the calibration, though. For the most part, it does the rotation well (sometimes adjust speed values), but there is an issue where setting the speed to 0 can require adjustment with the internal potentiometer. In a future iteration, I think I would try and use some other type of motor, or just see how I can keep this consistent.

I also added a button with state control to tell the arduino when to rotate the servo. This was simple to implement.

I will come back to the code a little later, but first:

# Motor Mount

![](https://lh5.googleusercontent.com/sFLXQKsQxiS-M-z6D32q06uluSKOZmCSUNdQWQq8EoCT1d9CdKKAl6qiW6sFwJH7qs9Hen95aLGsOHJEF1ZQqOv1caF_DH42mIX7lstonAlYcjl4Miy_nlJ4eJ1xCXCzkOJM--jM)

Here are all of the test cuts I did in cardboard. There was too much risk in cutting on the acrylic, so I did as may tests as I could beforehand. Eventually, I managed to line up all of the holes properly.

I couldn't find a schematic for my motor online, so I tried to use the calipers, but they were nowhere to be found. I used a ruler and tested a lot. One thing I didn't have to worry about, though was the size of the holes. I used the screw matching thing on the floor.

![](https://lh3.googleusercontent.com/Q5q5mqYQ9iRVzoZtoFWNXl0K34IhnrG4_XzFVxAOx-JjosWSLihNX0XF5mob8ABo1xika-J83QYiVXqruOuicJTHhxQcTNo1zgmuqcZe5z3NR_-kf8be-HKofr-I33B2PSuH0w77)

Eventually, this gave me the right fit.

# Illustrator

![](https://lh4.googleusercontent.com/G7aOn6i4by5DXNTCAB7JhHhCcNGazKtGoLD5CAO9pdRsWiNFa7bMc9qeJfAnOSt0i_P99NyG_7lMUVD9900ye4UgiagKDQK0btlxigVAPt9TUhwMhLW_ksp9XTQIuF9sDgT3ja4W)

Here is my illustrator file. I had to run a few tests to make sure this all worked, but ultimately, this was the best fit for everything.

I adjusted things a few times as I tested, but I feel it better to spend less time here and more on the bending

# Acrylic Bending

After printing the piece as a single block, I heated things on the bender.

![](https://lh5.googleusercontent.com/NPo1QwO0XUsO9T2wVj71HIafSGLm-OcjyhIvmOvD3XbtaAAXfiq8Xby_Mz_If61m7uEGgZLvW2rmqb7nR95zvYrvqJzifkO3bSeQT-8g58XpAILavS0YTEJl0BmQXB1xKslw_KZs)

My first Test resulted in cracking the acrylic.

![](https://lh6.googleusercontent.com/oEHi7aiS5SPgUTq6Qa06Qac-59eN3olielGpvAFHeo5KJsKJY-W4raVFWhpohq6uyA-kTzLU_hLOAIbAh6n9w_s_MWHcOgVt29Eizc6nd0mugtSM416Dmnyi7eo5FzemR5viKCFD)

That said, the other bend went just fine. However, there was this ugly film that I thought was a part of the acrylic. I had assumed it was a part of glitter acrylic.

![](https://lh5.googleusercontent.com/4gcG0w3VQ8bHn7nKj0LzsyV005kRbMvPL0VTIkXKLlZctN_4pSOhor-vgdWZkRXsnKseA6TpjqlN6XyB6YGvY1eNcaHmcAckqTaFQfBeJHemBRbehii9VSVgtUROlunFCrKZWp7I)

TURNS OUT, there actually WAS a protective film over the acrylic. It's much prettier now.

I had to do a few more iterations.

![](https://lh3.googleusercontent.com/GEgIB2XXW5dKsXBpgoljUUP82vnUblcDIy7dsMrJmQKavrBt4u9QTUNhW6t4S6WR1FpJEYSp1PPT5hYi9NFliCgMklf8nkmINoJAeI-uZwQ0oEQuLtydygFLVjWbtPeMG64JDF9_)

![](https://lh3.googleusercontent.com/gRV-RHX3Xv0Uo_Ewq5y576Z8FE-pLg_t672TJDKlC72lvlWB7pSYyCx2pQqocnKx6jUGRf5UzTvhv85UIL_UT5g12hWGBmQR3-sHOjhq1umTFrHxPrL5dJ2x0kPK4tIVQosb42xI)

# Code Part 2

This is where things got horrible. I spent about 4 hours on this before remembering that the code isn't as important to Ben.

I wanted to port the large circuit from before into 2 smaller wireless circuits. I had no issues connecting 2 Arduinos to the internet and transmitting a variable at first.

Then, very quickly, things fell apart. I think it was the arduinos I was using, but the exact same circuit was causing the arduino to short or just shut off. I spent a long time working on these circuits.

![](https://lh6.googleusercontent.com/bpa7Rs0wxiVLjI2vvt2VOkXin5Xmls56WHS2j04kVwoqcHdaXKuiyLi5daS20xqkPEqOTdIJMi-xnvbvI8LXfc_xrNpwpy1gX-N2DJm2mFoijA5FShfdap6vZZFqKEli-bOb97ac)![](https://lh3.googleusercontent.com/O_je090VaR18EWgN0YOLs-DOZzmv13zC1StFLfwUm9AHl05ql99bpwMl6UuCAj_8Sn43vrUco0SDpxfi4slEVE_UGwpqE5pjQZ0aaZwftTfNbQWtsnC0s7E9LhUx5qfLDHjNPsCP)![](https://lh5.googleusercontent.com/NyWVTyB4wr52WF4hNmc8-K81v3OeUBWxz8ugYZ7nOPnSXB3Ba1DNb36lWTrqiQ9dNai2sDnfrox8S2WE3rpbE4ZoYtTvaV18l0DH5iyLmZjHNXE0tVy979-eCjVfFoTQT5nAPLsW)

I did eventually get a super inconsistent, glitchy piece to work, but it made more sense to just make the button work better and attach it to the breadboard controlling the servo.

# Button Holder

I used a small tin to hold the button. I had some issues finding the center without calipers, but eventually got it right.

![](https://lh6.googleusercontent.com/5LhASuGDt8ZoaGaby0JFYYYLcbzptzGsCXi3rQfTfv2SRbkp0YjHgncszMkOQznBO1IcY7lSzAI6dPQYcGHYKyHtwaE1HvzXuHmE8BLb8mIq1caGPQdfU9vlJwPo-vcEfjEMO4oC)

Unfortunately, when drilling, I slipped a bit off center. I should have used something to score or dent the center to help the drill find its location.

![](https://lh4.googleusercontent.com/tQo17FmeqVO3p3kqt4lkDig9FWu0lnqBfjQbwATZ6NBuII88b4sWxtLN9PQcavgStuoNFnuRn_bZ5iI4Q0RS2vVnvCnupFbuUFyO9BM0phcQWlrZqzWzoRDw3cnteJz9Fn5RdC1t)

# Stylus Tip

I could not find a tip for a stylus ANYWHERE. I tried a few things with capacitive touch, using a battery, rubber, tinfoil, and eventually a sponge. The battery and sponge worked, but I just can not get it to accurately scroll to the next slide.

What needs to happen is I get a stylus with a proper tip that has enough give to push firmly on the screen. Otherwise, there is no way to scroll down.

# What’s next?

Firstly, I want to get this properly working. I have no real issues with the design, but there are a ton of problems with the implementation.

I also really wanted to spray paint the tin, but because I spent so long coding I ran out of time. Classic misuse of time.