# Processes 1
## Definition
- A program is a **passive** entity stored as an executable file
- A process is **a program in execution** that is an **active entity** 
	- (a program becomes a process when it is loaded into memory)
## Processes In Memory
The **virtual address space** of a process consists of:
1. Text (program code)
2. Data (global variables)
3. Heap (dynamically allocated memory)
4. Stack (statically allocated memory)

The heap and stack grow towards each other during execution
(note that, in reality, the address space of a process may not be contiguous)
### Diagram

![[Pasted image 20231004090640.png]]
*Note that, in reality, the address space of a process may not be contiguous; the diagram is presented as such for clarity.*
## Process States
Processes can be classified into one of 5 states:
1. [[New Process|New]]
2. [[Ready Process|Ready]]
3. [[Running Process|Running]]
4. [[Waiting Process|Waiting]]
5. [[Terminated Process|Terminated]]
### Diagram
![[Pasted image 20231004091402.png]]
## Process Control Block (PCB)
An important data structure used by the OS to store information pertaining to a process is the [[PCB]]
### Context and Context Switching
- The information stores in the [[PCB]] is said to represent the **context** of a process
- When the OS Performs a **[[Context Switch]]** away from a process, it is necessary to save this context to memory so it can be performed later
#### Effects of Context Switching
- Context switching represents an overhead for the OS
- A simple PCB and OS will make context switching less computationally expensive
## Processor Scheduling
To maximise CPU utilisation, most modern OS support [[Concurrency|concurrency]]

The [[processor scheduler]] selects the next process for the CPU to execute and maintains the [[scheduling queues]] of all current processes