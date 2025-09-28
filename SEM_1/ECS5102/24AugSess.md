# 24 August 2025 (BASICS OF LOGIC GATE)

> [Click here for recording](https://cciitpatna-my.sharepoint.com/:v:/r/personal/ecs5102_iitp_ac_in/Documents/Recordings/ECS%205102%20-%20Lecture%20Room-20250824_131415-Meeting%20Recording.mp4?csf=1&web=1&e=PHH4Bi&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)

## Basics of logic gates

- AND
  - Y=(A.B)/ (A*B)
- OR
  - Y=(A+B)
- NOT
  - Y=A'
- BUFFER
  - Y=A
- NOR
  - Y=(A+B)'
- NAND
  - Y=(A.B)'
- XOR
  - Y=(A^B)
- XNOR
  - Y=(A^B)'

## Rules of combinational circuit

- Every circuit element is itself combination
- Every node is considered as an input to the circuit or connects to exactly one output
- The cicuit must not contain any cyclic path

## Some definition

- Compliment with a bar over it: A',B',C'
- Literal: variable or its complement A, A', B, B', C, C'
- Implicant: product of literal ABC', A'C, BC
- Minterm: Y = 0->A' && 1->A  
- Maxterm: Y = 0->A  && 1->A'

## Sum of product

- For eg: ABC + A'B'C'
- Minterm is product of liberals
- Y = F(A,B)= AB + A'B
- Oring of minterms

## Product of sum

- For eg: (A+B+C) . (A'B'C')
- Maxterm is sum of liberals
- Y = F(A,B)= (A'+B') . (A+B')
- Anding of maxterms

## Boolean equation example

- Will be continued in 30AugSess.md
