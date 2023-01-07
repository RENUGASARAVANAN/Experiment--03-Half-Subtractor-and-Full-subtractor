# Experiment--03-Half-Subtractor-and-Full-subtractor
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

 Procedure
Write the detailed procedure here 

 Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

HALF SUBTRACTOR:

module HalfSub(a,b,difference,borrow);

input a,b;

output difference,borrow;

assign difference=(a^b);

assign borrow=(~a&b);

endmodule



FULL SUBTRACTOR:

module FullSub(a,b,c,difference,borrow);

input a,b,c;

output difference,borrow;

assign borrow=(~a&(b^c)|(b&c));

assign difference=(a^b^c);

endmodule


Developed by: S.RENUGA
RegisterNumber:  22008594


 Output
 RTL
 
 HALF SUBTRACTOR
 
 ![Screenshot (14)](https://user-images.githubusercontent.com/119292258/211151526-090438e9-6096-474c-a5df-7d32d601fd72.png)

 
FULL SUBTRACTOR


![Screenshot (20)](https://user-images.githubusercontent.com/119292258/211151561-234a00ea-0f4c-4d8f-ab9b-fa4c208ba034.png)



 Timing diagram 
 
 HALF SUBTRACTOR
 
 ![half subtracter](https://user-images.githubusercontent.com/119292258/211151586-9b7893f2-bcd0-4ffb-b936-7d1f9809ee85.png)

FULL SUBTRACTOR

![full subtracter](https://user-images.githubusercontent.com/119292258/211151612-5585ebdb-c9ee-4eee-9f50-ffcb03ddbae4.png)

TRUTH TABLE 

HALF SUBTRACTOR

![Screenshot (17)](https://user-images.githubusercontent.com/119292258/211151628-32aebc18-eefa-4eba-8082-6a393807ae96.png)


FULL SUBTRACTOR

![Screenshot (18)](https://user-images.githubusercontent.com/119292258/211151661-7dc97281-8802-456f-8833-444c92a3f413.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
