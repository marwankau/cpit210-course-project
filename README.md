# CPIT210 Course Project
Introduction about your project, describe the problem, and your solution. Project truth tables, expressions, k-maps and any related task must included here. Also project documentation must included.

In this project students should work in groups of 3 to implement a fully functioning sequential circuit. This sequential circuit should work as a Buffer, a competition circuit, or 4-way light circuit depending on the student's choice. The idea of the three projects will be explained in the lab. To design the circuit, Logisim should be used. Students should submit their software implementation and the report here. 

## Group Members
[comment]: <> (each group memeber should write his first, middle and last name with link to his GitHub account)
- [Turki Naif Alghamdi](https://github.com/TurkiNAlghamdii)
- [Ahmad Fahad Alagbari](https://github.com/Memeedo)
- [Yousef hisham Bogari](http://github.com/usiifo)
### Selected topic: 
1. Traffic Light


[comment]: <> (Students should include the contribution percentage of each group member.)
[comment]: <> (Example:)
### Contribution:
- Yousef Bogari 34%
- Ahmed Alagbari 33%
- Turki AlGhamdi 33%

## Circuit Project topics:

[comment]: <> (Choose one of the following, your choice need to be accepted by Instructor)


### Traffic Light
#### Problem Statement
This circuit is used to control a four-way traffic light control system. In what follows, it makes each traffic light work when it’s needed to be green or yellow and when it’s not (Red). Students are asked to design, and implement the required circuit.


### Components Used
#### Counters
Since we have 2 inputs named Tg and Ta, express the duration of the green light and the yellow light respectively.
We will need two counters with different pulses rate of clock. To clarify, the counter responsible for the green light will have a clock with 3 ticks per second. While the other counter will have 2 ticks per second. As a result, the duration of the green light will be more than the yellow light.

#### Multiplexer
The multiplexer is used to select one single input and carry it out as an output based on the selected value. We used three multiplexers as we have 3 D Flip Flops. The selection line are Q0, Q1, Q2. 
To get the next Q0, we must control the D0.
Using the multiplexer. We will generate the accurate input for each flip flop with the appropriate duration of each state.

#### D Flip Flops
D Flip Flop will be used to store the data and count operations. As we have 3 current states on the truth table we will need 2^3 D Flip Flops.
The inputs of the D Flip Flops are generated by the three multiplexers. Based on the inputs we will have the next states. 

#### Decoders
The decoder is used to change the binary number into 2^n output lines.
Why would we need decoders ?
For each state, the Flip Flops will bring out a number with 3 bits.
Our First decoder simply will take the 3 bit number and convert it to 8 output lines. Each line will have its Integer value.
We will connect the output of the main decoder other 4 decoders. Each 2 values of the outputs will be connected to a specific decoder in a specific region. To clarify: when the output of the main decoder is 0 the decoder on the North will be ON and the light is green. When it’s 1 the light will be Yellow .. etc.


## Deadline
Monday 29 / 7 / 1444 H, *20 Feb. 2023*

## Logic Expression
Include exported image from Logisim of your project here. *(Screenshot is not accepted!)*

![Our Awsome Project logic expression](/images/logic-expression.png)

