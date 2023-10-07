# Processes 2
## Process Creation
An OS must facilitate ways for users to create new processes

Typically, a system process (parent) creates a user process (child)

In the event that a user process needs to create another user process, the OS provides [[System Calls|system calls]] to do that
- In UNIX-based operating systems, processes can be created using the [[fork()]] system call
### Options
#### Address Space Options
- In UNIX's [[fork()]], the child's address space is a duplicate of its parents
- In Windows, a similar function CreateProcess() requires specifying a new program to be loaded into the address space of the child
#### Resource (CPU, Memory, File) Sharing Options
Either:
- Parent and children share all resources
- Children share a subset of parent resources
- Parent and children share no resources
#### Execution Options
Either: 
- Parent and children execute concurrently (as with [[fork()]])
- Parent waits until children terminate
## Process Termination
A process typically terminates after its last statement, at which point all resources held by the process are released

Otherwise, it can be terminated by the `exit (int status)` [[System Calls|system call]] which returns a status code to the parent

- After a child process is terminated and before its exit status is collected by the parent it is called a [[zombie process]]
- If the parent process exits before the child, the child process becomes an [[orphan process]]

Usually, [[Orphan Process|orphan processes]] are assigned the `init` process as a parent which periodically calls `wait` to collect the return IDs of orphan processes

