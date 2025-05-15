# Kernel

* What is the main purpose of inventing computer?

  - To run the sequence of instructions which is known as program
  - The program is often referred as Process

* If you look back the history, single computer were used to run single process

* later general purpose computers are designed to run many processes simultaneously, but how its been achieved?

* In general – what is required for process

    - It requires hardware resources such are Memory, Processor time, Storage space, etc

* To run many processes simultaneously, we need middle layer to manage the distribution of hardware resources of the computer efficiently & fairly among all the various processes running on the computer

* This middle layer is referred to as the `kernel`

* Basically the kernel virtualizes the common hardware resources of the computer to provide each process with its own virtual resources.

* This makes the process seem as it is the sole process running on the machine

* The kernel is also responsible for preventing & mitigating conflicts between different processes

![alt text](../images/picture1.png)