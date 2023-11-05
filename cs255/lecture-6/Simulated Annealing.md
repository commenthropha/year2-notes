A [[Stochastic Local Search]] technique that works in the following manner:
- Pick a variable at random, then a value at random
- If the value is an improvement, we always adopt it
- If not, we adopt it with some probability dependent on a *temperature value T*, which reduces over time
### Probability Formula
![[Pasted image 20231105110404.png]]