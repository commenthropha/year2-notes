The Critical Section Problem asks whether - given a set of processes - we can design a protocol which satisfies the following properties: 
1. Mutual Exclusion 
   - No two process can be simultaneously executing code in their [[Critical Section|critical sections]]. 
2. Progress 
   - At least one process is able to enter its [[Critical Section|critical section]] if no other process is in theirs. 
3. Bounded Waiting 
   - No one particular process must wait indefinitely to enter its [[Critical Section|critical section]].

Gary L. Peterson proposed [[Peterson's Algorithm|a solution]] to the Critical Section Problem in 1981, however all modern solutions to the problem are based on the idea of [[Locks|locks]]
