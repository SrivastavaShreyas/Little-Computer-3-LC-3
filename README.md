# Little-Computer-3-LC-3

## What is LC-3?
Little Computer 3, or LC-3, is a type of computer educational programming language, an assembly language, which is a type of low-level programming language. It features a relatively simple instruction set, but can be used to write moderately complex assembly programs, and is a viable target for a C compiler. It has a simplified instruction set compared to **'x86'**, but contains all the main ideas used in modern CPUs.

## Memory
The LC-3 has 65,536 memory locations (the maximum that is addressable by a 16-bit unsigned integer 2^16), each of which stores a 16-bit value. This means it can store a total of only 128kb, which is a lot smaller than you may be used to! In our program, this memory will be stored in a simple array:

`uint16_t memory[UINT16_MAX];`

## Registers
A register is a slot for storing a single value on the CPU. Registers are like the "workbench" of the CPU. For the CPU to work with a piece of data, it has to be in one of the registers.The LC-3 has 10 total registers, each of which is 16 bits. Most of them are general purpose, but a few have designated roles.

-8 general purpose registers (R0-R7) : The general purpose registers can be used to perform any program calculations
-1 program counter (PC) register : The program counter is an unsigned integer which is the address of the next instruction in memory to execute.
-1 condition flags (COND) register : The condition flags tell us information about the previous calculation.

## Instruction Set
An instruction is a command which tells the CPU to do some fundamental task. Instructions have both an opcode which indicates the kind of task to perform and a set of parameters which provide inputs to the task being performed.

There are just 16 opcodes in LC-3. Everything the computer can calculate is some sequence of these simple instructions. Each instruction is 16 bits long, with the left 4 bits storing the opcode. The rest of the bits are used to store the parameters.

## Execution / Procedure
- Load one instruction from memory at the address of the `PC register`.
- Increment the `PC register`.
- Look at the `opcode` to determine which type of instruction it should perform.
- Perform the instruction using the `parameters` in the instruction.
- Follow the above steps again untill the result is achieved.

`https://github.com/SrivastavaShreyas/Little-Computer-3-LC-3/issues/1`
