## The Problem
![[Pasted image 20231031114446.png]]
## Intuitive Ideas
### Greedy Solution
Recall [[The Interval Scheduling Problem|the Interval Scheduling problem]] which worked with a greedy algorithm if all weights are 1

However, the algorithm fails if we use different weights for each job; observe:
![[Pasted image 20231031114720.png]]
### Binary Choice
#### Notation
![[Pasted image 20231031120154.png]]
#### Basic Idea
![[Pasted image 20231031120216.png]]
#### Implementations
##### Brute Force
###### Algorithm
![[Pasted image 20231031120242.png]]
###### Analysis
![[Pasted image 20231031120431.png]]
##### Memoization
###### Algorithm
![[Pasted image 20231031120620.png]]
###### Analysis
![[Pasted image 20231031120715.png]]
###### Finding a Solution
![[Pasted image 20231031121151.png]]
*Optimal Value* 
- The maximum total weight or value that can be achieved by selecting a non-overlapping set of intervals
- Answers the question "What is the maximum total value that can be obtained?"

*Solution*
- The specific set of non-ooverlapping intervals that achieves the optimal value
- Answers the question "Which intervals should be selected to maximize the total value?"
###### Bottom-Up Approach
An alternative approach to the one discussed previously:
![[Pasted image 20231031121406.png]]