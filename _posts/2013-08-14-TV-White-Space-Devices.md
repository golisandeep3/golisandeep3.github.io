---
layout: post
title: Broadband Connectivity through TV White Spaces
---
Indoor Localization is a hot topic and has uses in different fields.If you look at current GPS systems which mainly work only in outdoors,thus limiting navigation in indoor environments.Even GPS  systems are accurate upto 100nsecs (30 meters) ,so this may not be feasible to use for indoor applications,which require around nano second accuracy. Indoor Localization technology helps to achieve this nano second accuracy. 

There are various methods that can be used to track the user in indoors.One of the approach is calculating Time of Flight (TOF).Time of Flight is the round trip time that a signal takes to reach its current position from the destination.If you know the position of the destination,then you can calculate the distance between the destination and current position by multiplying TOF with speed of light.The problem with this approach is ,there will be a variable delay at the destination as well as at the receiver.Since the delay is variable,the measurements will not be accurate.
While i was working in CSIRO Australia,i did experiments with their own in built Software Defined Radios and could achieve the accuracy within 1 meter.

**Some of the Applications I could think..**

If you go to big shopping malls or in Airports,it is hard to find the place that you are looking for.For example ,I always look for McDonald ,during my layover at Airports.I have to ask many people to find it.

Similarly in big grocery stores,Its very hard to find particular item.If there is an indoor map which shows locations of all items and could accurately identify your position.It saves lot of time for end user.
