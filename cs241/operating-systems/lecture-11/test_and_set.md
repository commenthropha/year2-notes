### Functionality
The `test_and_set` instruction takes the memory address of some boolean variable, sets the value of the variable to true, then returns the original value of the variable.
### Illustrative Examples
We can describe `test_and_set` with the following C code:
```c 
/* Return the original value of target and set its new value to TRUE */ 
boolean test_and_set (boolean *target) { 
	boolean rv = *target; 
	*target = TRUE; 
	return rv: 
}```

Using the above description, we can implement a simple synchronised thread function:
```c
/* shared variable */ 
bool lock=false; 

do { 
	while (test_and_set(&lock)){
		/* do nothing */
	}
	/* critical section */ 
	lock = false; 
	/* remainder section */ 
} while (true);
```
However, this does not satisfy **Bounded Waiting** as the same process can keep re-acquiring the same lock, forcing other processes to wait indefinitely.

Below is a better solution using `test_and_set`:
```c
/* shared variables */ 
bool waiting[n]; // initially all false 
bool key = false; 

do { 
	/* stores the wish to enter CS */
	waiting[i] = true;  
	/* stores the status of the lock */
	key = true;  
	
	/* keep waiting and checking the lock status */ 
	while (waiting[i] && key) {
		key = test_and_set(&lock);
	} 
	
	waiting[i] = false; 
	
	/* critical section */ 
	
	/* find the next waiting process*/ 
	j = (i + 1) % n; 
	while ((j != i) && !waiting[j]) {
		j = (j + 1) % n;
	} 

	/* if not found release lock */ 
	if (j == i) { 
		lock = false;
	} 
	/* if found make it non-waiting */
	else { 
		waiting[j] = false;
	}  /* remainder section */ 
} while (true);
```
In this solution, the same process does not re-acquire the lock unless no other processes are waiting, hence satisfying the **Bounded Waiting** principle.