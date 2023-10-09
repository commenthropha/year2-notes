## Definition
A scheduling queue is a list of processes waiting to be executed. Each queue potentially has it's own scheduler.
### Job Queue
Contains processes in the [[New Process|new]] state and is processed by the [[Long-Term Scheduler]]
### Ready Queue
Contains processes in the [[Ready Process|ready]] state and is processed by the [[Short-Term Scheduler]]
### Device (IO) Queue(s)
Contains processes in the [[Waiting Process|waiting]] state (i.e. those waiting for an IO signal)

When a process is done waiting it returns to the ready queue
## Diagram
![[Pasted image 20231009091204.png]]