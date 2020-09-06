# How I built a RISC-V CPU Core in a span of 5 days.
Project Repository for RISC-V MYTH ( Microprocessor for You in Thirty Hours) workshop, conducted by VSD Corp and Redwood EDA.This workshop was conducted over a period of 5 days and in  this short span of time we were able to understand & implement a RISC-V core with base instruction set. Programming language used in the software section was C, assembly (pseudo codes) were also utilised, along with TL-Verliog for HDL implementation. Tools used: Spike and Makerchip IDE.

# Table of Contents
- [What is RISC?](#What is RISC?)
- [Day 1.](#Day 1)
  - [Lab 1.](# Lab 1)
  - [Lab 2.](# Lab 2)
- [Day 2.](# Day 2)
  - [Lab 1.](# Lab 1)
  - [Lab 2.](# Lab 2)
- [Day 3.](# Day 3)
- [Day 4.](# Day 4) 
- [Day 5.](# Day 5)
- [Observations.](#observations)
- [Challenges.](#challenges)
- [Limitations.](#limitations)
- [Acknowledgements.](#acknowledgements)


# What is RISC?
RISC-V is an open source instruction set architecture(ISA) based on reduced instruction set computing concept.Unlike other existing commercial ISAs, the RISC-V ISA is open and this makes it easy and flexible for anyone to build a processor that supports it. This workshop thus gave us and overview of the software as well as the hardware aspect and following hands on experiments were done to learn by doing rather than just reading the theory or specifications.

# Day 1 : Instruction Set Architecture
  This was just a warm up of the extensive work we would be doing in the further days. It made us familiar with the VSD-IAT platform and using the lab instances . 
  A brief overview of how the higher level languages are converted to assembly and then into machine/binary format , in a hierarchical level was given. Then we     were introduced to the various types of instructions which are as follows
  
  - RV64I or RV32I Base integer instructions: 64 and 32 bit data instructions respectively
  - RV64M i.e Multiply extension
  - RV64IM : Includes base and multiple extension.
  - RV64F and RV64D : Floating point and Double extenstion. 
  
  Additionally we learnt about the integer number representation and their maximum and minimum ranges.
  
  - Integer: 
    - Word i.e. 32 bits.
    - Double word i.e 64 bits
    RV64 has range 0 to (2<sup>64</sup> - 1)
    
  - Negative i.e floating point numbers:  - 2<sup>63</sup> to (2<sup>63</sup> - 1)
    
    The instructions which work on these numbers are called Base Integer Instruction **RV64I**.
  
## Lab 1 : C program of Sum 1 to n  numbers
  A basic C program to calculate sum of natural numbers upto a limit provided by the user. The program can be found here (insert link) 
  (**Note** : This problem  is used as a basis to understand at each hierarchy level of programming and then finally implement our core till day 5. )
  Command used to compile the C program is `gcc <filename.c>` or `gcc -o <binary file name> <filename.c>`and to run we use `./a.out` or `./<binary file name>`
  
  **Output on console**
  
## Lab 2 :
  The same c program is now compiled using RISC-V toolchain.  
  - Command used to compile the C program is `riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c`. 
  - To view to disassemble and view the object file in readable format, following is the command `riscv64-unknown-elf-objdump -d sum1ton.o`.
  - To run we use spike which is a RISC-V simulator, following is the command `spike pk sum1ton.o`.
  - Spike has a debugging feature too which can be used to run it in steps, following is the command `spike -d pk sum1ton.o`.
  
  **Output on console**

## Lab 3 :
  A C program is implemented to  show the maximum and minimum sizes for RV64I. The program can be found here (insert link)  
  - Commands used are same as Lab 2

  **Output on console**

# Day 2

## Lab 1

## Lab 2

# Day 3

# Day 4

# Day 5

# Observations

# Challenges

# Limitations

# Acknowledgements
