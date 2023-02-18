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
- Write counter
- Read counter
- Item counter
- D F/F
- Multiplexer
- Data input && Data output
- CLR button
- Clock
- Splitter
- Logic Gate (AND – OR – NAND – NOT)
- Power
- RAM and Hex digit display.

### Explanation of Whole Circuit:
#### 1- First counter is the write counter(tail of queue):
It’s the counter of the write address so when you add a number on address of 4-bit then press the write button that mean you want to write and add a number of the element on the tail (enqueue)  of the queue (start of the queue). that mean the counter of writing will increment by '1' for each press on the writing button until we reach the 16 element.

![image](https://user-images.githubusercontent.com/77943208/219878508-5e59dd6f-7f96-4ff1-b6b3-90ea7e03f797.png)

#### 2- read counter (head or front of queue):
It’s the counter of the read address so the function of this counter is for reading first element you add (if its not empty) from the top(front) of the buffer queue (dequeue), so then it will do increment by '1' also for each press on the read button.

![image](https://user-images.githubusercontent.com/77943208/219878603-796197d1-d9dc-41a1-9a27-b8c17413e33d.png)

#### 3- items counter:
![image](https://user-images.githubusercontent.com/77943208/219879631-8035ff24-296a-4d6f-b534-fb4f58dff90c.png)

This FF is responsible for every adding element, so its function is to count every element in buffer(queue) after and before each prosses of read and write.

In every write prosses the counter of element will also increment by '1' as the write counter until it reach to 16 input data(address) then it will be full thats why we implement this NAND gate.

![image](https://user-images.githubusercontent.com/77943208/219879790-7a5a57f5-5afb-45f7-b275-d6cc23aa8d9c.png)


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

