# FULL_ADDER_SUBTRACTOR

DHINESHKUMAR E ( 24900879 )

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

FULL ADDER :

![image](https://github.com/user-attachments/assets/e07c9c9a-37a9-4830-8afe-a4ef33f69544)

FULL SUBTRACTOR :

![image](https://github.com/user-attachments/assets/a65c4a4f-762a-4786-9d90-76f43e1c32e5)

**Procedure**

Write the detailed procedure here

**Program:**

FULL ADDER :

```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule 
```

FULL SUBTRACTOR :

```
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```

**RTL Schematic**

FULL ADDER :

![Screenshot 2024-12-11 052641](https://github.com/user-attachments/assets/e68340f9-f58a-4167-b7dc-ae9e79560f2d)

FULL SUBTRACTOR :

![Screenshot 2024-12-11 052801](https://github.com/user-attachments/assets/697d4ca4-8791-4ef1-8342-4ce423e3a70a)

**Output Timing Waveform**

FULL ADDER :

![Screenshot 2024-12-11 052845](https://github.com/user-attachments/assets/ca06618b-da94-4ba4-aad3-129adce1b9fe)

FULL SUBTRACTOR :

![Screenshot 2024-12-11 052942](https://github.com/user-attachments/assets/31e6118a-1689-4d96-b125-1f13a40c284c)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



