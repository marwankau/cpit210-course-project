# Calculator Project:

### Introduction:
.
## Group Members

- [Baraa Majed Algomlas](https://github.com/Techiewicky)
- [Faisal Alzahrani](https://github.com/fsalzhrane)
- [Salman Balahwal](https://github.com/SalmanBalahwal)


### Contribution:
- Baraa Majed Algomlas 30%
- Faisal Alzahrani 40%
- Salman Balahwal 30%


## Problem Statement:



.

## Addition

### Half Adder:
Half Adder has two inputs, and it has two outputs which are the sum and carry. For example, if both inputs are 1 the output in sum will be 0 and the carry will be 1.

#### Half Adder Circuit:

![Our Project](Images/Half%20Adder.png)

### Full Adder using combined Half-Adder:


#### Full Adder Circuit:

![Our Project](Images/Full%20Adder.png.png)

### 8-bit parallel binary Adder:



#### 8-bit Adder Circuit:

![Our Project](Images/8-Bit%20Adder.png)

## Subtraction

### 8-bit parallel binary Subtractor:

Subtraction can be represented as adding a positive number to a negative number, for example: 4–2 = 4 + (-2) 
the real question is, how do we represent a negative number in binary?
One of the most efficient ways is to use 2’s complement which basically is to invert the added value and add 1 to the total.  
The way we will represent that in the Subtraction component we re-used the 8-bit adder the only difference is that the circuit inverts the B inputs and sets the carry input to 1.
As you can see, we added an enable button to control the circuit and to add 1 to the carry.

#### Components: 
- 8-Bit Adder
- Not gate
- Buffer
- Pin
#### Subtractor Circuit:

![Our Project](Images/Subtractor.png)


## Multiplication

### Multiplier Helper:

#### Multiplier Helper Circuit:

![Our Project](Images/Multiplier%20helper.png)

### Full Multiplier:

Now after we preform 8 by 1 bit in the multiplier helper all we need to do now is to expand this concept to 8 by 8 bit circle allowing us to multiply two 8-bit binary numbers.

To do so we need to use the multiplier helper many times….
.
.
.

#### Components:
- Multiplier Helper
- 8-bit parallel binary Adder


![8x8Multiplier](Images/Full%20Multiplier.png)




## Final Circuit Design:

![Our Project](Images/Full%20project.png)

#### Explanation:

