# Operating System Notes - Last Minute Revision :white_check_mark: 

Here we have last minute revision notes of Operating System. These questions will familiarize you with the most important operating system concepts and help you ace your job interviews :raised_hands:

## Most Asked Operating System Interview Questions

---

<img src="/assets/images/os-interview.png" width="400" height="200">

### What is an operating system?

It is a program that provides an interface between the software and hardware of a computer. In other words, an operating system offers an environment for the user to execute software using hardware.

- Your Application do not need interact directy with hardware, Applications talk to the operating system and operating systems talk with the hardware.

---

### Types of operating system?

According to the functionality that operating Systems provides the types are:

- Single Tasking System: This OS are very very basic. They do not provide multiple functionality they just exist in Ram. They are loaded in the ram then they allow only one processor to be there in the Ram at a time and to be run at a time.
    - Eg: MS-DOC



---

### What is the difference between multitasking and multiprocessing OS?

**Multitasking**: It is a system that allows more efficient use of computer hardware. This system works on more than one task at one time by rapidly switching between various tasks. These systems are also known as time-sharing systems. 

<img src="/assets/images/M-OS.png" width="400" height="200">

**Multiprocessing**: It is a system that allows multiple or various processors in a computer to process two or more different portions of the same program simultaneously. It is used to complete more work in a shorter period of time. 

<img src="/assets/images/Multiprocessing-OS.jpeg" width="400" height="200">

---

### What is Kernel? Explain the types of kernel.
The kernel is basically a computer program usually considered as a central component or module of OS. It is responsible for handling, managing, and controlling all operations of computer systems and hardware. Whenever the system starts, the kernel is loaded first and remains in the main memory. It also acts as an interface between user applications and hardware.

#### Types of Kernel:

Though there are many types of kernels, only two of them are the most popular:

**Monolithic Kernel**: In this type of OS kernel, all user and kernel services reside in the same memory space. Old operating systems would use this type of kernel. Some examples are Windows 95, 98, and Unix. Linux also uses it.

**MicroKernel**: This kernel type is small, and all the user and kernel services reside in different memory addresses. Operating systems like macOS and Windows use microkernels.

---

### Difference between Kernel and OS?

**Kernel**: Kernel is a system program that controls all programs running on the computer. The kernel is basically a bridge between the software and hardware of the system.

**Operating System**: Operating system is a system program that runs on the computer to provide an interface to the computer user so that they can easily operate on the computer.

<img src="/assets/images/os-kernel.png" width="400" height="200">

---

### What is a process? Name all the states of a Process

A process is a program in execution. when a program goes to RAM and start running then become a process.

<img src="/assets/images/process.png" width="600" height="200">

---

### What is a thread?

A thread is a lightweight process that shares the same memory space as the parent process. It allows multiple tasks to run concurrently within a single process.
Basically, It is a path of execution that is composed of the program counter, thread id, stack, and set of registers within the process.

---

### What is difference between process and thread?

| Process    | Thread    | 
| ------------- |-------------| 
| It is a computer program that is under execution.     | It is the component or entity of the process that is the smallest execution unit. | 
| These are heavy-weight operators.     | These are lightweight operators.    |  
| It has its own memory space. | It uses the memory of the process they belong to.     |  
| It is more difficult to create a process as compared to creating a thread. | It is easier to create a thread as compared to creating a process.    |  
| It takes more time to create and terminate a process as compared to a thread.   | It takes less time to create and terminate a thread as compared to a process.   |  
| It does not share data.    | It shares data with each other.   |  

---

### What is starvation and Aging?

**Starvation**: It is generally a problem that usually occurs when a process has not been able to get the required resources it needs for progress with its execution for a long period of time. In this condition, low priority processes get blocked and only high priority processes proceed towards completion because of which low priority processes suffer from lack of resources. 

**Aging**: It is a technique that is used to overcome the situation or problem of starvation. It simply increases the priority of processes that wait in the system for resources for a long period of time. It is considered the best technique to resolve the problem of starvation as it adds an aging factor to the priority of each and every request by various processes for resources. It also ensures that low-level queue jobs or processes complete their execution. 


---

### What is Context Switching?
Context switching is basically a process of saving the context of one process and loading the context of another process. It is one of the cost-effective and time-saving measures executed by CPU because it allows multiple processes to share a single CPU. This technique is used by OS to switch a process from one state to another i.e., from running state to ready state.

---

### Difference between preemptive and non-preemptive scheduling?

| Preemptive Scheduling | Non-Preemptive Scheduling   | 
| ------------- |-------------| 
| Processes are allocated to the CPU for a limited period. | A process remains in the CPU till it gets entirely executed. | 
| If a new process comes with high priority, then the ongoing CPU process must stop.    | Here the priority of the process does not matter. The new process has to wait until the first process finishes execution.    |  
| There is a continuous switching between the running and ready states of the processes. | This is not the case in non-preemptive scheduling. |  
| Preemptive schedules the process based on their priority. | Non-preemptive uses the process of burst time. |  
| There is a high probability that the process with less priority will starve.  | Here process with less burst time will starve.   |  

---

### What is a Scheduling Algorithm? Name different types of scheduling algorithms.

A scheduling algorithm is a process that is used to improve efficiency by utilizing maximum CPU and providing minimum waiting time to tasks. It is used to allocate resources among various competing tasks. 

Types of Scheduling Algorithm:

<img src="/assets/images/scheduling-algorithms.jpg" width="400" height="200">

#### 1. First Come First Serve (FCFS): 
FCFS is the simplest scheduling algorithm. The idea is the process that comes first will scheduled first. FCFS is a non preemptive (when you assign a process to a processor you can't take it back) process. FCFS can cause starvation problems in which the process does not get the proper resources.
#### 2. Shortest Job First: 
It could be preemptive or non-preemptive. In this algorithm, the process gets the CPU closest to its execution. Here, the CPU gives priority to those jobs which have a low execution time. so that other process do not have to wait for too long.
#### 3. Shortest Remaining Time First (SRT): 
Shortest Remaining Time is the preemptive version of Shortest Job First algorithm, where the processor is allocated to the job closest to completion. 
#### 4. Priority-Based Scheduling: 
It could be preemptive or non-preemptive. In this algorithm, Every job is assigned a priority and CPU is assigned to the highest priority job among all the jobs in the Ready queue.
#### 5. Round Robin Scheduling:
The Round robin scheduling algorithm is one of the CPU scheduling algorithms in which every process gets a fixed amount of time quantum to execute the process.

In this algorithm, every process gets executed cyclically. This means that processes that have their burst time remaining after the expiration of the time quantum are sent back to the ready state and wait for their next turn to complete the execution until it terminates. This processing is done in FIFO order which suggests that processes are executed on a first-come, first-serve basis.

Note: The CPU time quantum is the time period defined in the system.
#### 6. Multilevel Queue Scheduling
Multilevel queue scheduling is a type of CPU scheduling in which the processes in the ready state are divided into different groups, each group having its own scheduling needs. The ready queue is divided into different queues according to different properties of the process like memory size, process priority, or process type. All the different processes can be implemented in different ways, i.e., each process queue can have a different scheduling algorithm.


---

### What is a deadlock?

When two processes are trying to execute simultaneously and waiting for each other to finish the execution, as they depend on each other, this halt in execution is known as a deadlock. When a deadlock occurs in the program, the system usually freezes.

<img src="/assets/images/deadlock.png" width="400" height="200">

---

### What are the necessary conditions for a deadlock?

The necessary conditions for a deadlock are as follows:

- Mutual exclusion (Resources must be non shareable. e.g: printer)
- Hold and wait (Process must be holding one resource and waiting for other resource)
- No preemption (OS, assigned a resource to a process and can't take it back)
- Circular wait (process are waiting in circle for each other)

---

### What is process synchronization?
When the race condition occurs, it can lead to an undesirable outcome. So to prevent the race condition, we follow a process known as synchronization. Here, we ensure that only one process executes at a time.

---

### What is a critical section?
The program will behave oddly if program parts perform concurrent access to the shared resources. So to protect the shared resources of a program, we create a protected section known as the critical section or critical region. A critical section can only execute one process at a time, eliminating the problems concurrent accessing resources can cause.

---

### What do you mean by Semaphore in OS?

Semaphore is a synchronization mechanism that is used to control access to shared resources in multi-threaded or multi-process systems. It maintains a count of available resources and provides two atomic operations: wait() and signal(). It can have a count greater than one, allowing it to control access to a finite pool of resources.

#### Types of Semaphores

There are two main types of semaphores:

- **Binary semaphore**: A binary semaphore is a synchronization object that can only have two values: 0 and 1. It is used to signal the availability of a single resource, such as a shared memory location or a file.
- **Counting semaphore**: A counting semaphore is a synchronization object that can have a value greater than 1. It is used to control access to a finite number of resources, such as a pool of database connections or a limited number of threads.

---

### What do you know about mutex?

It is an abbreviation for **Mut** ual **Ex** clusion. It is a userspace program object that helps multiple threads to access the same resource, but not simultaneously. The sole purpose of a mutex is to lock a thread with a resource so the other threads can not use the same resource until the first thread finish executing.

<img src="/assets/images/Mutex-diagram.png" width="600" height="200">

---

### What is virtual memory?
Virtual memory is a technique that enables a computer to use more memory than it physically has by temporarily transferring data from the RAM to the hard disk. It provides a way to run large applications that require more memory than the system has.

---

### What is demand paging?
Demand paging is a concept used by a virtual machine. Only a part of the process needs to be present in the main memory to execute some process, meaning that only a few pages will be present in the main memory at any time, and the rest will be kept in the secondary memory.

---


### Differentiate between paging and segmentation?


| Paging | Segmentation | 
| ------------- |-------------| 
| Divides the virtual memory into physical memory.   | Divides the physical memory into logical memory. | 
| Paging divides the memory into fixed lengths.  | Segmentation divides the memory into arbitrary memory lengths.   |  
| Only loads information about the process. | Loads the entire logical portion of the page.     |  
| Pages are smaller than segments. | Segments are generally more significant.    |  
| It’s the hardware that divides the paging memory. | LThe software divides the segmentation memory.  |  

---

### What is cache memory?
It is a volatile computer memory directly attached to the register, which provides high-speed data access to the processor.

<img src="/assets/images/cache.png" width="500" height="200">

---

### What is a page in OS?
A page can be defined as the smallest unit of data, a fixed-length contiguous block of virtual memory.

---

### Explain page frames.
When a page is transferred from the secondary memory to the main memory, it requires a fixed length of a continuous physical memory block, known as a page frame. The operating system's job is to map the pages in the page frames.

---


### What is the difference between logical and physical addresses?

| Logical Address    | Physical Address   | 
| ------------- |-------------| 
| The CPU generates it.     | It is theactuall address of the program in the memory. | 
| A user can access the logical address of the program.  | The physical address can be accessed directly.    |  
| CPU generates a logical address at the execution time. | It is generated by the Memory Management Unit (MMU) at the creation time.     |  

---

### What is the page fault?
An error occurs when the CPU tries to access a specific block of memory address not present in the physical memory (RAM).

---

### What is thrashing?
It is a scenario when continuous page fault and paging activities occur. Thrashing could lead to a program collapse and degraded CPU performance.

---

### What is different between primary memory and secondary memory.
| Primary Memory    | Secondary Memory   | 
| ------------- |-------------| 
| Primary memory is temporary.    | Secondary memory is permanent. | 
| Primary memory is directly accessible by Processor/CPU.  | Secondary memory is not directly accessible by the CPU.    |  
| Nature of Parts of Primary memory varies, RAM- volatile in nature. ROM- Non-volatile. | It’s always Non-volatile in nature.    |  
| Primary memory devices are more expensive than secondary storage devices.   | Secondary memory devices are less expensive when compared to primary memory devices. | 


---

### What is Spooling?
Spooling is a process in which data is temporarily held to be used and executed by a device, program, or system. Data is sent to and stored in memory or other volatile storage until the program or computer requests it for execution.

---



### Thanks for Reading 

<img src="/assets/images/save.png" width="600" height="200">

**For any doubt, feel free to connect on Linkedin and Instagram**

> [Linkedin](https://www.linkedin.com/in/amanchowdhury046/) \
[Instagram](https://www.instagram.com/aman_chowdhury_046/)


















