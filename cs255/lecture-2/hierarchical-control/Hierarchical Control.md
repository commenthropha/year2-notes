### Description
In this model:
- Each controller sees the controllers below it as a “virtual” body from which it gets percepts and sends commands
- The lower level controllers perform simple computations and hence run faster
	- This allows them to react to the world more quickly as well as deliver a simpler view of the world to the higher level controllers