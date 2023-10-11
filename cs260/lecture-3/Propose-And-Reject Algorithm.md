Also called the Gale-Shapley algorithm
### Pseudocode
```
Initialize each entity to be free. 

while (some doctor is free and hasn’t applied to every hospital) { 
	Choose such a doctor d 
	h = 1st hospital on d's list to which d has not yet applied 
	
	if (h is free) 
		assign d and h to be matched 
		
	else if (h prefers d to current match d') 
		assign d and h to be matched, and d' to be free 
	
	else 
		h rejects d 
}
```