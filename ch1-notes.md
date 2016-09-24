# Computer Organization and Design: The Hardware/Software Interface
###### By David A. Patterson & John L. Hennessy

## Chapter 1

##### Embedded Computer
* a computer inside another device used for running one predetermined application or collection of software

##### Cloud Computing
* refers to large collections of servers that provide services over the internet
* some providers rent dynamically varying numbers of servers as a utility 

##### Software-as-a-Service (SaaS)
* delivers software and data as a service over the Internet, usually via a thin program such as a browser that runs on local client devices
    - as opposed to binary code that must be installed and runs wholly on the local device
* examples include: web search apps and social networking

##### Moore's Law
* states that integrated circuit resources double every 18-24 months
* resulted from a 1965 prediction made by Gordon Moore (one of the founders of Intel)

##### Pipelining
* a very prevalent pattern of paralellism, running programs faster by overlapping the execution of instructions
* simliar to the 'human-chain' approach used in putting out a fire (think old west movies)
* an example of _instruction-level paralellism_
    - the parallel nature of the hardware is abstracted away so the programmer and compiler can think of the hardware as executing instructions sequentially

##### Hierarchy of Memories
* a way of looking at the available memory as a pyramid
* fastest, smallest, and most expensive memory is at the top
* slowest, biggest, and cheapest memory makes up the bottom of the pyramid

##### Abstraction
* to go from a complex application to the simple instructions a computer understands involves several layers of software that interpret or translate high-level operations, providing abstraction

##### Systems Software
* the layer of software (abstraction) between Applications software and the Hardware itself
    - include operating system and compiler
        + an **Operating System** manages the resources of a computer for the benefit of programs that run on that computer
        + a **Compiler** translates high-level code into instructions the hardware can execute

##### Binary Digit
* one of the two numbers in base 2 (0 or 1) that are the components of information
    - also called a **bit**
* using numbers to represent instructions _and_ data is a foundation of computing

##### Assembly Language
* a symbolic representation of machine instructions
* created by early programmers who were tired of writing in binary
* a great improvement over binary, but requires one line for each instruction given
    - forces the programmer to think like a computer

##### Machine Language
* a binary representation of machine instructions

##### Assembler
* a program that translates a symbolic version of _instructions_ into the binary version
    - assembly language -> machine language
    - add A,B -> 1000110010100000

##### High-Level Programming Language
* a portable language such as C, C++, Java, or Visual Basic that is composed of words and algebraic notation
* allows programmeers to think in a more natural, human-like language
* allows programs to be developed independant of the computer on which they were developed
* languages can be designed according to their intended use
* can be translated by a compiler into assembly language
    - C++ -> Assembly language
    - A + B -> add A,B

##### Input Device
* a mechinism through which the computer is fed information, such as a keyboard

##### Output Device
* a mechanism that conveys the result of a computation to a user, such as a display, or to another computer

##### Active Matrix Display
* a **liquid crystal display** using a transistor to control the transmission of light at each individual pixel
    - has a tiny transistor switch for each **pixel**
    - _LCD_ screens use a thin layer of liquid polymers that are used to transmit or block light according to whether a charge is applied
        - not the source of light, but controls the transmission of it

##### Pixel
* the smallest individual picture element
* many color displays use 8 bits for each color (red, green, blue) for a total of 24 bits per pixel
* screens are composed of hundred of thousands to millions of pixels, organized in a matrix
    - this matrix is called a **bit map**
    - **frame buffers** contain upcoming images, as bit maps, to be displayed onscreen

##### Integrated Pixel
* a device combining dozens to millions of transistors, also called a **chip**

##### Cetral Processor Unit
* the active part of the computer
* contains the _datapath_ and _control_, which adds numbers, tests them, signals I/O devices, etc
* also called the **processor**

##### Datapath
* the component of the _processor_ that performs arithmetic operations

##### Control
* the component of the _processor_ that commands the datapath, memory, and I/O devices according to the instructions of the program

##### Memory
* the storage area in which programs are kept when they are running
* also contains the data needed by the running programs

##### Dynamic Random Access Memory _(DRAM)_
* a volatile type of **memory** built as an integrated circuit
* provides random access to any location (access times don't depend on data location)
* access times are fast, about 50 nanoseconds

##### Static Random Access Memory _(SRAM)_
* also memory built as an integrated circuit, but faster and less dense than _DRAM_
* more expensive than _DRAM_

##### Cache Memory
* a small, fast memory that acts as a buffer for slower, larger memory

##### Instruction Set Architecture
* also called _architecture_
* an abstract interface between the hardware and the lowest-level software
* enables many _implementations_ of varying cost and performance to run identical software
* encompases all the information necessary to write a machine language program
    - including instructions, registers, memory accesss, I/O, etc

##### Application Binary Interface _(ABI)_
* the user portion of the _instruction set architecture,_ plus the operating system interfaces used by application programmers
* defines the standard for binary portability across computers

##### Implementation
* hardware that obeys the architecture abstraction

##### Volatile Memory
* storage, such as DRAM, that retains data _only if it is receiving power_
* typically called **main** or **primary memory**

##### Nonvolatile Memory
* a form of memory that retains data even in the absence of a power source
* used to store programs between runs
* a DVD disk would be an example of nonvolatile storage
* often referred to as **secondary memory**

##### Magnetic Disk 
* a form of nonvolatile, secondary memory
* composed of rotating platters coated with a magnetic recording material
* access times are slow due to moving parts, about 5 to 20 milliseconds
* also called a **hard disk**

##### Flash Memory
* a nonvolatile semiconductor memory
* cheaper and slower than _DRAM_
* faster and more expensive than _hard disks_
* access times are about 5 to 20 microseconds

##### Transistor
* an on/off switch controlled by an electronic signal

##### Integrated Circuit
* a chip combining dozens to hundreds of _transistors_ onto a single chip
* **very large-scale** integrated circuits contain hundreds of thousands to millions of transistors

##### Semiconductor
* a substance that does not conduct electricity well

##### Silicon
* a natural element that is a _semiconductor_
* through a chemical process, tiny areas are transformed into one of the following:
    1. excellent conductors of electricity (using microscopic copper or aluminum wire)
    2. excellent insulators of electricity (like plastic sheathing or glass)
    3. areas that can conduct or insulate under certain conditions (as a switch)

##### Silicon Crystal Ingot
* a rod composed of _silicon_
* typically between 8 and 12 inches in diameter, and about 12 to 24 inches long
* the beginning piece in manufacturing an integrated circuit

##### Wafer
* a slice from a _silicon crystal ingot_ no more than .1 inches thick
* patterns of chemicals are applied to the wafer, creating transistors, conductors, and insulators
* a single microscopic flaw, or **defect** will render that part of the wafer unusable

##### Die
* the individual rectangular sections that are cut from a wafer
* more informally known as **chips**

##### Yield
* the percentage of good _dies_ from the total number of dies on the _wafer_

##### Response Time
* the total time required for a computer to complete a task
    - including disk accesses, memory accesses, I/O activities, operating system overhead, and so on
* typically measured in seconds per program
* also called **execution time** 

##### Throughput
* another measure of performance, the number of tasks completed per unit of time
* also called **bandwidth**

##### CPU Execution Time
* the actual time the CPU spends computing for a specific task
* **User CPU Time**
    - the CPU time spent in a program itself
* **System CPU Time**
    - the CPU time spent in the operating system performing tasks on behalf of the program

##### Clock Cycle
* the time it takes for one _clock period_
* a **clock period** is the length of each _clock cycle_

##### Clock Cycles per Instruction
* average number of clock cycles per instruction for a program or program fragment

##### Instruction Count
* the number of instructions executed by the program
* basic performance equation can be written in terms of:
    - **CPU Time = Instruction Count x CPI x Clock Cycle Time**

##### Instruction Mix
* a measure of the dynamic frequency of instructions accross one or many programs

##### Workload
* a set of programs that is either: 
    - the actual collection of applications run by a user
    - constructed from real programs to approximate such a mix
* typically specifies both the programs and the relative frequencies

##### Benchmark
* a program selected for use in comparing computer performance

##### Amdahl's Law
* a rule stating that the performance enhancement possible with a given improvement is limited by the amount that the improved feature is used
* a quantitative version of the law of diminishing returns

##### Million Instructions per Second _(MIPS)_
* a measurement of program execution speed based on the number of millions of instructions
* **MIPS** is computed as the instruction count divided by the product of the execution time and 10^6


## The BIG Picture

##### Time = Seconds/Program = Instructions/Program x (Clock Cycles)/Instruction x Seconds/(Clock Cycle)





##### The only valid and unimpeachable measure of performance is _execution time_

![Perforomance Equation](http://ece-research.unm.edu/jimp/611/slides/chap1_3-6.gif)


###### Challenges of Parallel Programming
* Scheduling
* Load Balancing
* Time for Synchronization
* Overhead for Communication Between Parties

###### The 5 classic components of a computer are:
1. Input
2. Output
3. Memory
4. Datapath
5. Control

> Here you can see the standard organization of a computer.
![CH1 Big Picture - Five Classic Components](http://i.imgur.com/e4XAQMg.png)

## Acronyms

* **PMD** - Personal Mobile Device
* **RAM** - Random Access Memory
* **LCD** - Liquid Crystal Display
* **CPU** - Central Processor Unit
* **DRAM** - Dynamic Random Access Memory
* **SRAM** - Static Random Access Memory
* **VLSI** - Very Large-scale Integrated Circuit
* **CPI** - Clock Cycles per Instruction
* **IPC** - Instructions per Clock Cycle
* **CMOS** - Complementary Metal Oxide Semiconductor
* **RAID** - Redundant Arrays of Inexpensive Disks
* **SPEC** - System Performance Evaluation Cooperative
* **MIPS** - Million Instructions per Second