# CS153 Labs

## Lab 1

* Change the exit system call signature to <void exit(int status)>. The exit system call must act as previously defined (i.e., terminate the current process) but it must also store the exit status of the terminated process in the corresponding structure.

* Update the wait system call signature to int <wait(int *status)>. The wait system call must prevent the current process from execution until any of its child processes is terminated (if any exists) and return the terminated child exit status through the status argument.

* Add a waitpid system call: <int waitpid(int pid, int *status, int options)>. This system call must act like wait system call with the following additional properties: The system call must wait for a process (not necessary a child process) with a pid that equals to one provided by the pid argument. The return value must be the process id of the process that was terminated or -1 if this process does not exist or if an unexpected error occurred. We are required only to implement a blocking waitpid where the kernel prevents the current process from execution until a process with the given pid terminates.

