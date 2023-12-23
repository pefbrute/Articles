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

## Rules for passing Parameters for System Call
Following are the rules for passing parameters to the System Call:
- The OS pushes on or pops parameters off the stack.
- We can pass parameters in registers.
- In case parameters are more than registers, they are stored in a block. The block address is passed as a parameter to a register.

## Important System Calls Used in OS
Following are the important system calls used in an OS:

### 1. `wait()`
Когда процесс запущен, остальные процессы остаются в состоянии ожидания и ждут своей очереди. Это происходит, когда родительский процесс создает дочерний процесс, и родительский процесс приостанавливается до тех пор, пока дочерний процесс не завершится. Приостановка родительского процесса происходит автоматически с помощью системного вызова wait(). Управление возвращается к родительскому процессу после завершения выполнения дочернего процесса.

### 2. `fork()`
Этот системный вызов позволяет процессу создавать процессы копирования самого себя. Родительский процесс создает дочерний процесс. Это приостанавливает выполнение родительского процесса до тех пор, пока не выполнится дочерний процесс.

### 3. `exec()`
Этот системный вызов запускается, когда исполняемый файл заменяет старый, когда процесс еще работает. Хотя исходный идентификатор процесса все еще остается, поскольку старый процесс все еще выполняется, новый процесс заменяет такие вещи, как стек, данные, заголовок и т. д.

### 4. `kill()`
Этот системный вызов отправляет сигнал завершения процессу и призывает его завершить работу. Однако на самом деле это не убивает процесс, но может иметь различные значения.

### 5. `exit()`
Этот системный вызов завершает процесс. выполнение программы. Он определяет, что выполнение потока завершено и ОС может вернуть ресурсы, используемые процессом.

## Заключение
Системные вызовы предоставляют интерфейс между процессом и ОС. Некоторые из самых важных и используемых системных вызов, в ОС, это `wait()`, `fork()`, `exec()`, `kill()`, `exit()`.

| Категории |	Windows |	Unix |
| --- | --- | --- |
| Контроль Процесса |	CreateProcess(), ExitProcess(), WaitForSingleObject() |	fork(), exit(), wait() |
| Управление Устройствами |	SetConsoleMode(), ReadConsole(), WriteConsole() |	ioctl(), read(), write() |
| Управление Файлами |	CreateFile(), ReadFile(), WriteFile(), CloseHandle() |	open(), read(), write(), close() |
| Поддержка Информации |	GetCurrentProcessID(), SetTimer(), Sleep() |	getpid(), alarm(), sleep() |
| Коммуникация |	CreatePipe(), CreateFileMapping(), MapViewOfFile() |	pipe(), shm_open(), mmap() |
| Защита |	SetFileSecurity(), InitializeSecurityDescriptor(), SetSecurityDescriptor Group() |	chmod(), umask(), chown() |

Источник: "https://data-flair.training/blogs/system-call-in-os/"
Bc
