TheBullyAlgorithm

Simulate the Bully election algorithm using any interprocess communication technology.

The program simulate the following scenarios:
    1: Initially, all processes start up, with each having a unique ID, and communication between each process starts,
        Each process should hear from the current coordinator at some predetermined interval (say every one second).

    2: When a process does not hear from the current coordinator for more than the specified time interval it will initiate election,
     (providing some way to let the user terminate the current Coordinator).

During this process i showed that:
    - the coordinator was shut down (as mentioned before,
     for the simulation purposes there should be a way to manually terminate the current coordinator) (a button to stop the selected process).
    - Elections will be initiated by processes that do not receive messages from coordinator 
     (more than one process will probably initiate elections once the coordinator goes down).
    - When a process receives an election request with a higher number than its, it should stop electing itself.

Initiating Elections
    - Elections initiated when the coordinator goes down or when system first starts.

Winning the Elections
    - Eventually the process with the highest number (id) wins an election.
    - The winning process will notify all the other running processes that it is the coordinator.
    - If a new process appears, it should initiate the election process. If it has the highest number, it wins the election.

 

Application Output:
    - You need to show the communication between processes except on processes that have been shut down.
    - Messages received at processes should be displayed with a receiving time stamps,
     the process number at which the message originated, and the type of the message (Ex. ELECTION, COORDINATOR ALIVE, …etc.).