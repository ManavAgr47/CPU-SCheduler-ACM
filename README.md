CPU Scheduling Algorithms
This project involves implementing various CPU scheduling algorithms in C++. Each algorithm determines how tasks are managed by the CPU, affecting the order and efficiency of task execution.

First Come First Serve (FCFS): FCFS schedules tasks based on their arrival time, where the task that arrives first is executed first. It's straightforward to implement and ensures fairness in task execution order, but it can lead to longer tasks causing delays for shorter ones.

Round Robin with varying time quantum (RR): RR allocates CPU time in equal slices (quantum) to each task, allowing each task to run for a specific time before moving to the next task in line. This method ensures fairness and prevents starvation of tasks waiting in the queue. However, longer tasks may not complete within one quantum, leading to delays.

Shortest Process Next (SPN): SPN prioritizes tasks based on their processing time, executing the shortest tasks first. This minimizes the waiting time for shorter tasks but can cause longer tasks to wait indefinitely if shorter tasks keep arriving.

Shortest Remaining Time (SRT): Similar to SPN, SRT prioritizes tasks based on their remaining processing time. It allows for preemptive scheduling, meaning a shorter task arriving later can interrupt a longer-running task. This ensures that shorter tasks are executed promptly but may lead to frequent context switches and overhead.

Highest Response Ratio Next (HRRN): HRRN prioritizes tasks based on a ratio of waiting time to estimated processing time. Tasks with higher response ratios are executed first, balancing fairness between short and long tasks. However, it can still result in longer tasks waiting if short tasks keep arriving.

Feedback (FB): FB uses multiple priority levels to manage tasks, where higher priority tasks are executed first. Tasks move to lower priority queues if they continue running, ensuring a mix of short and long tasks are processed. This method efficiently allocates CPU time based on task priority but is complex to implement and manage.

Feedback with varying time quantum (FBV): Similar to FB, FBV adjusts time slices (quantum) based on task priority. This ensures higher priority tasks receive more CPU time, optimizing efficiency. However, fine-tuning time slices is crucial to balancing fairness and performance.

Aging: Aging prevents tasks from waiting indefinitely by gradually increasing the priority of waiting tasks. This ensures that all tasks eventually receive CPU time, preventing starvation. It adds complexity to scheduling algorithms but ensures fairness in task execution.

Installation
To use these algorithms:

Clone the project repository.
Install the necessary compiler tools like g++ and make.
Compile the code using the make command.
Run the executable file to simulate and analyze CPU scheduling algorithms.
Input Format
Specify whether to trace or obtain statistical data.
Choose which scheduling algorithms to analyze and provide specific parameters.
Define the simulation duration and number of tasks.
For each task, provide details including name, arrival time, and either service time (for most algorithms) or priority (for Aging).
For more detailed examples and testing scenarios, refer to the provided test cases in the project repository.