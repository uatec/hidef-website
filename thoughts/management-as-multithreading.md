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

From this analogy it seems that it might be work an experiment in visualising work streams as threads complete with forks and joins so that dependencies might be made visible to the streams involved, and so that the limited number of works streams available (as in a limited number of available threads) can be used to show when work is able to be executed concurrently but cannot be due to other constraints, such as lack of a team/individual to conduct the work until other work has been completed.

### Message Passing

for monitoring, for interaction with other independent services

### Locks

### Cooperative Multi tasking

### Preemptive Multi tasking

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
