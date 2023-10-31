# Constraint-Satisfaction Problems
## Notes
### Definition
A CSP is characterised by: 
- A set of *variables* {V1, V2, ..., Vn}
	- Each variable Vi has an associate *domain* D_Vi of possible values
	- Variables in a CSP are one of [[Types of CSP Variables|two types]]
- The existence of *hard constraints* for various subsets of the variables which specify legal combinations of values
- A solution to the CSP being an assignment of a value to each variable that satisfies all the constraints
#### For Optimisation Problems
- For optimisation problems, we instead have *soft constraints* and an associated *cost function* which describes the distance to constraint satisfaction
- An optimal solution is thus one which *minimises* the cost function
- Problems which contain a mix of hard and soft constraints are called *constrained optimisation problems*
	- As well as distinguishing between hard and soft constraints, we can further [[Types of CSP Constraints|categorise each constraint]]
### Examples of CSPs
- N-Queens Problem
- Crossword Puzzle
- Assignment Problems
- Timetable and Scheduling Problems
### Backtracking
A noteworthy brute-force approach to solving CSPs is the [[Generate-And-Test Algorithm|generate-and-test algorithm]]
- As the assignment space D has d^n elements, we would need to test d^n assignments and clearly trial-and-error would not be efficient
	- Instead, we can employ [[Backtracking Search|backtracking search]]
	- To further improve the efficiency of backtracking, we can implement a few [[Backtracking Heuristics|heuristics]]
### Structuring CSPs as a Graph
One way to characterise a CSP is as a [[CSP as Graph Searching|graph search problem]]
### Constraint Networks
A [[Constraint Network|constraint network]] is a model that serves as a way of representing a CSP in a graph structure
- This is usually what a question is referring to when it asks us to 'draw the constraint graph'
#### Advantages
The constraint network model allows us to enforce [[Consistency|consistency]]; the two types of consistency conditions are:
- [[Domain Consistency]] (For constraints involving a single variable i.e. unary constraints)
- [[Arc Consistency]] (For constraints involving more than one variable i.e. higher order constraints)

The idea behind enforcing consistency is that we can apply some pre-processing to the constraint network to eliminate assignments which will obviously not work
### Structuring CSPs as a Tree
If the [[Constraint Network|constraint network graph]] is a [[Trees|tree]] (or forest), the CSP can be solved in *O*(n • d^2) - much better than the general O(d^n) bound
#### Algorithm for Solving Tree-Structured CSPs
![[Pasted image 20231029115037.png]]
### Nearly Tree-Structured CSPs
A natural question is whether we can apply the efficiency improvements detailed for tree-structures CSPs to those which almost have a tree structure

To do this, we need to condition the data structure, by either using:
- [[Conditioning]]
- [[Cutset Conditioning]]
### Variable Elimination
Often, however it is the case that our [[Constraint Network|constraint network graph]] is neither tree-structured nor nearly tree-structured

In that case, we can use a method known as [[Variable Elimination|variable elimination]] to find a satisfying assignment and we do this *after* enforcing [[Consistency|consistency]] using [[Domain Consistency|domain consistency]] and [[Arc Consistency|arc consistency]]
## Question Approaches
- [[Backtracking Qs Approach]]