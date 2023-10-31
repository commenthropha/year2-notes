This question is usually given with reference to a search tree or a constraint graph

Lay the solution out as a table with the following columns:
- Step number (1, 2, ...)
- Current assignment, initially empty
- Chosen assignment in this round (i.e. variable = value)
	- This is added to the current assignment column in following rounds
- Pruned
	- Keeps track of an assignment set that doesn't work

Rule used to choose the assignment:
1. First use MRV to choose a variable
2. Use degree heuristic as a tiebreaker if there are multiple variables with the same number of remaining values
3. Use LCV to choose a value

If you run into a dead end before you get a complete assignment:
- Prune the path
- Backtrack through your assignments
- Keep trying different choices