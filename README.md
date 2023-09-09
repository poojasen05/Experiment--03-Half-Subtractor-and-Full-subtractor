# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
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



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:O.Sirisha Reddy
RegisterNumber:212222230103
*/

## Half Subtractor:
```
module halfsubtractor(A,B,diff,borrow);
input A,B;
output diff,borrow;
assign diff = A^B;
assign borrow =((~A)&B);
endmodule
```
## Full Subtractor:
```
module fullsubtractor(A,B,bin,diff,borrow);
input A,B,bin;
output diff,borrow;
assign diff= A^B^bin;
assign borrow = ((~A)&B)|(b&bin)|((~a)&bin);
endmodule
```

## Output:
##  RTL realization
![56](https://github.com/Sriram8452/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118708032/28ba6a9f-71e8-4a95-a50a-d7563315b40f)

![58](https://github.com/Sriram8452/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118708032/9b7a0114-5de3-4438-8f00-579134bcbb72)


## Truthtable
![3](https://github.com/Sriram8452/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118708032/8e05cd36-6fc2-453b-99f6-63cfd452f4ca)
![4](https://github.com/Sriram8452/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118708032/fd4cb11b-b044-48cf-b69e-d333f170c91d)


## Output Waveform
![57](https://github.com/Sriram8452/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118708032/30794ed0-d3e9-4cfd-a3aa-5a99b3d5e278)
![59](https://github.com/Sriram8452/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118708032/898879f8-b551-4890-9c26-41a6e1b89fd0)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
