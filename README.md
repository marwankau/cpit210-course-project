# CPIT210 Course Project
Introduction about your project, describe the problem, and your solution. Project truth tables, expressions, k-maps and any related task must included here. Also project documentation must included.

In this project students should work in groups of 3 to implement a fully functioning sequential circuit. This sequential circuit should work as a Buffer, a competition circuit, or 4-way light circuit depending on the student's choice. The idea of the three projects will be explained in the lab. To design the circuit, Logisim should be used. Students should submit their software implementation and the report here. 

## Group Members
[comment]: <> (each group memeber should write his first, middle and last name with link to his GitHub account)
- [First Member](https://github.com/first-member)
- [Second one](https://github.com/second-member)
- ...

[comment]: <> (Students should include the contribution percentage of each group member.)
[comment]: <> (Example:)
### Contribution:
- Ahmed 35%
- Fahad 35%
- Ali 30%

## Circuit Project topics:

[comment]: <> (Choose one of the following, your choice need to be accepted by Instructor)

### Buffer
#### Problem Statement
This circuit solves the reading and writing to buffer. For example: If we have input 4, we want to write it, buffer works like memory and stores it there when we click the write button. In case when we want to read from the buffer, by pressing read button, it starts reading from the first entry sored in the buffer. Buffer is nothing but a temporary memory. In addition, we can clear the contents from the buffer. Students are asked to design, and implement the required circuit.

Buffer also can be defined as a queue. It is managed by head and tail. Head is the current item
that we need to read. Where tail is address of the place we want to write into.

If queue is **full**: we can't write.

If queue is **empty**: we can't read.

To implement the queue in real world. We need a place that points to head and another place/address point to tail. Also we want to know number of elements that stored in the queue.

The following circuit diagram is sample of Queue/Buffer circuit.

![Buffer/Queue logic expression](/images/buffer-circuit.png)


### Calculator
#### Problem Statement
This circuit is used to perform three arthimatic operations Addition, Subtraction, and Multiplication of two numbers with 8 bits. Students required to build required components from the basic logic gates (AND, OR, XOR, NOT gates). Implementation should contains design of half adder, full adder, and 8 bits parallel binary adder. Subtraction and Multiplier should implemented using full adder as described in following diagrams. You are not allow to use pre-designed Adder, Subtractor, and Multiplier, you mush build them from scratch.

![Calculator, not allowed components](/images/calculator/not-accepted-arthimatic-components.png)

Implementation of Half Adder:

![Calculator, half adder implementation](/images/calculator/half-adder.png)

Implementation of Full Adder using combined Half-Adder:

![Calculator, full adder implementation](/images/calculator/full-adder.png)

Implementation of 4-bit parallel binary Adder using compination of 4 Full-Adder:

![Calculator, 4-bit parallel binary Adder implementation](/images/calculator/4-bit-adder.png)

From above design you can expaned it to implement **8-bit parallel binary adder**.

Implementation of 4-bit parallel binary Adder/Subtractor using compination of 4 Full-Adder:

![Calculator, 4-bit parallel binary Adder/Subtracor implementation](/images/calculator/4-bit-subtractor.png)



### Traffic Light
#### Problem Statement
This circuit is used to control a four-way traffic light control system. In what follows, it makes each traffic light work when it’s needed to be green or yellow and when it’s not (Red). Students are asked to design, and implement the required circuit.


![Traffic Light logic expression](/images/traffic/traffic-1.png)

### Finite State Machine for Traffic Light Control
![Traffic Light logic expression](/images/traffic/traffic-2.png)

### Transition Table
![Traffic Light logic expression](/images/traffic/traffic-3.png)

### Implements D's using 8x1 Multiplixers:
![Traffic Light logic expression](/images/traffic/traffic-4.png)

### Logic Circuit part 1
![Traffic Light logic expression](/images/traffic/traffic-5.png)

### Logic Circuit part 2
![Traffic Light logic expression](/images/traffic/traffic-6.png)

### Selected Topic
1. Traffic Light 
1. Buffer
1. Calculator

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

