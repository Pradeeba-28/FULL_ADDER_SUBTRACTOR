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
FULL ADDER:  
<img width="429" height="395" alt="full adder" src="https://github.com/user-attachments/assets/f05e68e0-a04e-4daa-8c1d-892b6cb56c9b" />  

FULL SUBTRACTOR:  
<img width="438" height="393" alt="full subtractor" src="https://github.com/user-attachments/assets/4d0be6ee-ac26-4b02-a91d-5fad73b308c4" />

**Procedure**

Type the program in Quartus software.  

Compile and run the program.  

Generate the RTL schematic and save the logic diagram.  

Create nodes for inputs and outputs to generate the timing diagram.  

For different input combinations generate the timing diagram.  

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: V. PRADEEBA RegisterNumber: 25009895
*/
```
module ex4 (a,b,c,x,y,z,sum,dif,car,bor);
input a,b,c,x,y,z;
output sum,dif,car,bor;
assign sum = a^b^c;
assign car = a&b | a&c | b&c;
assign dif = x^y^z;
assign bor = ~x&z | ~x&y | y&z;
endmodule
```

**RTL Schematic**
<img width="1920" height="1080" alt="Screenshot (31)" src="https://github.com/user-attachments/assets/bae6a83c-98d7-4014-814f-7e7e395a8079" />

**Output Timing Waveform**
<img width="1920" height="1080" alt="Screenshot (33)" src="https://github.com/user-attachments/assets/5da46c38-7881-4a2f-be53-6faa6b2148c9" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



