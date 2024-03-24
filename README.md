# FULL_ADDER
# Aim:
To simulate and synthesis full adder using vivado.

# Apparatus Required:
vivado software.

# Procedure:
STEP:1 Start the vivado software, Select and Name the New project.

STEP:2 Select the device family, device, package and speed. 

STEP:3 Select new source in the New Project and select Verilog Module as the Source type.

STEP:4 Type the File Name and module name and Click Next and then finish button. Type the code and save it. 

STEP:5 Select the run simulation adn then run Behavioral Simulation in the Source Window and click the check syntax.

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table. 

STEP:7 Select the Implementation in the Sources Window and select the required file in the Processes Window.

STEP:8 Select Check Syntax from the Synthesize XST Process. Double Click in the Floorplan Area/IO/Logic-Post Synthesis process in the User Constraints process group. UCF(User constraint File) is obtained. 

STEP:9 In the Design Object List Window, enter the pin location for each pin in the Loc column Select save from the File menu.

STEP:10 Double click on the Implement Design and double click on the Generate Programming File to create a bitstream of the design.(.v) file is converted into .bit file here.

STEP:12 Load the Bit file into the SPARTAN 6 FPGA 

STEP:11 On the board, by giving required input, the LEDs starts to glow light, indicating the output.

# Truth Table
![image](https://github.com/RESMIRNAIR/FULL_ADDER/assets/154305926/02ead8f5-d958-4c89-ac51-368ca086cf41)
# Circuit Diagram
![image](https://github.com/RESMIRNAIR/FULL_ADDER/assets/154305926/418e00aa-ed19-4ab3-a413-bae9575bff0e)

# Boolean Expression
![image](https://github.com/RESMIRNAIR/FULL_ADDER/assets/154305926/0c26fe47-d78c-43dd-ac0d-804e427a3bbc)

# Program
//full adder using data flow modelling
module full_adder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum = a^b^c;

assign carry = (a&b)|(b&c)|(c&a);

endmodule

//full adder using gate level modelling

module full_adder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

wire w1,w2,w3;

xor g1(w1,a,b);

and g2(w2,a,b);

xor g3(sum,w1,c);

and g4(w3,w1,c);

or g5(carry,w3,w2);

endmodule

# output:
![image](https://github.com/Shaiksushma123/FULL_ADDER/assets/159005642/c1c35c7a-48d0-477d-806c-1c2eae0c9b70)

# Result:
Thus the verilog program for full adder has been simulated and verified successfully using logic truth table.

