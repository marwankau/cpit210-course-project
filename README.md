# CPIT210 Course Project
Introduction about your project, describe the problem, and your solution. Project truth tables, expressions, k-maps and any related task must included here. Also project documentation must included.

In this project students should work in groups of 3 to implement a fully functioning sequential circuit. This sequential circuit should work as a Buffer, a competition circuit, or 4-way light circuit depending on the student's choice. The idea of the three projects will be explained in the lab. To design the circuit, Logisim should be used. Students should submit their software implementation and the report here. 

## Group Members
[comment]: <> (each group memeber should write his first, middle and last name with link to his GitHub account)
- [Turki Naif Alghamdi](https://github.com/TurkiNAlghamdii)
- [Ahmad Fahad Alagbari](https://github.com/Memeedo)
- [Yousef hisham Bogari](http://github.com/usiifo)
### Selected topic: 
 Traffic Light


[comment]: <> (Students should include the contribution percentage of each group member.)
[comment]: <> (Example:)
### Contribution:
- Turki AlGhamdi 34%
- Yousef Bogari 33%
- Ahmed Alagbari 33%


## Circuit Project topics:

[comment]: <> (Choose one of the following, your choice need to be accepted by Instructor)


### Traffic Light
#### Problem Statement
This circuit is used to control a four-way traffic light control system. In what follows, it makes each traffic light work when it’s needed to be green or yellow and when it’s not (Red). Students are asked to design, and implement the required circuit.


## Components Used
### Counters
Since we have 2 inputs named Tg and Ta, express the duration of the green light and the yellow light respectively.
We will need two counters with different pulses rate of clock. To clarify, the counter responsible for the green light will have a clock with 3 ticks per second. While the other counter will have 2 ticks per second. As a result, the duration of the green light will be more than the yellow light.

### Multiplexer
The multiplexer is used to select one single input and carry it out as an output based on the selected value. We used three multiplexers as we have 3 D Flip Flops. The selection line are Q0, Q1, Q2. 
To get the next Q0, we must control the D0.
Using the multiplexer. We will generate the accurate input for each flip flop with the appropriate duration of each state.

### D Flip Flops
D Flip Flop will be used to store the data and count operations. As we have 3 current states on the truth table we will need 3 D Flip Flops.
The inputs of the D Flip Flops are generated by the three multiplexers. Based on the inputs we will have the next states. 

### Decoders
The decoder is used to change the binary number into 2^n output lines.
Why would we need decoders ?
For each state, the Flip Flops will bring out a number with 3 bits.
Our First decoder simply will take the 3 bit number and convert it to 8 output lines. Each line will have its Integer value.
We will connect the output of the main decoder other 4 decoders. Each 2 values of the outputs will be connected to a specific decoder in a specific region. To clarify: when the output of the main decoder is 0 the decoder on the North will be ON and the light is green. When it’s 1 the light will be Yellow .. etc.

### AND GATE
We used it to implement logical conjunction. So to check if the TA counter which has a 4 bit data counted to its full count (15). Combined with the Not GATE which sends 1s to the MUXS as long as the TA counter hasn't reach 15 and the TG counter still didn't reset. As soon as the TA counter reaches 15 and the TG counter resets the AND gate will output 1s which indicates the end of the yellow light phase.

### Splitter
We have many wires going into one gate or plexer etc. In such cases you we want to combine them in one bundle or saperate them. In order to do this we used splitters which allow us to combine many wires together or split the bundle to separate wires. We saperated the wires going as inputs into the AND gate from TA counter. By doing that we turned the current value of the counter to binary, also from the three D-flip flops to Muxs and Decoder. We combined the wires from the decoder to another splitter to sperate them into different decoders (S,W,E,N) based on what value was inputed into the decoder.





## Brief Overview

As we have 3 lights for a 4-way traffic light, each way has 3 states. Either green, yellow, or red. the red will be explained later since it depends on being the values 0. As for green and yellow. before we dig deeper. Since we have 4 traffic lights, that means each traffic light has 2 states (other than red). thus, we have 8 states (Q) for all traffic lights. We named each traffic light according to cardinal directions. Meaning north as N, west as W, east as E, south as S. the 8 states are going to be expressed in counting 0 to 7 (decimal) in binary. Starting with 000 (Q2Q1Q0) and ending with 111. These 8 states are being controlled according to whether that light is green or yellow (other than red). that’s why we need a controlling input. This controlling input is expressed in Tg (for green) and Ta (for yellow) combined. They are combined to form a binary number. This indicates that we have 4 situations. Two situations that focuses on the input of Tg and discards the input of Ta. The situations are. 0x (x = don’t care about the value (discard) ) which means that the light will be green on that certain way, As an example, let’s say it’s North. So 0x means green in north. Then 1x means the north light will change to yellow. now for Ta. X0 means that it will stay yellow in north. X1 means that it will change from yellow to green in the light. Let’s say west. Meaning the west light will be green. The same procedure will be repeated as the Q states keeps increasing one by one but with having a clock and counter to mange the time for each green or yellow light for each way. After doing the procedure, we can now form 3 D flip flops that represents each one of Q2Q1Q0. and the result of the 3 D flip flops as in Q2Q1Q0 combined will lead to form 3 multiplexers for each Q. so the select lines will be Q2Q1Q0 as stated before. As for input lines for each multiplexer, it depends on the equations that we obtain from the relationship between Tg,Ta and the next Q3Q2Q1. so after connecting the Muxs with D Ffs. Then we connect the Q2Q1Q0 from D ffs to a 3x8 decoder. The 8 outputs will be for each situation of the 4 way traffic light, meaning two for each traffic light. That means either green or yellow for North, and same for the rest. But each direction will have a 2x4 decoder of its own. These 2x4 decoders will be connected to 3x8 decoder to express the light or signal for each way. 


### Operations in detail 
Before we explain everything thoroughly, let’s highlight the major phases in our traffic light control. First one is about having a cloak connected to a counter named Tg which controls the input of the green color that will be displayed on the traffic light. Another cloak connected to a counter named Ta which controls the input of the yellow color that will be displayed on the traffic light. There are 3 D flip flips are being used to store data (Qs) the values that are being as input for the 3 D FFs are generated by a multiplexer. Meaning each multiplexer will generate a D ffs. Each Q of a D FF will be connected to a multiplexer. Then each multiplexer will generate the output for every D as follows. D0D1D2. But how will the input values of each multiplexer be determined? It will be determined based on TaTg values that we stated above before. Then we connect the correct values (Q2Q1Q0) from D ffs after the previous procedures are conducted to 3x8 decoder. Since we have 4 way traffic light. Each one will have 2x4 decoder. Then every 2v4 decoder will be connected to 3x8 to display the traffic light. so after highlighting the major phases. We will know explain the operations step by step. the explanation will be in an example to make it on point with no theoretical talk. Let’s take the first situation as an example, the first situation where the traffic light is green. So we obtain The Qs from D FFs as follows 000 (in a splitter) that are being sent to the mentioned multiplexers. Then each multiplexer will be selecting the first ( 0 ) input placed in that multiplexer. Let’s take the values of each multiplexer in this situation. The value in the first multiplexer will be Tg, and Tg equals 0 according to the truth table we obtained from the project material. As for the second multiplexer the value is 0. And 0 for the third multiplexer. So, the values are 000. these values will be sent to Dffs respectively.  All of this is controlled in a time-period according to TgTa as shown in the circuit. This 000 as v indicates the light is green according to the project material. This v will be sent to the decoder to be displayed. The v will keep increasing according to the project material and every v will display a specific light. 


## What problem we could face?
**- If we want to increase or decrease the time of a phase:**
You'd have to increase or decrease the Date Bits of it's counter. An example is the green light phase, we would have to increase the Data Bits of the TG counter to more than 4 Data bits or less based on what is preferred. The yellow light phase is set to a certen time and is dependent on the green light phase. When TG counter is done the yellow light phase starts. Since the TA is connected to an AND GATE which waits until it reaches it's full length of 15 to output 1 which means the end of yellow light phase.

**- We could've implemented the circuit using counters and ROM:** 
Which would have less cost and be much simpler, but since we don't have much experience with it we decided to go with what we have experience with.

##


## Deadline
Monday 29 / 7 / 1444 H, *20 Feb. 2023*

## Logic Expression
Include exported image from Logisim of your project here. *(Screenshot is not accepted!)*

![Our Awsome Project logic expression](/images/TrafficLight.png)

