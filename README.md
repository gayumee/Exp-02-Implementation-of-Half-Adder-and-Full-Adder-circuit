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
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: T. Gayathri
RegisterNumber:  212223100007
*/
## Half Adder 
module half_adder_dataflow (
  input a,   
  input b,    
  output s,   
  output c   
);

  assign s = a ^ b; 
  assign c = a & b;
endmodule

## Full Adder
module full_adder_s (
    input a,b,cin,
    output sum,carry
);
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        
and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);
or(carry,w2,w3,w4);     
endmodule 

## Logic symbol & Truthtable
## Half adder
![Exp3 truthtable (ha)](https://github.com/gayumee/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149037327/0fd7331b-93ab-4193-ab01-17fb2daac96f)
## Full adder 
![Exp3 truthtable (fa)](https://github.com/gayumee/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149037327/e37a36ab-6b59-4faa-a419-016053f4f78e)

## RTL realization
## Half adder
![Exp3 ha RTL diagram](https://github.com/gayumee/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149037327/2399ce4d-c29e-4907-871a-fe3659a8c52d)
## Full adder
![Exp3 fa RTL diagram](https://github.com/gayumee/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149037327/f3692347-7a64-4d1b-94b1-184cd842c665)

### Output:
### TIMING DIAGRAM
## Half adder
![exp3 ha wave](https://github.com/gayumee/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149037327/539197ab-8eb1-4c44-9962-e97d4d11f061)
## Full adder 
![exp 3 fa wave](https://github.com/gayumee/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149037327/3cf754f8-568e-44af-8e8a-1fb410198bf4)


### TRUTH TABLE 

### Result:
