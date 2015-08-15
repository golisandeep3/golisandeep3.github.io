---
layout: post
title: Optimizations in Scalable systems
---

**Event Based Systems**

In large scale systems ,the architecture will most likely be multi threaded and event based style.So,In  large systems we will be triggering lot of events based on different actions   and some of them will be duplicate events. How to get rid of these duplicate events which are redundant .These events can come from different flow of executions,so we cannot simply remove  the code which generates duplicate events. One simple solution is put all the events in a queue  and  execute them after a few secs in delay.So when a duplicate event comes,and that particular event is already in the queue ,we simply discard the newly generated event. So,this helps in getting rid of redundant events in short period of time.
There are few problems here ,how do we know ,if the event already exists in the queue.We can search the queue with event id but it will take O(n). So to reduce the time complexity we can maintain a concurrent HashMap for all the generated events.We can use delayed queue for storing the events in the queue.

