# CPIT210 Course Project
Introduction about your project, describe the problem, and your solution. Project truth tables, expressions, k-maps and any related task must included here. Also project documentation must included.

In this project students should work in groups of 3 to implement a fully functioning sequential circuit. This sequential circuit should work as a Buffer, a competition circuit, or 4-way light circuit depending on the student's choice. The idea of the three projects will be explained in the lab. To design the circuit, Logisim should be used. Students should submit their software implementation and the report here. 

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
### first part-Arif

#### " Arif " 

- The project was divided into three parts, and I will explain my part in a simple way and support it with some illustrations.

- At first I have configured 3 counters in my circuit and each circuit performs a different function than the other, let's see the function of each counter..

1- write counter: This counter tells us what the referenced address is in the RAM
2- item counter: This counter performs a very important function which is to tell us what address we are going to write to when we are writing.
3-read counter: This counter will tell us what address we will be reading.

- Then I will add a multiplexer that is connected to the RAM and contains two inputs one of them connected in write counter and the other one in read counter and one output, which is connected to the RAM.

-The D Flip Flop is by far the most important of all the clocked flip-flops. By adding an inverter (NOT gate) between the Set and Reset inputs, the S and R inputs become complements of each other ensuring that the two inputs S and R are never equal (0 or 1) to each other at the same time allowing us to control the toggle action of the flip-flop using one single D (Data) input.

-Also we have write button that are connected to an input of D Flip Flop, In Addtion read button in the side the same thing.

- In general, this is all about the first part of the project.

![Picture shown ](https://h.top4top.io/p_26079ui5z1.jpeg)
![Picture shown 2 ](https://g.top4top.io/p_26072h2j61.png)








### second part-Abdullah

### third part-faisal
And now the last part, we have added an nand gate and connect it with the above
 nand and also connect it with an and in the start of the circ , we also added an 
and gate and connect it with the  two nands that we have, and we added a not 
gate from the down nand and connect It with an and that is under the  second  d flip flop,
and from the third d flip flop we connect it with the middle and , now 
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
Include exported image from Logisim of your project here. *(Screenshot is not accepted!)*

![Our Awsome Project logic expression](/images/logic-expression.png)

