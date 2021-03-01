---
path: pxp_week03
date: 2021-02-25T00:11:58.426Z
title: Pixel by Pixel - Week 03
description: Processing Project Week 3
---
# Gravity Painter

This was a really fun project. I really felt held back not understanding how to create dynamically sized arrays as well as Object Oriented Programming. 

Here I was able to understand arrayLists, declaring/ initializing/ controlling objects, and I got a fantastic refresher on Attractors and Movers. 

The idea here is that a user could create any number of attractors to paint with gravity. While I have this set up for 10 movers, I actually think there is something more interesting in using a single mover; you get unique orbits.

The user clicks to add an attractor and uses Space to clear the screen (you then need to add a new attractor to see the particles again.

# Video

`vimeo: https://vimeo.com/516469550`

# Code

### Main
```
//HW Week 02
//Philip Cadoux
//Danny Rozin
//The World, Pixel by Pixel
//Physics related code adapted from Daniel Shiffman Nature of Code

ArrayList<Attractor> attractorArr;
ArrayList<Mover> moverArr;

void setup(){
  size(800, 600);
    background(0);

  attractorArr = new ArrayList<Attractor>();
  attractorArr.add(new Attractor(width/2, height/2));
  
  moverArr = new ArrayList<Mover>();
  for(int i = 0; i < 10; i++){
    moverArr.add(new Mover());
  }
}

void draw(){
  fill(0,5);
  rect(0,0,width,height);
  for(int i = 0; i < moverArr.size(); i++){
    for(int j = 0; j < attractorArr.size(); j++){
      PVector force = attractorArr.get(j).attract(moverArr.get(i));
      moverArr.get(i).applyForce(force);
      moverArr.get(i).update();
      moverArr.get(i).display();
    }
  }
  
  for(int i = 0; i < attractorArr.size(); i++){
    attractorArr.get(i).display();
  }
  
  if (keyPressed){
    if(key == ' '){
      fill(0);
      rect(0,0,width,height);
      for(int i = 0; i < attractorArr.size(); i++){
        attractorArr.remove(i);
      }
    }
  }
}

void mouseClicked(){
  attractorArr.add(new Attractor(mouseX, mouseY));
}
```

### Attractor
```
class Attractor{
  
  float mass;
  float G;
  PVector position;
  boolean dragging = false;
  boolean rollover = false;
  PVector dragOffset;
  
  Attractor(int x, int y){
    position = new PVector(x, y);
    mass = random(5, 20);
    G = 1;
    dragOffset = new PVector(0.0, 0.0);
  }
  
  PVector attract(Mover m){
    PVector force = PVector.sub(position,m.position);
    float d = force.mag();
    d = constrain(d,5.0,25.0);
    force.normalize();
    float strength = (G * mass * m.mass) / (d*d);
    force.mult(strength); 
    return force;
  }
  
  void display() {
    ellipseMode(CENTER);
    noStroke();
    fill(127, 50);
    ellipse(position.x,position.y,mass*2,mass*2);
  }
  
}
```

### Mover
```
class Mover {

  PVector position;
  PVector velocity;
  PVector acceleration;
  float mass;
  int randomSize = floor(random(16));

  Mover() {
    position = new PVector(random(width),random(height));
    velocity = new PVector(1,0);
    acceleration = new PVector(0,0);
    mass = 1;
  }
  
  void applyForce(PVector force) {
    PVector f = PVector.div(force,mass);
    acceleration.add(f);
  }
  
  void update() {
    velocity.add(acceleration);
    position.add(velocity);
    acceleration.mult(0);
  }

  void display() {
    noStroke();
    fill(255,128,0,50);
    ellipse(position.x,position.y,randomSize,randomSize);
  }

  void checkEdges() {

    if (position.x > width) {
      position.x = 0;
    } else if (position.x < 0) {
      position.x = width;
    }

    if (position.y > height) {
      velocity.y *= -1;
      position.y = height;
    }

  }

}
```