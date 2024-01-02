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
### Program:
```
module half_adder(A,B,C,S);
input A,B;
output S,C;
assign c=A&B;
assign S=A^B;
endmodule
module FullAdder(a,b,carryin,sum,carryout);
input a,b,carryin;
output sum,carryout;
wire x,p,q,r;
xor(x,b,carryin);
xor(sum,x,a);
and(p,a,b);
and(q,b,carryin);
and(r,a,carryin);
or(carryout,p,q,r);
endmodule
```

RTL realization

### Output:
# Logic symbol & Truthtable
![293334002-603405d1-6e6a-4e25-9d41-21ee7486e47c](https://github.com/Akshaya-SK/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149347593/e393143e-cad7-445a-8ea5-9391d31173fb)
![293334170-96ddd1a1-710e-44de-9d4f-0ec40ca49195](https://github.com/Akshaya-SK/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149347593/d80fa554-43f3-4fb8-8c98-c8cf96958454)

### RTL
![293334393-eddf84e3-d5bc-4ef5-9a73-ed83e5759da1](https://github.com/Akshaya-SK/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149347593/bee08e09-20aa-4157-88c4-dffb4fcd2659)
![293334589-526b9bdd-2746-4236-aefb-2c7cbf2ff453](https://github.com/Akshaya-SK/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149347593/69a06192-5c58-447e-9cac-6d8c5b044e76)

### TIMING DIAGRAM
![293334733-81757a56-2747-47c2-b7ac-4c1ac8bc3c4c](https://github.com/Akshaya-SK/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149347593/836e1ea9-fb90-4e6d-bf9a-6eaf64058568)
![293334893-36a9174d-ef20-4010-a456-15194746754d](https://github.com/Akshaya-SK/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149347593/9e10500b-dc45-428f-80ce-a6c8f2f527e6)

# RESULT:
Thus the given logic functions are implemented and their operations are verified using verilog programming
### TRUTH TABLE 

### Result:
