# Processes 2
## Process Creation
An OS must facilitate ways for users to create new processes

Typically, a system process (parent) creates a user process (child)

In the event that a user process needs to create another user process, the OS provides [[System Calls|system calls]] to do that
- In UNIX-based operating systems, processes can be created using the [[fork()]] system call