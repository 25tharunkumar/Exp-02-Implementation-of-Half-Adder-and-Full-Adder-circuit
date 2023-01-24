# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
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

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
###
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Tharun kumar.M
RegisterNumber: 22002150 
Half Adder Verilog Code:

module half_adder(a, b, s, c);
input a, b;
output s, c;
xor(s, a, b);
and(c, a, b);
endmodule
Full Adder Verilog Code:

module full_adder(x, y, z, s, c, x1, x2, x3, x4);
input x, y, z;
output s, c, x1, x2, x3, x4;
xor(x1, x, y);
xor(s, x1, z);
and(x3, x, y);
and(x4, x1, z);
or(c, x3, x4);
endmodule
Logic symbol & Truthtable
RTL realization

### Output:
### RTL ![image](https://user-images.githubusercontent.com/123470785/214309425-c86a3e23-373a-46e3-a20c-e15ec40374f3.png)
![image](https://user-images.githubusercontent.com/123470785/214309622-f1d950f9-68f4-4d0c-a548-222d883649b6.png)

### TIMING DIAGRAM ![image](https://user-images.githubusercontent.com/123470785/214309809-2f94b772-ddfe-4219-98c0-21288893e2b5.png)
![image](https://user-images.githubusercontent.com/123470785/214310225-7edded7c-10fa-4e0e-89cf-83d5cd1c61da.png)



### TRUTH TABLE ![image](https://user-images.githubusercontent.com/123470785/214310428-dc671d0e-75f5-40ee-a5a1-4704a311259e.png)
![image](https://user-images.githubusercontent.com/123470785/214310556-6993650f-7f9b-4b31-9ab7-b64b774f2b73.png)



### Result:
