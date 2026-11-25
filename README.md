# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**

``` Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:sairam v
RegisterNumber:212225230237
```
## Full Adder
```
module fa1_df(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule

```
## Full Subtractor
```
module full_subtractor(diff, borrow, a, b, bin);
  output diff;
  output borrow;
  input a;
  input b;
  input bin;
  assign diff = a ^ b ^ bin;
  assign borrow = (~a & b) | (~(a ^ b) & bin);
endmodule

```
**RTL Schematic**
## Full Adder
<img width="1177" height="744" alt="image" src="https://github.com/user-attachments/assets/ec28169c-5c98-47fa-b164-91affa57022e" /> 

## Full Subtractor
<img width="1351" height="542" alt="image" src="https://github.com/user-attachments/assets/68e3e418-bdb2-4fde-8741-f5d3da905419" />

**Output Timing Waveform**
## Full Adder
<img width="1920" height="1201" alt="image" src="https://github.com/user-attachments/assets/3a7903eb-919f-412e-9090-4db91b44a640" />

## Full Subtractor
<img width="1921" height="1201" alt="image" src="https://github.com/user-attachments/assets/a525a1a2-f69c-47d6-b7e6-b5184f9270ce" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



