---
layout: post
title: Thread pool
---
Thread pooling is one of the important concept in improving the efficiency of the server.As many of you know,threads are used for running  concurrent tasks or jobs.They are mainly used in serving web requests.For example,lets say you are uploading a picture on facebook and similarly like you, many people are doing the same task simultaneously.There are two ways of solving this problem ,either you create a separate thread for every job or a separate process.But the threads are light weight and time efficient than creating a process for every job(why is that ,you can find difference between thread and process on internet).
And other advantage is ,you can run threads on multiple processors.

There are three steps in threads lifecycle

1.Creating thread

2.Run the job

3.Destroy the thread

What happens if the jobs you are running are very short.......
.

.

.

You will be wasting lot of CPU cycles on creating and destroying the threads.So here comes the Thread Pool concept ,where you already create a predefined set of threads ,and allocate jobs when they are available,thus saving lot of time.
Java provides a thread pool library ,below is a simple example.

**How to create a simple ThreadPool class in Java**

```  java
public class ThreadPool
{
int MAX_THREADS=10;
ExecutorService executor = null;
static ThreadPool tp = new ThreadPool();

public ThreadPool getInstance()
{
return tp;
}
public void start()
{
executor = Executors.newFixedThreadPool(MAX_THREADS);
}
public void executeTask(Runnable task)
{
if(executor!=null)
executor.submit(task);
}
public void shutdown()
{
if(executor!=null)
executor.shutdown();
}
}
```

You can use Callable interface ,if you want the job to return some value 
