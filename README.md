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

FULL ADDER

![adder](https://github.com/user-attachments/assets/22e765a8-cc68-4b5f-9340-acf4d413b738)

FULL SUBTRACTOR

![sub](https://github.com/user-attachments/assets/5ccb9ac1-a6db-4c01-a7f7-f4f6f01ceaf8)



**Procedure**
```
Full Adder: 
1.Open Quartus II and create a new project. 
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

Full Subtractor: 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.
```
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:Hari sudhan S   RegisterNumber: 212224240048
*/
 exp4a-full adder

 *module exp4a(sum, cout, a, b, cin);*

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

Exp4b-full subtractor

*module fullsub(df, bo, a, b, bin);*

    output df;
    output bo;
    input a;
    input b;
    input bin;
    
	wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=(~a&b);
	 assign w3=(~w1&bin);
	 assign df=w1^bin;
	 assign bo=w2|w3;

endmodule


**RTL Schematic**
![Screenshot (173)](https://github.com/user-attachments/assets/e264e643-06a2-44a5-8ad9-2350e11a2a6b)

![Screenshot (174)](https://github.com/user-attachments/assets/e6c76635-b451-4719-bc8c-2720ae0f6696)


**Output Timing Waveform**
FULL ADDER 
![Screenshot (175)](https://github.com/user-attachments/assets/cbcdc725-a131-4da9-a243-f99760c62362)

FULL SUBBTRACTOR
![Screenshot (176)](https://github.com/user-attachments/assets/4383853e-2352-4d0f-85e5-9f0614d10d12)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



