# 17 August 2025 (BASICS OF DIGITAL LOGIC)

> [Click here for recording](https://cciitpatna-my.sharepoint.com/:v:/r/personal/ecs5102_iitp_ac_in/Documents/Recordings/ECS%205102%20-%20Lecture%20Room-20250817_111736UTC-Meeting%20Recording.mp4?csf=1&web=1&e=EIWIur&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)
> [For revision click here](https://cciitpatna-my.sharepoint.com/:v:/r/personal/ecs5102_iitp_ac_in/Documents/Recordings/ECS%205102%20-%20Lecture%20Room-20250823_090421UTC-Meeting%20Recording.mp4?csf=1&web=1&e=WEC09z&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)

## Art of managing complexity

- Abstraction
  - Hiding when they are not important
- Discipline
  - Intentially restricting design choice to work more productively at higher level of abstraction  
  - Digital discipline
- The 3-Y's
  - Hierarchy
    - A system divide into modules and submodules
  - Modularity
    - Having well defined functions and interfaces
  - Regularity
    - Encouraging uniformity, so modules can be easily reused

## Number system

- Binary to decimal
- Decimal to binary
- Hexadecimal to decimal
- Hexadecimal to binary
- Bites/ bytes/ nibble
- Power of two
  - 2^10 = kilo
  - 2^20 = mega = 1 million
  - 2^30 = gigi = 1 billion
- Estimating power of 2
- Addition of binary numbers
- Limitation of binary addition with overflow _msb_ bit
- Addressing the overflow of _msb_ bit
  - Signed binary
    - Signed magnitute
      - Range [-2^n-1 - 1, 2^n-1 - 1]
      - It has two representations of Zeros which causes issues
      - Addition and Subtraction of Signed Magnitude are way more difficult and cause discrepency
      - Signed Magnitude is a bit less efficient in the hardware
    - 2's complement
      - Range [-2^n-1, 2^n-1 - 1]
      - 2's Complement can easily perform Arithmetic operations
      - One can easily find the negative of any number with 2's Complement
      - For Binary Computation, the 2's Complement is highly used
- Increasing bit width: Value of the bit can be increased from _N_ to _M_ bits where _M>N_ by using
  - Sign extension
    - signed bits is copied in _MSB_
    - Number value remains the same
    - For eg
      - [3]  = 0011
      - [3]  = 0000 0011
      - [-5] = 0101 -> 1's complement -> 1010 -> [+1] -> 1011
      - [-5] = 1111 1011
  - Zero extension
    - Zeros are copied in _MSB_
    - Value will change for (-ve) numbers
    - For eg
      - [3]  = 0011
      - [3]  = 0000 0011
      - [-5] = 0101 -> 1's complement -> 1010 -> [+1] -> 1011
      - [-5] = 0000 1011
