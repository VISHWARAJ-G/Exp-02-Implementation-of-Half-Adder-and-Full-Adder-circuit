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
![image](https://github.com/VISHWARAJ-G/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140417431/fd1fe551-60b5-4602-a6a3-27cf32de81ac)

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
# Program:
### Half_Adder
````
module Half_Full(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 
````
### Full_Adder
````
module Full_adder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule 
````
Logic symbol & Truthtable
RTL realization

# Output:
# RTL
### Half_Adder
![Half_adder RTL](https://github.com/VISHWARAJ-G/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140417431/ed742a6b-f771-44ab-88f6-8ca98711c41d)
### Full_Adder
![Full adder RTL](https://github.com/VISHWARAJ-G/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140417431/27fcc8e4-1ae6-49ff-b3ac-16bf71f833fc)

# TIMING DIAGRAM
### Half_Adder
![Half Adder output](https://github.com/VISHWARAJ-G/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140417431/8df1c4dd-e789-47a9-8acd-86f537ba3abc)
### Full_Adder
![Full_adder output](https://github.com/VISHWARAJ-G/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140417431/1e515c45-e8e6-40be-938c-d792e2b41a17)


# TRUTH TABLE 
### Half_Adder
![image](https://github.com/VISHWARAJ-G/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140417431/7632fcfd-1959-4502-8d21-9323c2319076)
### Full_Adder
![image](https://github.com/VISHWARAJ-G/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140417431/9c160433-0acd-4e5a-9194-6edfdfd25fe0)

# Result:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming
