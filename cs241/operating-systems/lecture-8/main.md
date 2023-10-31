# Threads
## Definitions
We can define a [[Thread|thread]] and begin to think about accompanying paradigms such as that of [[Single-Threaded Process|single-threaded processes]] and [[Multi-Threaded Process|multi-threaded processes]]
## Threads vs Processes
Generally, threads are preferred over processes; this is because thread creation has less overhead than process creation
- For example	in Solaris, process creation is 30x slower than thread creation, and context switching is 5x slower than thread switching

There are a number of other [[Benefits of Threading|benefits]] which also make threading desirable in a computer system
## Concurrency vs Parallelism
It's important to distinguish between [[Concurrency|concurrency]] and [[Parallelism|parallelism]] as it's possible to have the former without the latter
- For example during the latter half of term, you might be part-way through multiple courseworks – these are concurrent. Since you can’t work on two courseworks at the same time, these are not parallel

There are also different types of [[Parallelism|parallelism]], namely:
1. [[Data Parallelism]]
2. [[Task Parallelism]]
### Amadhl's Law
Provides us with a way to precisely describe the speedup in computation time offered by parallelism
![[Pasted image 20231030151634.png]]
Note that as N approaches infinity, our upper bound approaches 1/S
## Thread Synchronisation
When multiple threads write to the same location, we must synchronise them to avoid [[Race Conditions|race conditions]]

A common way to synchronise threads is to use [[Mutex Locks|mutex locks]]