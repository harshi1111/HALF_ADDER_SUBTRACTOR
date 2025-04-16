## NAME : HARSHITHA V
## REGISTER NO : 212223230074
## EX 3 : HALF ADDER AND SUBTRACTOR

**AIM:** 

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Truthtable**

![image](https://github.com/user-attachments/assets/47228683-2129-4a89-b3e7-5c041e592036)

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

![image](https://github.com/user-attachments/assets/a2fc7c96-cc55-4b47-96d3-80bd1b7ae735)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

```
module ex3(a,b,sum,carry,difference,bout);
input a,b;
output sum,carry,difference,bout;
assign sum = a ^ b;
assign carry = a & b;
assign difference = a ^ b;
assign bout = ~a & b;
endmodule
```
**RTL Schematic**

![image](https://github.com/user-attachments/assets/5556f99c-503c-40cd-b996-6728e0184153)

**Output/TIMING Waveform**


![image](https://github.com/user-attachments/assets/7debbd68-8ee6-4849-a540-0c904936448f)


**Result:**

Hence , successfully designed a half adder and half subtractor circuit and verified its truth table in Quartus using Verilog programming.
