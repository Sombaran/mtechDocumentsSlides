# 16 August 2025 (INTRODUCTION)

> [Click here for recording](https://cciitpatna-my.sharepoint.com/:v:/r/personal/ecs5102_iitp_ac_in/Documents/Recordings/ECS%205102%20-%20Lecture%20Room-20250816_130536-Meeting%20Recording.mp4?csf=1&web=1&e=1tyq3t&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)

## Why learn this cousrse

- Both hardware and software effect performance of a computer
- Algorithm detemines _source level statements_
- Language/ Compilers/ Architecture determines _machine instructions_
- Process/ Memory determines _how fast instructions are executed_
- I/O and Cores detemines _overall system performance_

## Five classic components of computer

- Input
- Memory
- Control
- Datapath
- Output

> Control and datapath together called as CPU

## Levels of transformation

- Electrons
- Circuits (Analog)
- Logic (Digital)
- Microarchitecture: Internal design of the _processor_ like ALU/ Cache/ Register (Actual implementation)
- ISA (Instruction for CPU to process)
- Runtime system
- Programming language
- Algorithm
- Problem solving

## Software and hardware interaction

- Autometa: How the machine that solves a problem
- Instruction set maps as in interface between hardware and software
- User are writing codes in high level language which has to gets converted in some sort of instruction so that it can be   executed by the hardware. Therefore there is a component called assembler which is responsible for converting high level language to _machine code instructions_
- ISA acts as an interface between _software component and hardware component_
- Since its predefined therefore _sometimes new innovations are prevented_
- System chipset is called _microarchitecture_

## Computer system architecture

- OS is a program which acts as an interface between user and computer hardware
- COmputing system is broadly divided into 4 components
  - Hardware
    - CPU, I/O devices, Memory
  - Operating system
    - Control and coordinats with hardware among application and users
  - Application program
    - What we see in _monitor_
  - User
    - People, machines

## Operating system

- OS is a resource allocator
- OS is a control program
- One program runs every time is called _kernel_ and everthing else is either user or system program
- Boot sequence
  - Bootstrap program is stored in some non-volatile memory(ROM/ EPROM) generally called firware
  - Initilies all aspect of system
  - Loads kernel and starts execution
- When power in initialized on piece of program called _bootstrap loader_ which is stored in EEPROM/ROM located in _kernel_ loads into memory for execution
- GRUB is a bootstrap loader
- kernel loads and system is then _running_
- OS preserves the state of CPU by storing _registers_ and the _program counter_

## Common functions of interrupts

- OS is interupt driven
- Interrupts transfers control to ISR through interrupt vendor which contains addresses of all the ISR
- Interrupt is either caused by _user_ or _software_
- Interrupt architecture must save the address of the _interrupted instruction_
- Types of Interrupts
  - Polled interrupts
    - Specific type of I/O interrupt
    - Indicates device is ready to read
    - Sends poll requests to all devices to understand which one made the request
  - Vectored interrupts
    - Interrupting device directs the processor to appropriate ISR based on _set priority_

## Storage structure

- Main memory
  - Only large solid state media CPU can access directly
  - RAM, typically volatile
- Secondary storage
  - Extension of main memory typically non-volatile
- Hard disks
  - Rigid metal covered with magnetic recording material
- Solid state devices
  - faster than hard disks, non volatile

## Hierarchy

> registers (Very costly) \n
> cache \n
> main memory \n
> solid-state disk \n
> hard disk \n
> optical disk \n
> magnetic tapes \n
