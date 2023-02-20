# CALCULATOR
## Our solution
This circuit is used to perform three arithmetic operations Addition, Subtraction, and Multiplication of two numbers with 8-bits , Implementation contains design of 1-bit full adder and 8-bit parallel binary adder combined of 1-bit full adder, 8-bit Subtraction, and 8-bit Multiplier implemented by using 1-bit full adder

## Group Members
[comment]: <> (each group memeber should write his first, middle and last name with link to his GitHub account)
- [Ghassan Alghamdi](https://github.com/ONLYGHASSAN)
- [Abdulelah Khoj](https://github.com/abdulelah-khoj)
- [Faris Aloufi](https://github.com/Farisaloufi)

[comment]: <> (Students should include the contribution percentage of each group member.)
[comment]: <> (Example:)
### Contribution:
- Ghassan 34%
- Faris 33%
- Abdulelah 33%




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

## Subtraction:
The subtraction contains two numbers; the numbers are input a and input b we take these two numbers and subtract them from each other by the 8-bit adder .
We take the number of a and take the number of b after taking the two’s complement then we add 1 to the new result b after that added a to the new result of b and then we have the output of the subtraction.it has to be that, input a greater than b.
For example, if we have a = 80 decimal in binary = 1010000 and we want to subtract  with b = 20 in decimal in binary = 0010100
 
We take the number of b and the two’s complement, we get 11010111
After that added 1 to the two’s complement of b and we get 1101100
Then we added the two numbers and 1010000 + 1101100= 0111100 = 60



![subtracter](https://user-images.githubusercontent.com/123258988/220190937-9b3139dc-0d62-48e1-bf0f-300b2ea94c08.jpeg)

## Multiplier:
the Multiplier consists of an 1 bit adder and each 1 bit adder have 2 input so we have an 8x8 1-bit adder and every 2 inputs have a AND gate the number of AND gates are 64gates connected to the adders
Let’s see how The Multiplication in binary works
First must know the 0 and 1 multiplication
0 × 0 = 0
0 × 1 = 0
1 × 0 = 0
1 × 1 = 1  

Now we will show the steps for the multiplication
1)    First multiply all the b inputs in a input.
2)    Secondly shift the b input 1 digit to the left and keep multiplying the inputs.
3)    Repeat those steps until you finish the 8 digits.
4)    After we finish the multiply now add a + b
5)    You have the final output
 
In this circuit, we have 7 adders and each sum of these adders goes down to the sum of the next adder until the last adder and sums and the cout reach the (high) part
The sum of the first adder of each row goes to the (low) part.
 
Let’s take some examples to make sure that we understand the concept
If we have 2 input A and B and A (00011110) B(1)
The output will be (00011110) and this called by an 8x1bit multiplier
Another example A(00000110) and B(00000010)
The result will be (00001100)



![Multi_Cal](https://user-images.githubusercontent.com/123325830/220191230-4c7c0dc6-76bf-43f2-8cae-fb3914248bb0.jpeg)

 
 


## Logic Expression - calculater_circuit
Include exported image from Logisim of your project here. *(Screenshot is not accepted!)*

![Our Awsome Project logic expression calculater_circuit]

![calculator](https://user-images.githubusercontent.com/123293486/220192003-17bd712d-d6a9-4baa-b055-e8d8b6e9f8cc.png)

