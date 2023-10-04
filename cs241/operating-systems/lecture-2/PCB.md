### Definition
A data structure used by the OS to store metadata about a process in memory
- Implemented as a doubly linked list in UNIX
### Necessity
It is pivotal to track the state of a process while it's not actively executing, as well as manage **scheduling queues**
### Contents
The PCB stores:
- Process ID (PID)
- Program State
- IO Status 
- Pointers to Scheduling Queues
- Program Counter
- Accounting Information
- Register Contents
- Memory Management information (such as memory limits & lists of open files)