# Системные Вызовы в ОС

Мы используемые системные вызовы, чтобы предоставить интерфейсы между процессом и ОС.
Системный запрос помогает процессу запрашивать services from kernel. It is a programmatic method and the only entry point for the kernel system. These services are offered with the help of an API (Application Programming Interface).

## Introduction to System Call

### Workings of a System Call in OS
Following are the steps on how a System Call works:
Step 1: The processor executes a process in the user mode until a system call interrupts it.
Step 2: Then on a priority basis, the system call is executed in the kernel mode.
Step 3: After the completion of system call execution, control returns to user mode.,
Step 4: The execution resumes in Kernel mode.

### Need for System Calls
Following are the reasons we need system calls:

To read and write from files.
To create or delete files.
To create and manage new processes.
To send and receive packets, through network connections.
To access hardware devices.

### Services of System Call in Operating System
Following are the services provided by a system call:

Manages main memory
Helps access files and directories and manages the file system.
Creates and manages new processes
I/O device handling
Provides system protection
Types of System calls in Operating System
The five types of System Calls are:

1. Process Control
It performs the tasks of process creation, process termination, etc.

Functions of process Control:

End and Abort
Loading and Execution of a process
Creation and termination of a Process
Wait and Signal Event
Allocation of free memory
2. File Management
Technology is evolving rapidly!
Stay updated with DataFlair on WhatsApp!!

It handles jobs regarding file manipulation.

Functions of File Management:

Creation of a file
Deletion of a file
Opening and closing of a file
Reading, writing, and repositioning
Getting and setting file attributes
3. Device Management
It helps in device manipulation like reading from device buffers, writing into device buffers, etc.

Functions of Device Management:

Requesting and releasing devices
Attaching and detaching devices logically
Getting and setting device attributes
4. Information Maintenance
It handles information and information transfer between OS and the user program.

Functions of Information maintenance:

Getting or setting time and date
Getting process and device attributes
5. Communication
This is for interprocess communications.

Functions of interprocess communication:

Creation and deletion of communications connections
Sending and receiving messages
Helping OS transfer status information
Attaching or detaching remote devices
Rules for passing Parameters for System Call
Following are the rules for passing parameters to the System Call:

The OS pushes on or pops parameters off the stack.
We can pass parameters in registers.
In case parameters are more than registers, they are stored in a block. The block address is passed as a parameter to a register.
Important System Calls Used in OS
Following are the important system calls used in an OS:

1. wait()
When a process is running, the rest of the processes stay in the waiting state and wait for their turn. This happens when a parent process creates a child process, and the parent process suspends until the child process is done executing. This suspension of the parent process occurs automatically with the help of the wait() system call. Control moves back to the parent process after the child process ends execution.

2. fork()
This system call allows a process to create copy processes of itself. A parent process creates a child process. This suspends the execution of the parent process until the child process executes.

3. exec()
This system call runs when an executable file replaces the older one when the process is still running. Though the original process identifier still remains as the old process is still executing, the new process replaces things like a stack, data, head, etc.

4. kill():
This system call sends a termination signal to a process and urges the process to exit. However, it doesn’t really kill a process but can have various meanings.

5. exit():
This system call terminates a process. program execution. It defines that the thread execution is complete and the OS can reclaim the resources used by the process.

## Summary
System calls provide an interface between a process and an OS. Some important system calls used in OS are wait(), fork(), exec(), kill(), exit().

| Categories |	Windows |	Unix |
| Process control |	CreateProcess(), ExitProcess(), WaitForSingleObject() |	fork(), exit(), wait() |
| Device manipulation |	SetConsoleMode(), ReadConsole(), WriteConsole() |	ioctl(), read(), write() |
| File manipulation |	CreateFile(), ReadFile(), WriteFile(), CloseHandle() |	open(), read(), write(), close() |
| Information maintenance |	GetCurrentProcessID(), SetTimer(), Sleep() |	getpid(), alarm(), sleep() |
| Communication |	CreatePipe(), CreateFileMapping(), MapViewOfFile() |	pipe(), shm_open(), mmap() |
| Protection |	SetFileSecurity(), InitializeSecurityDescriptor(), SetSecurityDescriptor Group() |	chmod(), umask(), chown() |
