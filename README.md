# CPIT210 Course Project
Introduction about your project, describe the problem, and your solution. Project truth tables, expressions, k-maps and any related task must included here. Also project documentation must included.

In this project students should work in groups of 3 to implement a fully functioning sequential circuit. This sequential circuit should work as a Buffer, a competition circuit, or 4-way light circuit depending on the student's choice. The idea of the three projects will be explained in the lab. To design the circuit, Logisim should be used. Students should submit their software implementation and the report here. 

## Group Members
[comment]: <> (each group memeber should write his first, middle and last name with link to his GitHub account)
- [Ghassan Alghamdi](https://github.com/ONLYGHASSAN)
- [Abdulelah Khoj](https://github.com/abdulelah-khoj)
- [Faris Aloufi](https://github.com/Farisaloufi)

[comment]: <> (Students should include the contribution percentage of each group member.)
[comment]: <> (Example:)
### Contribution:
- Ahmed 35%
- Fahad 35%
- Ali 30%

# CALCULATOR


## Our solution
This circuit is used to perform three arithmetic operations Addition, Subtraction, and Multiplication of two numbers with 8-bits , Implementation contains design of 1-bit full adder and 8-bit parallel binary adder combined of 1-bit full adder, 8-bit Subtraction, and 8-bit Multiplier implemented by using 1-bit full adder

### 1-bit full adder 
inputs : 
- A
- B
- Carry in (Cin)

outputs : 
- Sum
- Carry out (Cout)

to design 1-bit full adder we use:
- NOT Gate
- AND Gate
- OR Gate

The full adder adds the three binary inputs (A, B, Cin) each with 1-bit . To produce the sum and carry out(Cout) . If one of the inputs has a value of 1 and the other values ​​are zero, then the result will be 1 for sum and zero for Cout, if two of the inputs have a value of 1 and the third input has a value of zero, then the result will be zero for sum and 1 for Cout, and if all inputs have a value of 1 then the result will be 1 for Sum and Cout



#### Examples
if the value of A = 1 , B = 0 and Cin = 0
the output will be 1 for sum and zero for Cout   
 
if the value of A = 1 , B = 1 and Cin = 0
the output will be zero for sum and 1 for Cout  
 
if the value of A = 1 , B = 1 and Cin = 1
the output will be 1 for sum and 1 for Cout   


![1-bit_adder_calculator](https://user-images.githubusercontent.com/123293486/220189469-442db8cf-3d30-440e-a363-78e5449b965d.png)

### 8-bits full adder
to design 8-bits full adder we use:
- 1-Bit full adder

We have used a combination of the 1-bit full adder to design the 8-bit full adder , this circuit use to add two inputs (A , B) each with 8-bits and the result will be 8-bits for sum and 1 bit for carry out
example : 
If A = 01000011 which is 67 in decimal and B = 00101011 which is 43 in decimal the sum will be 01101110 which is 110 in decimal 

![8-bit_adder_calculator](https://user-images.githubusercontent.com/123293486/220189524-00aefbd0-2bd8-4072-942b-3173aaa77eb9.png)

[comment]: <> (Choose one of the following, your choice need to be accepted by Instructor)





## Logic Expression - calculater_circuit
Include exported image from Logisim of your project here. *(Screenshot is not accepted!)*

![Our Awsome Project logic expression calculater_circuit](https://user-images.githubusercontent.com/123293486/219744083-ba5e0230-4e8d-44d2-8db3-dbfb538a8519.png)


