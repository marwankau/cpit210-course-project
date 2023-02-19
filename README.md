# CPIT210 Course Project
Introduction about your project, describe the problem, and your solution. Project truth tables, expressions, k-maps and any related task must included here. Also project documentation must included.

In this project students should work in groups of 3 to implement a fully functioning sequential circuit. This sequential circuit should work as a Buffer, a competition circuit, or 4-way light circuit depending on the student's choice. The idea of the three projects will be explained in the lab. To design the circuit, Logisim should be used. Students should submit their software implementation and the report here. 

## Group Members
[comment]: <> (each group memeber should write his first, middle and last name with link to his GitHub account)
- [Khaled Ahmed Alghamdi](https://github.com/KhaledAhmedALghamdi)
- [Abdulrahman Majed Alobise](https://github.com/dahmoni1211)
- [ABDULMOHSEN AHMED ALMUTLAQ](https://github.com/Abdulmohsen-almutlaq)

[comment]: <> (Students should include the contribution percentage of each group member.)
[comment]: <> (Example:)
### Contribution:
- Ahmed 35%
- Fahad 35%
- Ali 30%

## Circuit Project topics:

[comment]: <> (Traffic Light)


### Traffic Light
#### Introduction
Traffic light is a signaling device that has an electronic circuit designed to control the flow of traffic at the roads by a specific sequence of lights. Traffic lights were first installed in 1868 in London, and have become widely used all over the world. Currently, there are different standards of traffic signals in the world, depending on the local traffic regulations. In the Kingdom of Saudi Arabia, the following sequence is followed: passing is permitted at green, then ready to stop at yellow, and finally comes to a complete stop at red. The goal for this project is to design and simulate a functioning 4-way traffic light control circuit using digital logic components and Logisim simulation software. The schematic of the 4-way traffic light is shown in Figure 1.

#### Methodology
The first step in the project is to construct the finite-state machine (FSM) or simply the state diagram of the 4-way traffic light which is used to show how the traffic flows. The state diagram can change from one state to another in response to some inputs; the change from one state to another is called a transition which has to be tabulated in what is called transition table. To ensure applying the logic of the traffic light properly, we have to control the inputs and follow certain sequence to switch from state to state. This can be implemented by using counter and selecting the proper flip flops and multiplexers. Therefore, inputs can be passed to traffic light through proper decoders. to ensure the functionality of the logical circuit the software Logisim will be used. Each step of the project including components will be explained and documented.

#### State diagram
The FSM is defined by a list of states, initial state, and inputs that trigger each transition. Initially, all signals in the 4-way traffic light system are red. The system inputs are TG and TA, where TG is the signal to control the time of the green light state, and TA is the signal to control the time of the attention (yellow light) state. The input signals are generated and controlled by a clock and a synchronous binary counter. The first state north green (NG) is when the northern signal is in the green light situation. The inputs to NG state have two modes, the first is 0x and the second is 1x, in both modes the first digit refers to the input variable TG and the second digit refers to the input variable TA. The input mode 0x means the signal of TG is 0 and the signal of TA is x which means in NG we don’t care about TA signal; in this situation the signal will continue in green light. When the input signal is 1x this means TG is 1 which is a signal to move from the first north green state NG to the second state which is north attention state (NA). In attention state TA signal is the controlling signal and we don’t care about TG signal, therefore the input signals will be x0 and x1, where the first means continue in NA and the second means change to third state which is west green (WG). Because we have four ways, the states will keep changing according to the following sequence NG>NA>WG>WA>SG>SA>EG>EA>NG as shown in the Figure 2.

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

