In direct message passing:
- Processes must name each other explicitly in system calls:
	`send(pid,msg)` and `receive(pid,msg)`
- Hard-coding PIDs like this isn't ideal as processes are typically assigned a new random ID each time they run
- Each link occurs between a specific pair of processes
	- There is a one-to-one relationship between processes
