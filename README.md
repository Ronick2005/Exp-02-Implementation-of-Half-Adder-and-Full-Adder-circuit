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
Program:

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Ronick Aakshath P

RegisterNumber: 22007303

Half Adder Verilog Code:
```
module half_adder(a, b, s, c);
input a, b;
output s, c;
xor(s, a, b);
and(c, a, b);
endmodule
```
Full Adder Verilog Code:
```
module full_adder(x, y, z, s, c, x1, x2, x3, x4);
input x, y, z;
output s, c, x1, x2, x3, x4;
xor(x1, x, y);
xor(s, x1, z);
and(x3, x, y);
and(x4, x1, z);
or(c, x3, x4);
endmodule
```

Logic symbol & Truthtable
RTL realization

### Output:
### RTL
![](half_adder_rtl.png)
![](full_adder_rtl.png)
### TIMING DIAGRAM
![](half_adder_timingdiag.png)
![](full_adder_timingdiag.png)
### TRUTH TABLE 
![](half_adder_truthtable.png)
![](full_adder_truthtable.png)
### Result:
Thus implementation of half adder and full adder circuit are verified