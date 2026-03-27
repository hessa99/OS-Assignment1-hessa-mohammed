# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:
A process is a stand-alone program that is running and has its own memory and system resources. Unless specific communication techniques are employed, each process operates independently and does not share memory with other processes. A thread, on the other hand, is a lightweight unit of execution that shares memory and resources with other threads in a process.

Because they have less overhead than processes, threads can be created and managed more quickly. Because the simulation required several processes to operate well in a shared environment, threads were used in this project. When mimicking CPU scheduling, using threads improves performance and speeds up context switching.
**



---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:
A process is preempted and placed at the end of the ready queue in Round-Robin scheduling if it does not complete within its time quantum. This ensures fairness and keeps any one process from controlling the CPU by allowing other processes to run. When the process gets back to the front of the queue, it will have another opportunity to run.
Example from my output:
P1 executing quantum [4000ms]
 P1 completed quantum 4000ms │ Overall progress: 80%
Remaining time: 962ms
 P1 yields CPU for context switch
 P1 (Priority: 1) added to ready queue
In this example, process P1 was given a time quantum of 4000ms but did not finish its execution because it still had 962ms remaining. As a result, the scheduler preempted P1 and placed it at the end of the ready queue. This behavior is clearly shown in the output where P1 is re-added to the queue. Later in the simulation, P1 gets another turn and finishes execution when it runs for the remaining 962ms.

**


---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:
1. **New**:  
P1 is in the New state when it is first created in the program before the scheduler starts execution. This happens when the process object and its thread are initialized but before the start() method is called.

2. **Runnable**:  
P1 enters the Runnable state after it is added to the ready queue, as shown in the output:
P1 (Priority: 1) added to ready queue
At this stage, P1 is waiting for the CPU to be assigned to it.

3. **Running**:  
P1 enters the Running state when the scheduler selects it and starts executing it:
P1 executing quantum [4000ms]
Here, P1 is actively using the CPU and performing its task.

4. **Waiting**:  
P1 enters a waiting-like state when the scheduler pauses it after its time quantum expires and before it gets CPU again. This is shown in the output:
P1 yields CPU for context switch
At this point, P1 is not running and is waiting in the ready queue for its next turn.

5. **Terminated**:  
P1 reaches the Terminated state when it finishes execution completely:
P1 finished execution!
This occurs after P1 runs again for its remaining 962ms and completes its burst time.

**
[When is P1 Terminated?]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:
Example 1: Handling Web Server Requests
Multiple client requests are handled concurrently by a web server, each of which is handled as a distinct thread. 

Why Round-Robin is effective in this situation: 
By giving each request a brief processing period before moving on to the next, Round-Robin guarantees equity. This enhances responsiveness and keeps additional requests from being blocked by a single request.

Example 2: Operating System Time Sharing 

Time-sharing is a feature of modern operating systems that enables several programs to run concurrently. 

Why Round-Robin is effective in this situation: 
Round-Robin scheduling ensures that no program is starving and the system stays responsive by allocating equal CPU time to all running apps. 

--- ## summary 
These questions helped me understand the following key concepts: 
1. The distinction between threads and processes 
2. How Round-Robin scheduling guarantees equity 
3. A thread's life cycle and states 
Ideas I should learn more about: 
1. Sophisticated synchronization of threads 
2. Optimizing scheduling algorithms' performance

**
