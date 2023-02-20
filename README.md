# CPIT210 Course Project

In this project, we will work as members of one group, and we will make a sequential circuit that operates at its full capacity, and this sequential circuit must work as a time store circuit, a competition circuit, or a lighting circuit that contains 4 directions, and we will explain and present the logisim required of us as a team to design the circuit.

## Group Members
[comment]: <> (each group memeber should write his first, middle and last name with link to his GitHub account)
- [Arif Ziyad Alharthi](https://github.com/Arif-Alharthi)
- [faisal abdullah alghamdi](https://github.com/faisalgh7)
- [Abdullah Khaled Banaemah](https://github.com/AbdullahBM-1419)

[comment]: <> (Students should include the contribution percentage of each group member.)
[comment]: <> (Example:)
### Contribution:
- Arif 33.3%
- Faisal 33.3%
- Abdullah 33.3%

## Circuit Project topics:

[comment]: <> (Choose one of the following, your choice need to be accepted by Instructor)

### Buffer
#### Problem Statement
This circuit solves the reading and writing to buffer. For example: If we have input 4, we want to write it, buffer works like memory and stores it there when we click the write button. In case when we want to read from the buffer, by pressing read button, it starts reading from the first entry sored in the buffer. Buffer is nothing but a temporary memory. In addition, we can clear the contents from the buffer. Students are asked to design, and implement the required circuit.


## description 
### First section "Arif" 

- The project was divided into three parts, and I will explain my part in a simple way and support it with some illustrations.

- At first I have configured 3 counters in my circuit and each circuit performs a different function than the other, let's see the function of each counter..

- write counter: This counter tells us what the referenced address is in the RAM
- item counter: This counter performs a very important function which is to tell us what address we are going to write to when we are writing.
-read counter: This counter will tell us what address we will be reading.

- Then I will add a multiplexer that is connected to the RAM and contains two inputs one of them connected in write counter and the other one in read counter and one output, which is connected to the RAM.

-The D Flip Flop is by far the most important of all the clocked flip-flops. By adding an inverter (NOT gate) between the Set and Reset inputs, the S and R inputs become complements of each other ensuring that the two inputs S and R are never equal (0 or 1) to each other at the same time allowing us to control the toggle action of the flip-flop using one single D (Data) input.

-Also we have write button that are connected to an input of D Flip Flop, In Addtion read button in the side the same thing.

- In general, this is all about the first part of the project.

![Picture shown ](https://h.top4top.io/p_2607tdnqd1.jpeg)
![Picture shown 2 ](https://d.top4top.io/p_2607s7y211.jpeg)








### second section "Abdullah"

https://f.top4top.io/p_2607sbi2o1.png

We started connecting some of the AND gats here, specifically the middle AND GATE (blue wires). We connected its output with combined wire between Q2 & Q3 D Flip-Flop. Then we took a wire from that connection and connected it to the first select line in the Multiplexer (S0). And we also connected bothe Q0 & Q1 together (from the output pin of Q0 to the data pin of Q1).

https://j.top4top.io/p_2607eiwko1.png

Then we added a NOT GATE at the bottom and connected it with the clear button as its input and we took the NOT GATE output as an input for the bottom  AND GATE then we connected the output of that AND GATE to Q2 D Flip-Flop (at the clear pin).

Then we flipped the upper AND GATE to the left in order to connect its output with both of their QA of write counter & item counter.

We also removed an extra AND GATE (under Q0 D Flip-Flop) for the moment.


### third section "Faisal" 
And now the last part, we have added an NAND gate and connect it with the above
 nand and also connect it with an AND gate in the start of the circuit , we also added an 
AND gate and connect it with the  two NANDs that we have, and we added a NOT 
gate from the down NAND and connect It with an AND gate that is under (Q2) d flip flop,
and from the (Q3) d flip flop we connect it with the middle AND gate , now 
every thing is good we just have to add the ram and connect the address with the 
multiplixer and connect the ‘sel’ with the last OR gate and connect the id with the 
multiplixer and connect the ‘cir’ with the clear and finally we connect the ram 
with the last AND gate, last thing we have to do is adding the 4 data inputs and 
connect them with a splitter and connect it to the ram, after we finish that we will 
add the hex digit display and connect it with the ram

We know that there are some mistakes in our circuit but I think 90% of it is right ,
we have tried every thing we can do to make the circuit right but we ran out of time due to the exams and other projects 



### 
#### 

## 

## 
## Logic Expression
"Final image of the project"

![Our Awsome Project logic expression](https://f.top4top.io/p_2607t0d0v1.jpeg)

