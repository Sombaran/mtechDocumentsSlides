# 30 August 2025 (BASICS OF LOGIC GATE)

> [Click here for recording](https://cciitpatna-my.sharepoint.com/:v:/r/personal/ecs5102_iitp_ac_in/Documents/Recordings/ECS%205102%20-%20Lecture%20Room-20250830_130641-Meeting%20Recording.mp4?csf=1&web=1&e=8bKVjj&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)
> Session is linked to 24 August 2025

## Boolean alzebra

- It is set of axioms and theorem to simplfy boolean equations or simplfy logical expression withour changing its functionality
- Its follows principle of duality
- Axioms

    | Axioms                | Duality               |
    | --------------------  | --------------------  |
    | B = 0 then B! = 1     | B=1 then B!=0         |
    | 0' = 1                | 1'= 0                 |
    | 0.0 = 0               | 1+1 = 1               |
    | 1.1 = 1               | 0+0 = 0               |
    | 0.1 = 1.0 = 0         | 1+0 = 0+1 =1          |

- ![Boolean Alzebra Theorems](C:\Users\ritup\OneDrive\Pictures\boolean_alzebra.png)

## Bubble pushing

- Pushing bubbles backward (from the output) or forward (from the inputs) changes the body of the gate from AND to OR or vice versa
- Pushing a bubble from the output back to the inputs puts bubbles on all gate inputs
- Pushing bubbles on all gate inputs forward toward the output puts a bubble on the output and changes the gate body

## Rules for bubble pushing

- Begin at the output of the circuit and work toward the inputs
- Push any bubbles on the final output back toward the inputs
- Draw each gate in a form so that bubbles cancel
