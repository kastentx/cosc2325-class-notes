* what type of signals are moving around between components?
    - addresses
    - data
    - control signals
    - status flags
* what's a multiplexor?
    - like a traffic cop/switch
    - can be as simple as a 2-way or 16-way gate
    - takes 1 bit for every two pathways, to select between A and B
* what's a demultiplexor?
    - same thing but in reverse
* draw an ALU and think about the data lines needed
    - need to provide two pieces of data in
    - needs a data line going out for result
    - going to need control signals to tell ALU what to do
        + which operation is being performed?
    - status flags are coming back, in addition to the result
* if an ALU was getting data from an internal register, external memory, or a constant.. how would it be hooked up to control signals?
    - a demultiplexor is going to filter multiple pieces of data down into the right ones to send
* why do chip designers make it possible to read from two interal registers?
    - for speed
    - to be able to add two numbers from registers simultaneously
* how is memory connected to the control unit?
    - an address is needed to say where the data is coming from
    - registers are needed
        + one to hold on to the address
        + one to hold on to the data at that address
    - need control lines to tell you what to do
        + read or write?
* what are wait states?
    - need them to tell the computer to hold on while data needed data is arriving somewhere
* how is decoding an instruction done?
    - draw a register and split up the different bits
    - you need the opcode, the kind of operand
    - what are the operands
    - essentially, taking apart the bits and looking at what they mean
* What is Register Transfer Language?
    - used to model how things move from one component to another
    - focuses on the wires connecting one thing to another
    - "r1 + r2" for example, tells you that an ALU is needed that can add
    - eliminates some of the need for circuit diagrams
    - tells you the instructions you'll need to accomplish the tasks
* what major categories of instructions are there
    - arithmetic/logic operations
    - Input/Output
    - data movement
    - branching/controlling the program flow
* can RTL be used to study the timing of things?
    - by looking at the transfers of data, we can see how many operations there are
        + this is the same as the number of clock ticks we'll need
        + using these numbers, we can calculate the speed/timing
* define internal registers needed by Von Neumann
    - the general registers included.. doesn't need to be super specific
* common bus - what does it do?
* explain this `MOV SRC, DEST`
    - what are the allowable places for the SRC and the DEST
    - Intel doesn't want you to be able to use two memory locations
* superscalar - what is the fundamental idea?
    - wanting to go fast!
    - find any trick available to speed things up
    - caching, buffers, storing more than one piece of info at a time
* the problem with the addition in superscalar is 
    - read after write
* pentium: two modes
    - Real 
        + thinks machines only have 16 bits and 1 mb of ram
        + machine keeps this state until the boot process starts
        + HW sanity check and load an OS
        + isolates blocks of memory so the program thinks it has access to everything
    - Protected
* how does Pentium isolate memory?
    - starting location and size
    - machine stitches all these locations together so it appears linearlly
* what is virtual memory?
    - memory that actually lives on the hard drive
    - frees up blocks of faster memory for other things that need them
* draw a diagram of the RDX register in the 64-bit pentium
    - DL, DH, DX, RDX, EDX,
* what is a mnemonic
    - the codes that represent instructions
    - should help you figure out what the instruction does
* how do you declare an initialized variable? and uninitialized variable?
    - `resw 10000` to reserve 10,000 words
* initialized and uninitialized data are seperate. why?
    - because you don't need to store uninitialized data in a program's executable file
* whats a literal?
    - a value that's literally there!
    - something defined at compile time
    - can be an address, or a constant
    - NOT calculated at run-time
* RTDSC
    - a timing chip, that gives you clock ticks since it was turned on
    - not entirely accurate because there can be other programs drawing on resources
    - the process may have been interrupted without you knowing it, which will affect the timing
* when doing a timing analysis..
    - need to make sure that overhead from other programs aren't affecting the readings
    - you need to also make sure that the sample size is accurate for your specific application
    - complexity analysis needs to tell you if you can do something a million times, for example
* be able to talk your way through memory hierarchy
* cache memory
    - using part of an address to identify an address of a different block
        + then those parts are stored in a faster type of memory
        + the odds are, the next stuff you'll need will be located nearby
* difference betwen static and dynamic memory
    - Cost!
    - Speed!
* volatile vs. non-volatile memory
    - volatile memory disappears when the power is removed
    - non-volatile persists even when power is removed
* solid-state drives
    - no moving parts
    - transistors instead of spinning disks