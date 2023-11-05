An algorithm proposed by Gary L. Peterson in 1981 to solve [[The Critical Section Problem|the Critical Section Problem]]
### Algorithm
![[Pasted image 20231105150511.png]]
### Evaluation
#### Merits
- It fulfils all three criteria outlined by [[The Critical Section Problem|the Critical Section Problem]]
#### Flaws
- It employs busy-wait, which is a waste of resources
- It may fail in modern architectures, where independent read and write operations (i.e. to the `flag` and `turn` variables) may be reordered
	- The image below demonstrates **Mutual Exclusion** being broken when this occurs![[Pasted image 20231105150917.png]]	


