# CPIT210 Course Project
Introduction about your project, describe the problem, and your solution. Project truth tables, expressions, k-maps and any related task must included here. Also project documentation must included.

In this project students should work in groups of 3 to implement a fully functioning sequential circuit. This sequential circuit should work as a Buffer, a competition circuit, or 4-way light circuit depending on the student's choice. The idea of the three projects will be explained in the lab. To design the circuit, Logisim should be used. Students should submit their software implementation and the report here. 

## Group Members
[comment]: <> (each group memeber should write his first, middle and last name with link to his GitHub account)
- [Suhaib Alghamdi](https://github.com/SuhaibAG)
- [Abdulaziz Khalifah](https://github.com/its-Abdulaziz)
- [Meshal Alghamdi](https://github.com/Meshal-Alghamdi)

[comment]: <> (Students should include the contribution percentage of each group member.)
[comment]: <> (Example:)
### Contribution:
- Suhaib 
- Abdulaziz 
- Meshal

## Circuit Project topics:

[comment]: <> (Choose one of the following, your choice need to be accepted by Instructor)

### Buffer
#### Problem Statement
This circuit solves the reading and writing to buffer. For example: If we have input 4, we want to write it, buffer works like memory and stores it there when we click the write button. In case when we want to read from the buffer, by pressing read button, it starts reading from the first entry sored in the buffer. Buffer is nothing but a temporary memory. In addition, we can clear the contents from the buffer. Students are asked to design, and implement the required circuit.

### Solution
before we started on the project we split it into multiple parts while through out the project we stayed in contact to advice and fix eachothers problems, each person mainly held a piece of the project to implement into logism

#### Part 1: (Suhaib)
In this part after we planned out our board I went ahead and started defining all the devices that we need for the project.

I started by adding 3 counters into the circuit, the first counter is the Item counter this counters job is to tell us which address we are pointing at in the ram. The second counter is the Write counter, this counters job is to tell us which address we will write into when we make a write opreation.
And in the same sense the Read counter will tell us which address we are reading from.

After that i added 4 D Flip Flops these filp flops will manage most of the operations in the circuit and through them the circuit will be truly defined.
Then I added 2 buttons one for writing which I connected to the "0" flip flop and a read button which connected to the "2" flip flop.

After that I added a multiplexer which will take 2 inputs read and write, and depending on which of the 2 a different operation will occur.
And then I defined a piece of 16Bits RAM with 4 address bits and 4 data bits, and I connected a Hex digit display that shows the bit we are reading when the read button is pressed. Then finally I added a clear button that will be used to reset the entire circuit.

![CPIT_210_BUFFER_(1 0)](https://user-images.githubusercontent.com/123287867/219379025-3e13cea3-b2d5-48a2-abfd-5a8babde9862.png)

#### Part 2: (Abdulaziz)
Here we started make the devices we made in the previous part communicate with each other to perform the jobs we want them to do. 

In the begging, we connected the output “value” of the item counter which is 4-bits to a NAND gate, this NAND gate will output 0 only when the item counter becomes full, as a result, the flip flop “0” which is responsible to writing in memory, will get 0 as an input, and that’s means when we click the write button, 0 is passed to flip flop “1”  after this writing operation is refused.
In the other hand, when the output is 1, writing operation is proceed and the write and item counter will increment. 

Same as writing opreation, item counter will send the value to an OR gate, the output will be 0 only if the item counter is empty, this output is connected to “q2” to determine the availability of the data in the RAM. If output is 1, reading operation will occur, “Q2”  and “Q3” will be inputs for an AND gate to increment the read counter.

About the multiplexer, it got in input from “Q2” to determine that we writing or reading from the RAM. 

Also, we connected the clear button with all the counters, and “Q0” and “Q2”  as it became 1, all counters are reseted. 

However, The clock button is responsible to control most of the operations of the circuit, making the clock button connected to flip	flops “1” and “3” and all the counters, it gives as the response when every puls happened.

![part2](https://user-images.githubusercontent.com/93838404/219731942-a1b9d6f4-ed40-4975-a757-1cae05a8adb8.png)


#### Part 3: (Meshal)
in this particular part I will be talking about the RAM, how every opreation will work and how we attached everything to it.
Before starting, we have fixed two bugs from part 2. One on the left side and one on the other side.

We created a RAM cosist of 16 addresses. each address will hold 4-bits with maximum value being 15.

In order to know which location we are writing\reading from we have attached the address of the RAM to the output of the multiplexer. We have also taken the values
which to be stored in the RAM from the inputs.

The store value will be used for the write opreation which it is attached using OR gate between Q0 and Q1, if the write opreation is correct the value will be stored. Otherwise it will not.

Chip select is attached to the flip-flops using AND gate, to make sure we are writing\reading the right value. We also attached the clock value to the clock so we can update values by switching from 0 to 1.

The load value will be used for the read opreation which it is attached from the multiplexer's selectd source. if the write opreation is correct it will check if there are values in the RAM or not, if yes it will read it. Otherwise it will not. Also, we have attached the clear value to the clear button just to reset the RAM.

Lastly, attaching the data value to the 7-segmat so we can present the current value in RAM.

![CPIT_210_BUFFER_3 0](https://user-images.githubusercontent.com/123258447/219868167-e39e6515-fb33-4f0d-a261-5d766ab22cbb.png)


## Selected Topics
1. Traffic Light
2. Competition
3. Buffer

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


