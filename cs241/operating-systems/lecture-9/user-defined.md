A user-defined signal handler can override the [[default]] handler
### Signal Safety
User-defined signal handlers should, typically, only call *signal-safe* functions
- This is to prevent a signal handler from interfering with the interrupted function
- Many functions which use of an internal buffer such as `printf` are *not* signal safe
![[Pasted image 20231105141258.png]]