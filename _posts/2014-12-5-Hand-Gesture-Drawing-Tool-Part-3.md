---
layout: post
title: Hand Gesture Drawing Tool Part 3
---

In the previous post ( [Part 2](http://golisandeep3.github.io/Hand-Gesture-Drawing-Tool-Part-2/)) I explained about the system Architecture of the tool.In this post,I will concentrate on ,how to use the tool and also some of the challenges faced.

<h4>Gestures</h4>
There are mainly four types of Gestures that Leap Motion software can identify (circle, key tap, screen tap and swipe). The following gestures are mapped to draw basic shapes.

<h5> Drawing circle</h5>
To draw a circle, the user has to rotate the index finger either clockwise or anticlockwise direction. As shown in the figure below the index finger is rotated in the form of a circle.

![Circle Gesture](https://github.com/golisandeep3/golisandeep3.github.io/blob/master/_posts/circlegesture.jpg?raw=true)

<h5> Drawing Arrow</h5>
To draw arrows just make a key Tap gesture by tapping it downward. This gesture is similar to pressing a piano key.

![Arrow Gesture](https://github.com/golisandeep3/golisandeep3.github.io/blob/master/_posts/arraowgesture.jpg?raw=true)

<h5> Drawing Rectangle</h5>
To draw rectangles make a swipe gesture by a linear movement of a finger. 

![Rectangle Gesture](https://github.com/golisandeep3/golisandeep3.github.io/blob/master/_posts/rectanglegesture.jpg?raw=true)

<h5> Erase Diagram</h5>
To erase the complete diagram just make a quick forward tapping movement by a finger. This gesture is similar to touching a vertical touch screen.

![Erase Gesture](https://github.com/golisandeep3/golisandeep3.github.io/blob/master/_posts/erasegesture.jpg?raw=true)

<h4>Challenges</h4>
There are many challenges associated with the accuracy and usefulness of gesture recognition software. One of the challenges is mapping gestures to draw different shapes. Since there are limited numbers of gestures we could identify right now, it’s better to use free form diagram recognition.
<h4>Limitations</h4>
•	Using this tool you can only draw 3 shapes circle, rectangle and arrow. 
•	Also the size and color of the shape cannot be controlled by the user. 
•	You cannot edit an existing diagram.
<h4>Future Work</h4>
•	Integrating voice with hand Gestures. Using voice commands we can   control the properties of the shapes.

•	Ability to draw free form diagrams.

You can find the demo video ([here](fff))

<h4>References </h4>
1. “Comparing Gestures and Diagrams” Barbara Tversky,Azadeh Jamalian Columbia University
2. “An Interactive System for Recognizing Hand drawn UML Diagrams” Edward Lank Queens University
3. https://developer.leapmotion.com/documentation/java/devguide/Leap_Gestures.html


