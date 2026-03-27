# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - March 27, 2026, 5:00 PM
**What I did**: Set up the project environment and ran the initial code
**Details**:  
I started by setting up the development environment on my computer. I opened the project in VS Code and checked if Java was properly installed. After that, I updated the student ID in the code. Then, I compiled and ran the program for the first time to observe how the CPU scheduler simulation works. The program executed successfully and displayed the processes along with their burst times and scheduling behavior.
**Challenges**:  
Initially, I faced an issue where the Java compiler was not recognized in the terminal. This prevented me from compiling and running the program.
**Solution**:  
I installed the JDK and configured the environment variables correctly by setting the PATH. After restarting the terminal, the issue was resolved, and I was able to run the program successfully.
**Time spent**: 45 minutes
---


### Entry 2 - March 27, 2026, 6:00 PM
**What I did**: Analyzed the Round-Robin scheduling behavior
**Details**:  
I focused on understanding how the Round-Robin algorithm is implemented in the code. I carefully examined the ready queue and how processes are added and removed from it. I ran the program multiple times and observed how each process gets a fixed time quantum (4000ms) and how unfinished processes are moved back to the queue. I also paid attention to the order of execution and how fairness is maintained among all processes.
**Challenges**:  
It was confusing at first to track the movement of processes in the ready queue, especially when multiple processes were being re-queued after not finishing their execution.
**Solution**:  
To solve this, I followed one process (P1) step by step through the output and traced its execution cycle. This helped me clearly understand how the scheduling works.
**Time spent**: 1 hour
---


### Entry 3 - March 27, 2026, 7:00 PM
**What I did**: Implemented Feature 1 (Process Priority)
**Details**:  
I added a new attribute called priority to the Process class. I generated random priority values between 1 and 5 for each process. Then, I modified the output so that each process displays its priority when added to the ready queue. I tested the program again and confirmed that priorities were correctly assigned and displayed without affecting the scheduling behavior.
**Challenges**:  
The main challenge was deciding where exactly to add the new attribute and ensuring that it integrates smoothly with the existing code without breaking anything.
**Solution**:  
I carefully analyzed the structure of the Process class and added the new attribute in the appropriate place. I also tested the program after each change to ensure stability.
**Time spent**: 1 hour
---


### Entry 4 - March 27, 2026, 8:00 PM
**What I did**: Implemented Feature 2 (Context Switch Counter)
**Details**:  
I added a counter to track how many times the CPU switches between processes. I incremented the counter each time a new process starts execution. After implementing this feature, I displayed the total number of context switches at the end of the program. I verified the output and confirmed that the count increases correctly during execution.
**Challenges**:  
It was a bit tricky to determine the correct place to increment the counter to ensure accurate counting of context switches.
**Solution**:  
I placed the increment statement right before each process execution inside the scheduling loop. This ensured that every switch is counted correctly.
**Time spent**: 1 hour
---


### Entry 5 - March 27, 2026, 9:00 PM
**What I did**: Implemented Feature 3 (Waiting Time) and performed final testing
**Details**:  
I implemented waiting time tracking for each process by recording the creation time and calculating how long each process waits before execution. I added code to update the waiting time whenever a process starts running. After that, I printed a summary table at the end of the program showing each process’s burst time and waiting time. Finally, I tested the entire program thoroughly to ensure all features work together correctly.

**Challenges**:  
The most difficult part was calculating the waiting time accurately, especially when processes are paused and resumed multiple times.
**Solution**:  
I used System.currentTimeMillis() to track time precisely and updated the waiting time incrementally. I tested the program multiple times to confirm the correctness of the results.
**Time spent**: 1.5 hours
---


## Summary
**Total time spent on assignment**: 6 hours  
**Most challenging part**:  
The most challenging part was understanding the internal behavior of the Round-Robin scheduler and tracking how processes move between execution and waiting states. Additionally, implementing the waiting time calculation correctly required careful attention.
**Most interesting learning**:  
The most interesting part was seeing how CPU scheduling works in practice and how the system ensures fairness between processes. It was insightful to observe how context switching and time slicing affect performance.
**What I would do differently next time**:  
Next time, I would start earlier and break the work into smaller tasks from the beginning. I would also add more debugging outputs early on to better understand the program behavior.

