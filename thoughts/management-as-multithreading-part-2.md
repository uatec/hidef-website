
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
