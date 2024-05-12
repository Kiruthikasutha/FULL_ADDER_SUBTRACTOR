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

**FULL ADDER:**
![Screenshot 2024-05-12 124442](https://github.com/Kiruthikasutha/FULL_ADDER_SUBTRACTOR/assets/144979570/81e5b20f-0777-4c09-aec4-6510aa10f8fd)

**FULL SUBTRACTOR:**

![Screenshot 2024-05-12 124500](https://github.com/Kiruthikasutha/FULL_ADDER_SUBTRACTOR/assets/144979570/07f34d45-8a43-4ab6-86f4-7c197096b47e)



**Procedure**

Write the detailed procedure here

~~~
**Full Adder:**
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

**Full Subtractor:** 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.
~~~


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:

~~~
module EX04(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;

//FULL ADDER
assign sum = a^b^c;
assign carry = (a&b) | (b&c) | (a&c);
wire a0;
not (a0,a);

//FULL SUBTRACTOR
assign DIFF = a^b^c;
assign BO = (a0&b) | (b&c) | (a0&c);
endmodule

Developed by: KIRUTHIKA M
RegisterNumber: 212223040098
~~~
*/

**RTL Schematic**

![Screenshot 2024-05-12 125255](https://github.com/Kiruthikasutha/FULL_ADDER_SUBTRACTOR/assets/144979570/323f09a9-42cf-488b-8600-ac314e5184bb)


**Output Timing Waveform**
![Screenshot 2024-05-12 125316](https://github.com/Kiruthikasutha/FULL_ADDER_SUBTRACTOR/assets/144979570/41cfb781-4fd6-4bfd-a90c-c825e5ce482c)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



