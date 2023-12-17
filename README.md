Name:THENMOZHI P<br>
Reg.No:23005024

# Exp-03 Implementation of Half Adder and Full Adder circuit

# Implementation of Half Adder and Full Adder circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


## Half Adder

module exp3(sum, carry,a,b); 
input a,b; 
output sum,carry; 
xor sum1(sum,a,b); 
and carry1(carry,a,b); 
endmodule

## Truth Table
![WhatsApp Image 2023-11-27 at 16 05 12_b1129c8b](https://github.com/Naveen1825/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/138969868/d47375b8-4d29-4079-baff-57327446b4f2)
## RTL
![WhatsApp Image 2023-11-27 at 16 05 00_81ff270e](https://github.com/Naveen1825/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/138969868/48c80aac-3fb3-4f7b-b48c-03f4ff534cc7)

![WhatsApp Image 2023-11-27 at 16 05 07_2267e9af](https://github.com/Naveen1825/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/138969868/d51e1b0b-00ea-42d7-9e80-edca445d6ed1)

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 
![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)
#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.


## Full Adder

module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule
 
## Full Adder Truth Table
![WhatsApp Image 2023-11-27 at 16 05 33_636a0a53](https://github.com/Naveen1825/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/138969868/f54f679d-7b57-483a-a821-fbde70d4d0b1)

## RTL
![WhatsApp Image 2023-11-27 at 16 05 18_bae45d76](https://github.com/Naveen1825/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/138969868/7fb0d691-46f6-4f1e-b95d-1e77d47725ac)
![WhatsApp Image 2023-11-27 at 16 05 28_077dfe17](https://github.com/Naveen1825/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/138969868/421f82fe-551b-4fde-af0d-651d17ca8882)
## Result
Thus the given logic function verified using verilog programming
