## Developed by : Kailash Kumar S
## Register Number : 212223220041
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
#### Figure -01 HALF ADDER:
 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)
#### Figure -02 FULL ADDER:
![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png) 

### Procedure:
Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:
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
## Output:
## Logic symbol & Truthtable:
## Half Adder:
![image](https://github.com/kailash2506/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149034874/03446362-314d-4448-bbbc-30e71fda1296)
## Full Adder:
![image](https://github.com/kailash2506/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149034874/4c0018cd-eb4a-490a-9f30-c9b96fed6dc1)
## RTL realization:
## Half Adder:
![image](https://github.com/kailash2506/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149034874/35bbce60-d4c4-4d11-aba6-c1cc1132f9b6)
## Full Adder:
![image](https://github.com/kailash2506/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149034874/c561642f-a2a8-4a69-b3c8-a6405b66cc78)
### TIMING DIAGRAM:
## Half Adder:
![image](https://github.com/kailash2506/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149034874/06fc324d-5708-4887-995c-d96f9c422c5b)
## Full Adder:
![image](https://github.com/kailash2506/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149034874/b5c34f1b-ecd6-4305-b8be-b4246c3a667b)
### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming
