# XV Quiz (CSL 3030)

Welcome to the XV Quiz for CSL 3030 - Operating Systems!



## Instructions
- Answer the multiple-choice questions by selecting the correct option.
- For theoretical questions, provide concise and accurate explanations.
- Feel free to use this quiz for self-assessment or educational purposes.

## Multiple-Choice Questions

#### Question 1: Basics
1. What is XV6?
   - a. A programming language
   - b. A Unix-like operating system
   - c. A file system
   - d. An assembly language


#### Question 2: Architecture
2. XV6 is based on which earlier operating system?
   - a. Windows
   - b. Linux
   - c. BSD
   - d. DOS



#### Question 3: File System
3. Which file system is used in XV6?
   - a. FAT32
   - b. NTFS
   - c. ext4
   - d. simple


#### Question 4: System Calls
4. How are system calls implemented in XV6?
   - a. As functions in the C standard library
   - b. As interrupts
   - c. Through the command line
   - d. As external programs


#### Question 5: Processes
5. In XV6, what is the maximum number of processes that can run simultaneously?
   - a. 128
   - b. 256
   - c. 512
   - d. 1024


#### Question 6: Shell
6. What is the name of the shell used in XV6?
   - a. Bash
   - b. Zsh
   - c. Sh
   - d. Fish


#### Question 7: Scheduling
7. How does XV6 handle process scheduling?
   - a. Round-robin scheduling
   - b. Priority-based scheduling
   - c. First-Come-First-Serve (FCFS)
   - d. Random scheduling


#### Question 8: Memory Management
8. Which memory management technique is used in XV6?
   - a. Paging
   - b. Segmentation
   - c. Virtual Memory
   - d. None of the above


#### Question 9: Interrupts
9. How are interrupts handled in XV6?
   - a. Through polling
   - b. Using hardware interrupts
   - c. Using software interrupts
   - d. Both b and c


#### Question 10: Multithreading
10. Does XV6 support multithreading?
    - a. Yes
    - b. No


#### Bonus Question:
11. Who developed XV6?
    - a. Microsoft
    - b. Google
    - c. MIT
    - d. IBM


## Theoretical Questions

#### Question 12: Process States
12. Briefly explain the different states a process can be in within the XV6 operating system.

#### Question 13: File System Structure
13. Describe the structure of the file system in XV6. Include the key components and their roles.

#### Question 14: System Calls vs. Library Functions
14. Explain the difference between system calls and library functions in the context of XV6. Provide examples of each.

#### Question 15: Memory Paging
15. How does memory paging work in XV6? Discuss the benefits of using paging in memory management.

#### Question 16: Shell Commands
16. Name and briefly explain three essential shell commands in the XV6 operating system.

#### Question 17: Process Synchronization
17. Discuss the concept of process synchronization in XV6. Why is it essential, and what mechanisms are used to achieve it?

#### Question 18: Interrupt Handling
18. Explain the role of interrupts in the XV6 operating system. How are interrupts handled, and what is their significance in system operation?

#### Question 19: Virtual Memory
19. What is virtual memory, and how is it implemented in XV6? Discuss the advantages of using virtual memory.

#### Question 20: Boot Process
20. Outline the steps involved in the boot process of XV6. What happens from the moment the computer is powered on to when the XV6 kernel is loaded into memory?

## Answers
Please write your answers here

Ans 1: b. A Unix-like operating system
Ans 2: c. BSD
Ans 3: d. simple
Ans 4: b. As interrupts
Ans 5: a.128
Ans 6: c.Sh
Ans 7: a. Round-Robin scheduling
Ans 8: a.Paging
Ans 9: d. Both b and c
Ans 10: b. No
Ans 11: c. MIT

Ans 12:

These are the following states of processes in xv6:

UNUSED: Not yet in use.
EMBRYO: Being created or initialized.
SLEEPING: Present in sleep/idle state.
RUNNABLE: Ready to execute, but waiting for the CPU.
RUNNING: Currently being executed.
ZOMBIE: Completed execution but it still has an entry in the process table

Ans 13:

In xv6, the hierarchical file system resembles Unix, incorporating directories and files. Inodes serve as metadata containers, storing information about files and the locations of their data blocks. This structure enables efficient management and retrieval of file-related data in the operating system.

Ans 14:

A system call is a request made by the program to switch from user mode to kernel mode to access a process. 
Eg. fork() , open()
A library call is a request made by the program to access a library function defined in a programming library. 
Eg printf() , malloc()

Ans 15:

Memory in xv6 is managed in pages (and frames) where each  page is 4MB in size. Memory is divided into pages of fixed-size.
Each process has its own page table which is used to translate virtual to physical addresses.
Benefits of paging include:

- Since memory of each page is fixed , external fragmentation is reduced.
- Paging also allows the user to increase degree of multiprogramming

Ans 16:

Three shell commands in xv6:

- ls : shows the contents of the current directory
- mkdir : creating a directory
- cd : changing the current directory

Ans 17:

Process synchronization is used to ensure orderly execution of concurrent processes, preventing race conditions and data inconsistencies. Mechanisms like locks, semaphores, and condition variables are employed for synchronization. Locks provide mutual exclusion, ensuring that only one process can access a critical section at a time, while semaphores enable control over access to resources.  These mechanisms collectively maintain the integrity of shared resources and foster cooperation among concurrent processes in xv6.

Ans 18:

When an interrupt occurs, the CPU transfers control to a designated interrupt handler, preserving the system's responsiveness and enabling efficient multitasking. xv6 manages interrupts through an interrupt descriptor table (IDT), directing each interrupt to its corresponding handler. This mechanism allows the operating system to handle events like I/O operations or timer ticks promptly, enhancing overall system efficiency and responsiveness.

Ans 19:

xv6 utilizes virtual memory, providing each process with the illusion of a dedicated address space. Virtual memory allows for process isolation and memory protection, enhancing system stability.