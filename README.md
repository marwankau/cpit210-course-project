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

![Our Awsome Project logic expression](/images/logic-expression.png)

