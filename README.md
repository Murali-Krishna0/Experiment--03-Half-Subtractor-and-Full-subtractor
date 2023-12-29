# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
1.Use module projname(input,output) to start the Verilog programming.
2.Assign inputs and outputs using the word input and output respectively.
3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.
4.Use each output to represent one for difference and the other for borrow.
5.End the verilog program using keyword endmodule
## Program:
```
module halfsub(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule
module fullsub(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign difference=(a^b^c);
assign borrow=(~a&(b^c)|(b&c));
endmodule
```
## Output:
## HALF SUBTRACTOR
![image](https://github.com/Murali-Krishna0/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149054535/8bffe79e-1b81-4880-9ea8-bd05857881bf)
## FULL SUBTRACTOR
![image](https://github.com/Murali-Krishna0/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149054535/216e7a91-1398-4fb0-8339-6b8587bc270b)

##  RTL realization
## HALF SUBTRACTOR
![image](https://github.com/Murali-Krishna0/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149054535/c831e216-dae7-4c91-afb0-33aa4d24e9f3)
## FULL SUBTRACTOR

![image](https://github.com/Murali-Krishna0/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149054535/dc6cb8e4-504c-4c18-80d9-7eb70423fade)



## Timing diagram 
## HALF SUBTRACTOR

![image](https://github.com/Murali-Krishna0/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149054535/360a12a7-216e-41b0-9b5c-d48180647b5c)

## FULL SUBTRACTOR

![image](https://github.com/Murali-Krishna0/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149054535/c41ec6c8-a871-4cb1-bba0-13a85952299b)
## RESULT
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.

