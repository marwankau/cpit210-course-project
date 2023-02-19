# CPIT210 Course Project
Introduction about your project, describe the problem, and your solution. Project truth tables, expressions, k-maps and any related task must included here. Also project documentation must included.

In this project students should work in groups of 3 to implement a fully functioning sequential circuit. This sequential circuit should work as a Buffer, a competition circuit, or 4-way light circuit depending on the student's choice. The idea of the three projects will be explained in the lab. To design the circuit, Logisim should be used. Students should submit their software implementation and the report here. 

## Group Members
[comment]: <> (each group memeber should write his first, middle and last name with link to his GitHub account)
- [Hassan Abdullah Turkistani](https://github.com/HassanHAT)
- [Eyad Adel Fageera](https://github.com/EyadFageera)


[comment]: <> (Students should include the contribution percentage of each group member.)
[comment]: <> (Example:)
### Contribution:
- Hassan
- Eyad



### Traffic Light
#### Problem Statement
The 4 direction traffic flow is controlled by the traffic light system. One direction light will turn on when it is green, the other directions will turn red, the light in that direction will turn yellow to signal that traffic is about to stop, then red, and other directions will repeat the same process. In this way, the circuit will be controlled by a minimum of 8 states. Each direciotn will have two state which is yellow and green light.        


## Finite State Machine for Traffic Light Control

![Finite State](/images/Finite-State-Machine.png)

Each of the different states in this finite state machine will cause a different action to be taken. There are 4 directions, green and yellow lights. If we select the north direction to be green, the next state will be yellow. When this state is over, we will choose the next direction to be green, and so on through the entire state. The value shown above in the diagram determines how the states change. Each arrow indicates that the first value is for TG and the next value is for TA, and these values will be displayed in the transition table.

## Transition Table

![Transition Table](/images/Transition-Table.png)

The finite state has 8 states equal to 2^3 so the table will have 3 Q's state denoted by Q0, Q1, and Q2. Each one of them will have 2 input TG and TA. The state will change to the next state by the inputs. Therefore, we need to implement D flip flop for all the current states Which it will be 3 D's flip flops. The Transition Table for D value is equal to the output, meaning that D0 is the same as Q0 after the clock transition. The implement for D is by an 8x1 Multiplexer.

## Component used 
### Multiplexer 
![Mutliplexer](/images/MultiPlexer-4.png)

There will be 3 Multiplexer for each D function. The selectors will be the current state Q0, Q1 and Q2. 

The first multiplexer when the selector value is 0 the input 0 for the multiplexer is TG Because it follows the next state values for Q0. When the selector is equal to 1 the input will be TA’ based on the next state values and the rest for all the states will be the same as shown in the table. 

The second implementation of multiplexer for the D1. Based on the table of the Q1 next state, there will be 0’s and 1’s based on the value of the next state. For Example, once the select value is 0 the input stays 0, and when the select is 2 the input will be 1.

The last implementation of multiplexer D2. The Q2 next state is 0 until the select value is 3 it will follow the input TA  , and the next values of the select until 7 the Q2 next state is 1. For the last state which is 7, the input will be TA’.

### Counter 

![Coutner](/images/counter-truth-table.png)
The above truth table is the T flip flop coutner that count from 0 to 15, the carry is the value of TG and value will change to 1, when the counter reaches the maximum number. The bit output for the counter will be QA , QB, QC and QD which is the value of TA.

### D flip flop

Will act like a register it will store the output for the multiplexer. The input for the flip flop will be D0 to D3. when D0 value is one the next state for the traffic light will be yellow. D1 and D2 it will control the next state of which traffic light will be green. When the traffic light is yellow and the count reaches 4, then the counter will reset. The count of the yellow light can be reduced if we change the value TA from QC to QB it will reset when the counter reaches 2.     



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

![T ff Counter](/images/T-ff-Counter.png)

![4bit register](/images/4bit-register.png)

![Traffic Light Controller](/images/Traffic-Light-Controller.png)

![Traffic light](/images/main.png)

