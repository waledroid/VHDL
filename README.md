# VHDL
Design of a simple microprocessor capable of executing a set of assembly instructions.



## Introduction:

The objective of this project is to design a simple microprocessor capable of executing a set of assembly instructions. The microprocessor features an 8-bit address bus, separate 8-bit input and output memory data buses, an accumulator, and a program counter. The assignment requires the implementation of five fundamental instructions: Load (LDA), Store (STA), Add (ADD), Jump if No Carry (JNC), and Jump (JMP). Additionally, the CPU is connected to external memory, featuring an 8-bit address bus and separate read and write data buses. The design should include an asynchronous reset, initializing all registers, and execute a provided assembly code.

## Methods:

Design Process:

The microprocessor design follows a finite state machine (FSM) architecture, with each state representing a stage in the instruction execution. The FSM states include loading the opcode, fetching the operand, and executing specific actions based on the opcode. The design uses an asynchronous reset to initialize the registers, including the program counter, accumulator, and opcode.

Assembly Code Execution:

Load Opcode State (load_opcode): The microprocessor begins by loading the opcode from the memory and increments the program counter.

Fetch Operand State (fetch_operand): The operand is fetched from the memory, and the microprocessor transitions to the state corresponding to the specific opcode.

Individual Instruction States (LDA_1, STA_1, ADD_1, JNC_1, JMP_1):

LDA_1 (Load Accumulator): Loads the accumulator with the operand and increments the program counter.
STA_1 (Store Accumulator): Stores the accumulator value in the specified memory address and increments the program counter.
ADD_1 (Add): Adds the contents at the specified memory address to the accumulator and updates the carry flag.
JNC_1 (Jump if No Carry): Jumps to the specified address if the carry flag is not set.
JMP_1 (Jump): Jumps to the specified address.
Carry Flag Handling:

The design includes a carry flag that is updated during the ADD_1 state. The carry flag is checked in the JNC_1 state to determine whether to perform a jump based on the absence of a carry.

## Conclusion:

In conclusion, the microprocessor design aligns with the assignment specifications, providing a foundation for executing a simple assembly code. The simulation of the microprocessor should demonstrate the correct execution of the provided assembly code, confirming the proper functioning of the implemented FSM. To further enhance the algorithm, additional error handling mechanisms could be incorporated to address unexpected opcodes or memory addresses. Additionally, rigorous testing, both in simulation and on the hardware, is recommended to validate the correctness and robustness of the microprocessor design.


