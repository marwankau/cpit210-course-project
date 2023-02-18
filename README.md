# CPIT210 Course Project
Introduction about your project, describe the problem, and your solution. Project truth tables, expressions, k-maps and any related task must included here. Also project documentation must included.

In this project students should work in groups of 3 to implement a fully functioning sequential circuit. This sequential circuit should work as a Buffer, a competition circuit, or 4-way light circuit depending on the student's choice. The idea of the three projects will be explained in the lab. To design the circuit, Logisim should be used. Students should submit their software implementation and the report here. 

## Group Members
[comment]: <> (each group memeber should write his first, middle and last name with link to his GitHub account)
- [Moath Khalid Alahmadi](https://github.com/MoaathK)
- [Maan Almazroei](https://github.com/MaanAlmazroei)
- [farez Alghazzawi](https://github.com/Farez-gh)

[comment]: <> (Students should include the contribution percentage of each group member.)
[comment]: <> (Example:)
### Contribution:
- Moath 33%
- Maan 34%
- Farez 33%

## Circuit Project topics:



Calculator
=================
#### Problem Statement
This circuit is used to perform three arthimatic operations Addition, Subtraction, and Multiplication of two numbers with 8 bits. Students required to build required components from the basic logic gates (AND, OR, XOR, NOT gates). Implementation should contains design of half adder, full adder, and 8 bits parallel binary adder. Subtraction and Multiplier should implemented using full adder as described in following diagrams. You are not allow to use pre-designed Adder, Subtractor, and Multiplier, you mush build them from scratch.

![Calculator, not allowed components](/images/calculator/not-accepted-components.png)

#### Half Adder

![Calculator, half adder implementation](/images/calculator/half-adder.png)

#### Full Adder using combined Half-Adder:

![Calculator, full adder implementation](/images/calculator/full-adder.png)

#### 4-bit parallel binary Adder using compination of 4 Full-Adders:

![Calculator, 4-bit parallel binary Adder implementation](/images/calculator/4-bit-adder.png)

From above design you can expaned it to implement **8-bit parallel binary adder**.

#### 8-bit parallel binary Subtractor using compination of 8-bit parallel binary adder:

![Calculator, Subtracor implementation](/images/calculator/subtractor.png)

An enable input to activate subtractor output or deactivate.

#### Multiplier

The implementation of multiplier contains several components. One of them is an AND gate with $b_i$ with every bit in $A$.

![Calculator, A AND b_i](/images/calculator/multipire-1.png)

You need to use above component several times to perform multiplication of 8-bits input with 8-bits input. Here an example of multipling 2-bits with 8-bits.

![Calculator, 2x8 multiplier](/images/calculator/multipire-2.png)

As you can see the outout is the total number of bits in the inputs (2 + 8). We mark the first 8 bits as ($lo$) bits and the remaining 2 bits as ($hi$).

Here another example of 8-bits input multiplied with 3-bits input:

![Calculator, 3 bits multiplied with 8 bits](/images/calculator/multipire-3.png)

So you need to repeate this pattern until to you complete the design of 8-bits for $B$.

#### Final Circuit Design

The following design is combination of all the three arthimatic operation. As you can see in diagram there is 2x4 Decoder to choose operation:

0: Addition
1: Subtraction
2: Multiplication

Each selection will activate only one operation and disable the other two operation.

![Calculator, Complete Calculator design](/images/calculator/final-diagram.png)


## Our Explanation 
### **Addition**
  
  
### **Subtraction**
  #### Function:
   The main function of this circuit is to subtract the values in the second variable from the first variable.
  #### Components:
   - 8-bit binary subtractor
   - Controlled buffer
  #### Subtractor:
   The circuit subtract two number from each other. There is two input “A” & “B”. the value in “B” is subtracted from the from the value in “A”. The output is controlled by a controlling buffer or what we call it “Enable”. 
   #### How it works:
   1. we make 2nd compliment on “B”. which means converting 1 to 0 and vice versa. 
  2. add 1 to B’ to become b’’.
  3. Now we add “A” with B’’ and we will get the result of the subtraction.
  #### Example for illustration:
  - A: 1110010 (Decimal =114)
  - B: 1000101 (Decimal = 69)
  - Now perform step1 on B 
  - B’: 0111010 
  - Then perform step2 on B’
  - B’’: 0111011
  - Then perform step3 add A on B’’.
  - A: 1110010
  - B’’: 0111011
  - ---------------- +
  - 0101101 (This equivalent to 45 Decimal)
  #### Finally:
  To subtract any other number those the steps to do it. In the final circuit they will be 4 input ‘A’ ‘B’ in the form of 8-bit input, ‘Cout’ input always 0 which in the circuit is ground. ‘Enable’ input is used to make the subtractor circuit on when the decoder choose number ‘2’. This makes sure there is no overlap between the other circuit.
  
  
### **Multiplication**
#### The Multiplier

#### Function
The function of the multiplier circuit in this project is to perform multiplication of two binary numbers 8 bits each. And It integrated in the final combination with two other circuits (Addition and subtraction circuits) to work together as a calculator. 

#### Components
- Half adder
- Full adder
- 8-bit binary adder
- 8x8 Multiplier

#### Multiplier
#### The 8x8 bits multiplier circuit consist of the following:
- Two inputs A & B, the number which is to be multiplied by the other number is called multiplicand (A) and the number multiplied is called multiplier (B). 
- Eight Logic circuits of input A and B, each consists of 8 AND gate.
- Seven 8-bit parallel binary Adders
- Two controlled buffer gates for enabling connecting to High and Low outputs

#### How it works?
Multiplication in binary numbers is performed by similar method of  multiplication of decimal number system.
The multiplication process of 8x8 bits is performed as follow:
1st. step: multiply the whole 8 bits of multiplicand (A) by the first digit of the multiplier (B).
2nd. step: multiply the whole 8 bits of multiplicand (A) by the second digit of the multiplier (B).
3rd. step: shift the result of second step to the left by one digit.
4th. step : repeat steps 1, 2 and 3 until completing the whole 8 digits of multiplier (B).
Finally: make summation for the above 8 multiplication results.

#### Example for illustration:
(/images/calculator/multiplication.png)

These steps are performed in the logic circuit by applying two inputs to AND gate representing Ai and Bi, the first digit of the product result in each step of multiplication is connected directly to the final output port of the multiplication circuit (by-passing the Adder). By the end of the multiplication process, the total number will be 8 digits which are named Lo Output.
The initial carry in is considered to be zero. The the subsequent carry out of each step is added to the next step. By the end of the multiplication process, the total number will be 8 lines which are named Hi Output.
In order to enable/disable the output of the multiplier, two controlled buffer gates are connected to the Lo and Hi outputs. The controlled buffer gate is three-state buffer, it works as a switch to switch ON or OFF the output based on the control signal (enable or disable).








### Selected Topic
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

![Our Awsome Project logic expression](/images/calculator/210-FinalProject.png)

