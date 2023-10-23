### Definition
A consistent heuristic, h, is one that satisfies the **monotone restriction**: 

h(m) - h(n) ≤ cost(m, n) for any arc ⟨m, n⟩

- In other words, the heuristic is an underestimate locally as well as globally as the change in heuristic at each step is at most the cost at each step