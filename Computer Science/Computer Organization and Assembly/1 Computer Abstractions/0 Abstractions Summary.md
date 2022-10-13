# Unit Summary
Tags: #Summary #UAG

Relevant files: [[Chapter 1 Computer Abstractions and Technology.pdf|Lecture 1]]

## Inside the Processor
- There are largely three components
	- Datapath: how data is acted on (mux, and add)
	- Control: Chooses what operations are enacted
	- Cache memory: Memory stored extremely close to the processor
		- Memory for immediate operations
		- Fetching moves the instructions and data partitions to the cpu cache
		- Also called SRAM

Each type of processor is divided into components which have a specific kind of purpose. A few of these are the following
1. Arithmetic Logic Unit (ALU): Fast computations by basic arithmetic operations
2. Registers: Memory within the CPU
3. Control Unit (CU): Fetch data and instructions from memory. Flow info between registers and ALU

Each CPU has tons of ALUs depending on the design and number of cores. In addition the ALU has a number of bits which it can actually add.

Mobile phones processors are typically called an Application Processor (AP) and are typically based on ARM

### Abstractions for the CPU
In order to hide a layer of detail we need to create an abstraction layer. In order to do this the **Instruction set Architecture (ISA)** was created. This provides an interface for how to do things on a specific processor. This is effectively the interface between the software and hardware.

After this there is another layer of abstraction called the **Application binary interface (ABI)** which also includes how to use the system software.

## PC Memory
Computers need to store large amounts of information for a variety of purposes. Some of them need to be fast and non-perminant while others can be a bit slower but perminant. In order to solve this there are two categories of memory which are established
1. Volatile Memory
2. Non-volatile memory
Volatile memory is only temporary and requires power in order to keep values. Non-volatile does not have this same requirement.

### Homework #1
Need to research what types of RAMs there are

## Networks
Networks are important to do things

## Technology Trends
Started with Vacuum tubes, then transistors, then scaled ICs

## ISA
Here is a list of the modern ISAs
1. IA-32
2. PowerPC
3. MIPS (The one used for this class)
4. SPARC
5. ARM