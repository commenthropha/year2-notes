# Constraint-Satisfaction Problems
## Definition
A CSP is characterised by: 
- A set of *variables* {V1, V2, ..., Vn}
	- Each variable Vi has an associate *domain* D_Vi of possible values
	- Variables in a CSP are one of [[Types of CSP Variables|two types]]
- The existence of *hard constraints* for various subsets of the variables which specify legal combinations of values
- A solution to the CSP being an assignment of a value to each variable that satisfies all the constraints
### For Optimisation Problems
- For optimisation problems, we instead have *soft constraints* and an associated *cost function* which describes the distance to constraint satisfaction
- An optimal solution is thus one which *minimises* the cost function
- Problems which contain a mix of hard and soft constraints are called *constrained optimisation problems*
	- As well as distinguishing between hard and soft constraints, we can further [[Types of CSP Constraints|categorise each constraint]]
## Examples of CSPs
- N-Queens Problem
- Crossword Puzzle
- Assignment Problems
- Timetable and Scheduling Problems
## Backtracking
A noteworthy brute-force approach to solving CSPs is the [[Generate-And-Test Algorithm|generate-and-test algorithm]]
- As the assignment space D has d^n elements, we would need to test d^n assignments and clearly trial-and-error would not be efficient
	- Instead, we can employ [[Backtracking Search|backtracking search]]
	- To further improve the efficiency of backtracking, we can implement a few [[Backtracking Heuristics|heuristics]]
## CSP as Graph Searching
One way to characterise a CSP is as a [[CSP as Graph Searching|graph search problem]]