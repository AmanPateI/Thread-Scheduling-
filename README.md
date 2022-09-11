# Thread-Scheduling-
Multiprocessor operating system simulator pthreads for Linux
*Make sure that multiple CPU cores are enabled in your virtual machine

Implemented three CPU scheduling algorithms:

First In, First Out (FIFO) - Runnable processes are kept in a ready queue. FIFO is non-preemptive; once a process begins running on a CPU, it will continue running until it either completes or blocks for I/O.
Round-Robin - Similar to FIFO, except preemptive. Each process is assigned a timeslice when it is scheduled. At the end of the timeslice, if the process is still running, the process is preempted, and moved to the tail of the ready queue.
Longest Remaining Time First (LRTF) - The process with the longest remaining time in its burst always gets the CPU. Shorter processes must be pre-empted if a process that has a longer burst becomes runnable.

schedule() is the core function of the CPU scheduler. It is invoked whenever a CPU becomes available for running a process. schedule() must search the ready queue, select a runnable process, and call the context\_switch() function to switch the process onto the CPU.

pthreads will simulate an operating system on a multiprocessor computer. One thread per CPU and one thread as a 'supervisor' for the simulation. The CPU threads will simulate the currently-running processes on each CPU, and the supervisor thread will print output and dispatch events to the CPU threads.
