### How It Works
After a `fork()`, the program is concurrently executed by both parent and child process

- If successful, `fork()` creates a child process and returns its (stricly positive) [[Process Identifier (PID)|PID]] to the parent
- If unsuccessful, it returns a negative value

We can use these return values to execute different code in the parent and child processes:
``` c
int main() { 
	pid_t pid; // This initializes the pid to 0 
	pid = fork(); 
			
	if (pid < 0) printf("Could not create child process\n"); 
	else if (pid > 0) printf("Created child process\n"); 
	else { 
		// Child code 
		execlp(...); // Load new program 
	} 
}
```