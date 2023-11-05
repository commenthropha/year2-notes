Beam Search is similar to [[Parallel Search]], but at each step we choose the best c neighbours across all the individuals - that is, the best c globally rather than locally
- When c = 1, Beam Search acts the same as Greedy Descent
- When c = ∞, Beam Search acts the same as BFS

The value of c allows us to control the space complexity and parallelism.

A variant of beam search is [[Stochastic Beam Search|stochastic beam search]]