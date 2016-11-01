# Management As Multithreading

> What if developers and managers can be models using the same concepts as in multi-threaded software.

As developers we often talk about limiting work in progress. The reasons for this are well understood thanks to books like [The Phoenix Project](https://en.wikipedia.org/wiki/The_Phoenix_Project_(novel)) and [The Goal](https://en.wikipedia.org/wiki/The_Goal_(novel)) before it. As a developer I notice that this is not entirely unlike a single thread in my software doing a single piece of work at any one time.

Obviously, in an organisation of any size, you are going to have many individuals in many teams all working on towards different goals, and so you must have multiple work streams, even a single work stream is only working one task at once. This is a parallel for multithreading; increasing through put by increasing the number of channels available to do work.

Some of the roles of management in an organisation are to ensure that different work streams: 
 - Have work to do
 - Have access to the resources they need
 - Timelines align with those of other related teams

If we apply the idea of multi-threading to the space of work stream management, we might find some insight in to how teams might work better, and work better together.

## Concepts

### Forking/Joining

When a program reaches a point where work can be executed concurrently multiple threads can be created to perform this work concurrently. After work has been done on multiple threads, the program will reach a point where all concurrent work must have been completed before the program may continue.

When a stream of work reaches a point where multiple tasks may be conducted in parallel, e.g. multiple clients must consume the same service, and completion of these tasks must be synchronised, e.g. for a product launch, the manager is essentially forking threads of working, waiting for them to complete and joining these threads again before continuing execution of the peice of work.

From this analogy it seems that it might be worth an experiment in visualising work streams as threads complete with forks and joins so that dependencies might be made visible to the streams involved, and so that the limited number of works streams available (as in a limited number of available threads) can be used to show when work is able to be executed concurrently but cannot be due to other constraints, such as lack of a team/individual to conduct the work until other work has been completed.

### Locks

When two threads are trying to operate on the same resource, we often use locks to ensure that they do not interfere with each other. This means that the act of waiting for a resource to become available, be it a response from a request made to another thread or simply the right to access that same resource is a blocking operation. This mirrors the problem of workstreams being blocked when waiting for dependent tasks and resources to become available. Obviously steps are taken to ensure that the team does not remain blocked. Parking a task and continuing on another is a form of asynchronous work.

### Preemptive Multi tasking

This is probably the most common form of multitasking as an individual worker. You work on a task until someone interrupts you and asks you to do something else. This *does* allow you to be highly responsive as other parties to not have to wait for you to finish your task before interacting, but both humans and computer must context switch every time they are interrupted. For computers this overhead is so minor it's barely even considered, but for humans it is a huge inconveinence and frustration. One of the biggest completains I hear around the office is "I keep being interrupted, I can't get any work done". While this model works well in software for greatly increased flexibility, the trade off of context switching makes this a very painful and flow way of of managing concurrent tasks.

### Cooperative Multi tasking

In contrast to preemptive multi-tasking, cooperative multi-tasking allows the code or the worker to break multiple long running tasks down in to smaller chunks, so that when an individual chunk has been completed, a chunk from a different task can be conducted. This has several parallel swith agile software delivery. Small work items allow management (or the coordinating code) to choose its work dynamically rather than commiting to long periods without the ability to react and change direction. In our work, this may be a change of business or technical direction, in software this may be the decision to stop enumerating a complex data source. This model sacrifices the ability to interrupt a task, also reduces the obstacle of context switching. As humans we are also inclined to be happier about context switching when had got to a natuarl break in the work.

The lack of any ability to interrupt tasks can be a problem in software and in our work. Runaway threads/tasks or tasks that have become blocked never unblocked must be managed. Cooperating multitasking offers you nothing in this area; so while it is a much easier way for us humans to work it is useful to keep preemptive multi-tasking as a weapon on your arsenal in the unfortunate instance that a task or thread gets out of control.

### Thread Pooling

### Task Scheduling

prioritisation
timing
task allocation


### Runaway Task Management




-------


When writing multi-threaded software there are numerous different tools and techniques we use to manage the work being done across these threads, and managing their interaction with shared resources. 


Forking/Joining
Message Passing
Locking
Mutexes
Task Scheduling
Runaway Task Management




Developers with WIP limits of 1 are a single thread.
An "organisation" obviously must have multipe developers doing multiple things.
This is the same as multi-threading.
Management is forking and joining developer threads, facilitating access to shared resources.





In software development we go to extreme lengths to manage


Be this sharing a resource (Locks and Mutexes and messaging and immutability, anything we can do to make sure we're not actually working on the same data at the same time)
or adhering to the single responsibility principle, to make sure we don't confuse ourselves by doing too much at the same time.
