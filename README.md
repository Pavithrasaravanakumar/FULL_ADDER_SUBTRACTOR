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
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: S.Pavithra
RegisterNumber:212223220073
*/
//full adder
module fulladd(sum,cout,a,b,cin);
   output sum;
	output cout;
	input a;
	input b;
	input cin;
	
	      //Internal nets
 wire sl,cl,c2;

  //Instantiate logic gate primitives
 xor(sl,a,b);
 and(cl,a,b);
 xor(sum,sl,cin);
 and(c2,sl,cin);
 or(cout,c2,cl);
 
 endmodule
```

**RTL Schematic**
![Screenshot 2024-04-04 152522](https://github.com/Pavithrasaravanakumar/FULL_ADDER_SUBTRACTOR/assets/150664013/3eee00c7-af17-46e2-977b-c8b410bd0e19)

![Screenshot 2024-04-04 151153](https://github.com/Pavithrasaravanakumar/FULL_ADDER_SUBTRACTOR/assets/150664013/326dbf1a-f2ad-49ef-b9f1-1c4ed52e3b5b)


**Output Timing Waveform**
![Screenshot 2024-04-04 151607](https://github.com/Pavithrasaravanakumar/FULL_ADDER_SUBTRACTOR/assets/150664013/d8c4b476-e0c1-444b-bbb1-6ddfb9b08595)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



