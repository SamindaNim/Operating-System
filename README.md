# Find PID (Process ID) in C

This program demonstrates how to create a child process using `fork()` and how to get the process ID (PID) of the current running process using `getpid()` in C.

---

## Introduction

In operating systems, a process is an executing program. Each process has a unique identifier called the Process ID (PID). The `fork()` system call creates a new process by duplicating the current one. The new process is called the child process. Both parent and child processes run the same program but have different PIDs.

This program prints "Hello World" and then creates a child process using `fork()`. It prints whether the current process is the parent or the child along with its PID.

---

## Code

```c
#include <stdio.h>
#include <unistd.h>

int main()
{
    printf("\nHello World\n");

    int f = fork();       // Create a new process (child)
    int p = getpid();     // Get current process ID

    if (f == 0)
    {
        // This block runs in the child process
        printf("\nI'm the child Process %d\n", p);
    }
    else
    {
        // This block runs in the parent process
        printf("\nI'm the parent Process %d\n", f);
    }

    return 0;
}
```
## Output

[2021ict62@fedora ~]$ vi Find_pid.c  
[2021ict62@fedora ~]$ gcc Find_pid.c -o Find_pid  
[2021ict62@fedora ~]$ ./Find_pid  
  
Hello World  
  
I'm the parent Process 18030  
I'm the child Process 18031  
