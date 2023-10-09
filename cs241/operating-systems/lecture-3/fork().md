### How It Works
After a `fork()`, the program is concurrently executed by both parent and child process
- Both processes continue running from the `fork()` onwards
	- The child process uses the universal`PC` value to determine where to continue running from (which is copied alongside the other contents)
- If successful, `fork()` creates a child process and returns its (strictly positive) [[Process Identifier (PID)|PID]] to the parent
- If unsuccessful, it returns a negative value

We can use these return values to execute different code in the parent and child processes:
``` c
int main() { 
	pid_t pid; // This initializes the pid to 0 
	pid = fork(); 
			
	if (pid < 0) {
		printf("Parent: Creating a child process");
	}
	if (pid==0) { // child runs this
		execlp('./prime','prime',NULL,NULL);
	}
	
	if (pid > 0) { // parent runs this
		wait(NULL);
		printf("Parent: Child has finished executing")
	} 
}
```