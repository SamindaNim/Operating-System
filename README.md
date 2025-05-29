#  Signal Handling in C

This is a simple C program that demonstrates **signal handling** using the `signal()` function. It handles the `SIGINT` signal (triggered by pressing `Ctrl+C`) to exit gracefully.

##  Features

- Handles `SIGINT` (Ctrl+C)
- Shows how to use `signal()` in C
- Prints a custom message before exiting

##  Code

```c
#include <stdio.h>
#include <signal.h>
#include <unistd.h>

// Function to handle SIGINT (Ctrl+C)
void handle_sigint(int sig) {
    printf("\nCaught signal %d (SIGINT). Exiting gracefully...\n", sig);
    _exit(0); // Exit the program
}

int main() {
    // Register signal handler for SIGINT
    signal(SIGINT, handle_sigint);

    while (1) {
        printf("Running... Press Ctrl+C to stop.\n");
        sleep(1); // Wait for 1 second
    }

    return 0;
}
```
## Output Example  
  
$ gcc signal_handler.c -o signal_handler  
$ ./signal_handler  
Running... Press Ctrl+C to stop.  
Running... Press Ctrl+C to stop.  
^C  
Caught signal 2 (SIGINT). Exiting gracefully...  
