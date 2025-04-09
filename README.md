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
![Screenshot 2025-04-09 132900](https://github.com/user-attachments/assets/876dc58b-0af7-4412-b3b9-25a56881c783)


**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram

**Program:**
```
FULL ADDER
module fulladder(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

FULL SUBRACTOR
module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**

**FULL ADDER**
![Screenshot 2025-04-09 133146](https://github.com/user-attachments/assets/16dd6743-a25d-41ba-b1f7-dba9ed8fd251)

**FULL SUBTRACTOR**
![Screenshot 2025-04-09 133402](https://github.com/user-attachments/assets/87101a6f-43ee-40d2-bf2a-05499c3b68c0)


**Output Timing Waveform**


**FULL ADDER**
![Screenshot 2025-04-09 133457](https://github.com/user-attachments/assets/4f75f63b-1e3d-472e-b672-16e2d9460bff)

**FULL SUBTRACTOR**
![image](https://github.com/user-attachments/assets/21172ba8-8398-441d-a858-cf20f2253c08)

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



