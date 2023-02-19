# CPIT210 Course Project ( GROUP 7 )
Introduction about your project, describe the problem, and your solution. Project truth tables, expressions, k-maps and any related task must included here. Also project documentation must included.

In this project students should work in groups of 3 to implement a fully functioning sequential circuit. 4-way light circuit. To design the circuit, Logisim should be used. Students should submit their software implementation and the report here. 

## Group Members
[comment]: <> (each group memeber should write his first, middle and last name with link to his GitHub account)
- [Saud Aljedani](https://github.com/Saudsaad5)
- [Saher Marsi](https://github.com/SaherMarsi)
- [Abdulkarim Alsahli](https://github.com/Abdulkarim-Alsahli)

[comment]: <> (Students should include the contribution percentage of each group member.)
[comment]: <> (Example:)
### Contribution:
- Saud 33%
- Saher 34%
- Abdulkarim 33%



## Traffic Light
### The Problem That Needs To Be Solved
This traffic light system will be a very simple one, using multiple flip-flops, decoders, and multiplexers. The problem we need to solve is creating a synchronized traffic light system using logisim. There's 4 different Traffic Lights in an intersection, we are required to make one traffic light turn from green ( GO! ) to yellow ( Slow! ) to Red ( Stop! ), once the cycle ends in one of the traffic lights, another cycle will begin in the next traffic light (East for example) and thus the cycle repeats again, just like a real life 4 way traffic system.

This is a good illustration that represents our problem, there's a total of 4 different traffic lights. All of which have different decoders.
The cycle should be from North (N) -> East (E) -> South (S) -> West (W).
![Traffic Light Example](https://user-images.githubusercontent.com/93139459/219962272-ddb7242a-f686-4e76-b5f0-6b2534ad2760.jpg)


### COMPONENTS USED
- 1 4-Bit Counter
- 1 1-Bit AND gate
- 1 NOT gate
- 2 Power sources
- 2 Grounding sources
- 6 Splitters
- 3 Multiplexers
- 3 D Flip-Flops
- 1 Clock
- 1 3-Bit Decoder
- 4 2-Bit Decoder
- 12 LEDs

### COMPONENTS EXPLANATION

### CIRCUIT EXPLANATION
Basically the 4 bit counter has two pathways we use, one is TA which is from the AND gate and the other is TG which is the carry, we used an AND gate and a splitter to distribute all the four bits, we then distributed the TA, TA',TG, grounding, and the power source all over the Multiplexers in order to combine and transmit the signals. Also the D FF are very important here, it is powered by a power source and connect to a clock; the D takes in the output of the multiplexers as an input, then all the Qs' are combined with the multiplexers' selectors via splitter for a more efficient approach. This is then taken into the 3x8 decoder which will control which traffic light should activate, 0 and 1 enables the west decoder which then starts a cycle from green to yellow then when not activated, it returns to the state of red, and for your information, the rest of the traffic lights (decoders) if they're not activated then they're automatically red. 2 and 3 enables the north decoder, 4 and 5 enables the east decoder, and finally 6 and 7 enables the south decoder. This is of course a never ending cycle just like the real deal! And that concludes our project. Thank you for your time. 
## Grading Factors
Each student's grade will defer from his group-mate 
- content and organization
- stating the problem need to be solved
- explanation of each component used
- explanation of whole circuit/integration of component
- how often you update/participate/contribute in group repository

## Deadline
Monday 29 / 7 / 1444 H, *20 Feb. 2023*

## Our Logic Expression
![PROJECT EXPORTED](https://user-images.githubusercontent.com/93139459/219938044-359ee041-689d-4429-9bce-a0c383a9438a.jpg)


