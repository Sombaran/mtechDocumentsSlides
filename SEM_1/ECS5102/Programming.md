# FCS Topic 

## Design principle 1

- Simplicity favours regularity, i.e consistent instruction format with same number of operarnds (2 sources and 1 destinations) making it easier to encode and handle in hardware

## Design principle 2

- Make the common case fast
  - MIPS includes only simple, commonly used instructions
  - Hardware to decode and execute the instruction can be simple, small, and fast
  - More complex instructions (that are less common) can be performed using multiple simple instructions
  - MIPS is a reduced instruction set computer ( RISC), with a small number of simple
  - Other architectures, such as Intel’s IA 32 found in many PC’s, are complex instruction set computers ( CISC). They include complex instructions that are rarely used, such as the “string move” instruction that copies a string (a series of characters) from one part of memory to another
  
## Design principle `
  
- Smaller is Faster
  - MIPS includes only a small number of registers
 
## Design principle 4
 
- Good design demands good compromises
  - Multiple instruction formats allow flexibility
  - Number of instruction formats kept small
  - To adhere to design principles 1 and 3 (simplicity favors regularity and smaller is faster).

## What are operands

- A computer needs a physical location from which it retrieve binary command executed by a processor
- A computer retrieves operands from:
  - Registers
    - As memory is slow therefore most most architectures have a small set of (fast) registers (32)
	- MIPS is called a 32 bit architecture because it operates on 32 bit data
  - Memory
  - Constants (also called immediates)

> In load (LW) the first register is the destination
> In store (SW) the frst register is the source 


## MIPS instruction format
  
- There are 3 types of MIPS instruction
  - _R_
    - Register type
    - 3 register operands:
	  - rs, rt : source registers
	  - rd: destination register
	- Contains 6 fields
	  - opcode (op) __6 bits 000000__
	  - first register source (rs) 5 bits
	  - second register source (rt) 5 bits
	  - destination register (rd) 5 bits
	  - shift amount (shamt) 5 bits __if no shift value is given then use 00000__
	  - bit represtation of function (funct) 6 bits __what particular operand represent__
	  -  
  - _I_
    - Immediate type
	- 3 operands:
	  - rs, rt : register operands __5 bits each source and target__
	  - imm: __16 bit two’s complement immediate__
	  - opcode (op) __6 bits__
  - _J_
    - Jump type
	- 26 bit address operand addr 
	- Used for jump instructions j
	- opcode (op) __6 bits__