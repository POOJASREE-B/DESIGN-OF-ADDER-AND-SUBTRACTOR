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
full adder
![image](https://github.com/user-attachments/assets/61a2cc6b-84cb-4c61-b177-66a95ab9d5f5)

full subtractor
![image](https://github.com/user-attachments/assets/dd941da4-362c-474a-b5fa-2437f5edd674)


**Procedure**


1)Create a New Project: *Open Quartus and create a new project by selecting "File" > "New Project Wizard." *Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2)Create a New Design File: *Once the project is created, right-click on the project name in the Project Navigator and select "Add New File." *Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3)Write the Combinational Logic Code: *Open the newly created Verilog or VHDL file and write the code for your combinational logic.

4)Compile the Project: *To compile the project, click on "Processing" > "Start Compilation" in the menu. *Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5)Analyze and Fix Errors: *If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window. *Review and fix any issues in your code if necessary. *View the RTL diagram.

6)Verification: *Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF". *Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All. *Give the Input Combinations according to the Truth Table and then simulate the Output Waveform.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:Poojasree B

RegisterNumber:212223040148
*/
full adder
```
module exp4(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule
```

full subtractor:
```
module exp4(diff,carry,a,b,c);
input a,b,c;
output diff,carry;
xor(diff,a,b,c);
assign carry= (~a)&c | (~a)&b | (b&c);
endmodule
```
**RTL Schematic**
![image](https://github.com/user-attachments/assets/11010c7f-2d0a-4347-bb93-632a1cdadaa4)


![image](https://github.com/user-attachments/assets/626569b1-97f4-4658-a5e2-4394b0d378fb)

**Output Timing Waveform**

![image](https://github.com/user-attachments/assets/a4e7aaca-c96b-4fcc-8425-c9ff72aef013)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.


