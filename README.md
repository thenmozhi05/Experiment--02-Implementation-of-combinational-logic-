## Developed by: thenmozhi
## RegisterNumber:  23005024
# Experiment 02 Implementation of combinational logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime

## Theory:
A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.
## Procedure:
Create a New Project:
Open Quartus and create a new project by selecting "File" > "New Project Wizard."Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

Create a New Design File: *Once the project is created, right-click on the project name in the Project Navigator and select "Add New File." * * Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

Write the Combinational Logic Code:

* Open the newly created Verilog or VHDL file and write the code for your combinational logic.

4.Compile the Project:

* To compile the project, click on "Processing" > "Start Compilation" in the menu. *Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5.Analyze and Fix Errors:

* If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.

6.Verification:

* Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".

* Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.

* Give the Input Combinations according to the Truth Table and then simulate the Output Waveform.

## Program:
module experiment2(A,B,C,D,F1);
input A,B,C,D;

output F1;

wire x1,x2,x3,x4,x5;


assign x1=(~A)&(~B)&(~C)&(~C);

assign x2=(A)&(~D)&(~D);

assign x3=(~B)&(C)&( ~D);

assign x4=(~A)&(B)&(C)&(D);

assign x5=(B)&(~C)&(~D);

assign F1=x1|x2|x3|x4|x5;
endmodule

## RTL realization
![Screenshot 2023-11-26 173053](https://github.com/mounika2005/Experiment--02-Implementation-of-combinational-logic-/assets/145633112/21e1ae21-bf4e-4cf6-990c-04303e40d522)
# Truth table:
![Screenshot 2023-11-26 173233](https://github.com/mounika2005/Experiment--02-Implementation-of-combinational-logic-/assets/145633112/c6468b54-7ec8-4a38-b959-64b7df34c7e3)
# Timing Diagram:
![Screenshot 2023-11-26 173342](https://github.com/mounika2005/Experiment--02-Implementation-of-combinational-logic-/assets/145633112/4640dcf3-91e4-42c8-bf85-e0d7d05d2b63)
## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
