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

Full Adder:
<img width="429" height="395" alt="image" src="https://github.com/user-attachments/assets/b3eab467-7bb8-4510-95d5-d58c7985be81" />

Full Subtractor:

<img width="438" height="393" alt="image" src="https://github.com/user-attachments/assets/27885f76-dcfc-4bf0-8423-c73b8c655b39" />


**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**

````
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:MUTHUAKASH M
RegisterNumber:212225230194
````
Full Adder:
````
module fa(A,B,Cin,S,C);
input A,B,Cin;
output S,C;
assign S=A^B^Cin;
assign C=(A&B)|(A&Cin)|(B&Cin);
endmodule
````
Full Subtractor
````
module fs(A,B,Bin,diff,Borr);
input A,B,Bin;
output diff,Borr;
assign diff = A ^ B ^ Bin;
assign Borr = (~A & Bin) | (~A & B) | (B & Bin);
endmodule
````
**RTL Schematic**


Full Adder:

<img width="1119" height="729" alt="image" src="https://github.com/user-attachments/assets/eba1cede-9157-43b7-92b0-13dc9a2789fe" />


Full Subtractor:

<img width="818" height="476" alt="image" src="https://github.com/user-attachments/assets/7c662189-3fc8-4a6d-b897-33c12b5c1e67" />


**Output Timing Waveform**

Full Adder:

<img width="1919" height="606" alt="image" src="https://github.com/user-attachments/assets/d3649ff0-92e8-4fbc-b221-6cb7a1d9650e" />


Full Subtractor:

<img width="1918" height="450" alt="image" src="https://github.com/user-attachments/assets/4dbb31fb-1383-4791-933a-0025317ded63" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



