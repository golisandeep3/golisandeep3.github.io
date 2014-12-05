---
layout: post
title: Hand Gesture Drawing Tool Part 2
---

In the previous post ( [Part 1](http://golisandeep3.github.io/Hand-Gesture-Drawing-Tool-Part-1/)) I explained about the tool that  I am currently working on, In this post I will  briefly explain  about the System Architecture  and the technologies used.

<h5>Technologies<h5>

Software:  Leap Motion SDK, Java

Hardware: Leap Motion Controller

You find more about how to install Leap motion Software  ( [here](http://golisandeep3.github.io/How-to-use-Leap-Motion-Controller/))


<h5>System Architecture<h5>

The software architecture mainly consists of 3 modules. The Leap motion device senses the hand movements and sends the data to the Leap Motion gesture recognition software. The Gesture recognition software analyses the data points and recognizes the hand gestures. The Drawing tool module will map the gestures with the respective shapes and draws it on the canvas.
 
(i)	Leap Motion Device
Leap Motion controller is a hardware used for sensing hand movements. It has 150 degrees field of view and a Z-axis for depth. It can track hand movements at the rate of 200 frames per second.

![Architecture](/architecture.jpg)
(ii)	Leap Motion Gesture Recognition Software
The Leap Motion software runs as a service (on Windows) or daemon (on Mac and Linux). The software connects to the Leap Motion Controller device over the USB bus. The software analyses the overall motion that has occurred since an earlier frame and synthesizes representative translation, rotation, and scale factors. The Leap Motion SDK provides two varieties of API for getting the Leap Motion data: a native interface and a WebSocket interface. These APIs enable you to create Leap-enabled applications in several programming languages (Java) including JavaScript running in a browser environment.
(iii)	Drawing Tool Module
The Drawing tool module uses leap motion API to identify gestures and draws shapes based on the respective gestures. It uses Java Swing to create GUI. The Gestures mentioned in section 4 are mapped to respective shapes and drawn using Java swing API.

In the next post( [Part 3](ghgfbh)) I will explain  more about how to use the tool..
