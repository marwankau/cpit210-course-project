# CPIT210 Course Project
Introduction about your project, describe the problem, and your solution. Project truth tables, expressions, k-maps and any related task must included here. Also project documentation must included.

In this project students should work in groups of 3 to implement a fully functioning sequential circuit. This sequential circuit should work as a Buffer, a competition circuit, or 4-way light circuit depending on the student's choice. The idea of the three projects will be explained in the lab. To design the circuit, Logisim should be used. Students should submit their software implementation and the report here. 

## Group Members
[comment]: <> (each group memeber should write his first, middle and last name with link to his GitHub account)
- [Turki Baatta](https://github.com/TurkiBaatta)
- [Abdullah Al-Sharif](https://github.com/Abdullahalsharif21)
- [Yazen Ahmed](https://github.com/Yzn80)

[comment]: <> (Students should include the contribution percentage of each group member.)
[comment]: <> (Example:)
### Contribution:
- Turki 34%
- Abdullah 33%
- Yazen 33%

## Circuit Project topics:

[comment]: <> (Choose one of the following, your choice need to be accepted by Instructor)

### Buffer
#### *** Problem Statement ***
This circuit solves the reading and writing to buffer. For example: If we have input 4, we want to write it, buffer works like memory and stores it there when we click the write button. In case when we want to read from the buffer, by pressing read button, it starts reading from the first entry sored in the buffer. Buffer is nothing but a temporary memory. In addition, we can clear the contents from the buffer. Students are asked to design, and implement the required circuit.

#### *** The Solution ***
In this project we want to implement a buffer that receives a 4-bit input data and the output will be on a memory RAM consist of 16 address for 16 input data every address from these 16 address consist of 4-bit for each input data, so as a conclusion we need 3 counter address to read from, address to write to and the number of element on buffer. So start do 3 counter flop each of these counter have there special functionality.

### Components

We used a combination of ingredients:
1 – Write counter
2 – Read counter
3 – Item counter
4 – D F/F
5 – Multiplexer
6 – Data input && Data output
7 – CLR button
8 – Clock
9 – Splitter
10 – Logic Gate (AND – OR – NAND – NOT)
11 – Power
12 – RAM and Hex digit display.

## Grading Factors
Each student's grade will defer from his group-mate 
- content and organization
- stating the problem need to be solved
- explanation of each component used
- explanation of whole circuit/integration of component
- how often you update/participate/contribute in group repository

## Deadline
Monday 29 / 7 / 1444 H, *20 Feb. 2023*

## Logic Expression
Include exported image from Logisim of your project here. *(Screenshot is not accepted!)*

![Our Awsome Project logic expression](/images/logic-expression.png)

