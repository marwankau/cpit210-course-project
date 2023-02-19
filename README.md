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
The four-direction traffic flow is controlled by the traffic light system. One direction light will turn on when it is green, the other directions will turn red, the light in that direction will turn yellow to signal that traffic is about to stop, then red, and other directions will repeat the same process. In this way, the circuit will be controlled by a minimum of eight states. Each direciotn will have two state which is yellow and green light.        

![Traffic light](/images/traffic-1.png)

## Finite State Machine for Traffic Light Control

![Finite State Machine](/images/Finite State Machine.png)

Each of the different states in this finite state machine will cause a different action to be taken. There are four directions and green and yellow lights. If we select the north direction to be green, the next state will be yellow. When this state is over, we will choose the next direction to be green, and so on through the entire state. The value shown above in the diagram determines how the states change. Each arrow indicates that the first value is for TG and the next value is for TA, and these values will be displayed in the transition table.


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

