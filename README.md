# Dining Philosophers
Implementation of a solution for a modified version of the famous dining philosophers problem using Java threads, semaphores and barriers.
## Problem Description
  Here’s a short description of the problem: We have five forks, five plates and our five philosophers. At the beginning, philosophers are not at the table and they need to walk towards table. One philosopher can walk faster or slower than another philosopher, because of that philosophers must walk towards the table for a random amount of time, between 1 to 10 seconds. After reaching to the table, a philosopher must put his plate on   the table and must wait for other philosophers. When five philosophers sit around the table, they can startdining.
  When dining, these philosophers can either think or eat. In order to eat, they need two forks, the one on their left and the one on their right. If the forks are available, they start eating; otherwise they need to wait until both forks are available.  Due to different scenarios these philosophers may be *deadlocked* or they might *starve*. We need an algorithm to avoid these situations.
  More detailed info about the project description can be found in [here](https://github.com/bubblecounter/diningPhilosophers/blob/master/Project%20Description.pdf)
  
## Implementation Details
  We have five Java threads, one for each philosopher. While a philosopher waits other philosophers, the thread of the philosopher is blocked until other philosophers arrive to the table. To achieve this, i implemented a *Barrier* for 5 threads and users semaphores to prohibit *deadlock* and *starvation* scenarious
  
## Sample run
![Sample Run](https://github.com/bubblecounter/diningPhilosophers/blob/master/sampleRun.gif)
