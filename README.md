# cs3113-Assignment2

Project Overview

This project provides an opportunity for students to experiment with process synchronization mechanisms in C, utilizing POSIX shared memory for inter-process communication. The objective is to create four child processes that independently increment a shared memory variable while ensuring synchronization through semaphores.

This program implements multiple child processes that share a variable named total. Each child attempts to increase total to specific targets: Process 1 increments to 100,000, Process 2 to 200,000, Process 3 to 300,000, and Process 4 to 500,000. When the program terminates, the shared memory variable will have a total of 1,100,000, printed by whichever of the four processes finishes last. The parent process waits for all children to finish, printing each child’s process ID upon completion. After all children have terminated, the parent releases the shared memory and semaphores, displaying "End of Program."

System Requirements

Operating System: Linux
Compiler: GCC
Development Environment: Visual Studio Code
Tools: GitHub (for version control)
Directory Structure
bash
Copy code
cs3113-Assignment2/
├── program.c          # Main implementation file
├── README.md          # Project documentation
└── [Other relevant files] # Any additional files if needed
Compilation and Execution Steps

Clone the Repository: Clone the project repository to your local machine.
Navigate to the Project Directory: Change your directory to the project folder.
Compile the Program: Use GCC to compile the source code. The -lpthread option is necessary for linking the pthread library, which is required for semaphore functions.
Run the Executable: Execute the compiled program.
Project Features

Concurrency: The project allows multiple processes to increment a shared counter concurrently.
Synchronization: Implements semaphores to manage access to shared memory and prevent race conditions.
Ordered Output: Ensures that outputs from child processes are printed in a specified order.
