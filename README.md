# NAME: NITHISH S
# REFRENCE NUMBER:23013509
# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.
###  Procedure
1. TYPE THE PROGRAM IN QUARTUS SOFTWARE.
2. COMPILE AND RUN THE PROGRAM.
3. GENERATE THE RTL SCHEMATIC AND SAVE THE LOGIC DIAGRAM.
4. CREATE NODES FOR  INPUTS AND OUTPUTS TO GENERATE THE TIMING DIAGRAM.
5. FOR DIFFERENT INPUT COMBINATIONS,GENERATE THE TIMING DIAGRAM
   
### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![292767957-3e6797d2-4064-4f2a-b129-752f103a15cc](https://github.com/Nithish23013509/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149038138/fe444606-cfe3-4b25-8b94-169195d6f96c)

```
module de3hafeez(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```

RTL REALIZATION
![292768055-52c27ea9-5035-4c57-95a6-726a3120e907](https://github.com/Nithish23013509/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149038138/f9f43422-de6b-4371-beb0-8144c64e2e69)
# TRUTH TABLE
![292768068-349a992b-f4f9-43fd-b366-7da7c7f8f50d](https://github.com/Nithish23013509/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149038138/3255d42c-841f-4972-a391-89b2372ca0a8)
# TIMING DIAGRAM
![292768086-d9b5f80a-c443-4184-90e2-f9e96e65b61c](https://github.com/Nithish23013509/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149038138/b256225d-762f-4af0-943d-782bc088a653)

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)


Program:
```
module de3_1(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b|b&c|a&c;
endmodule
```

# RTL realization
![292768176-7431f1b3-2a88-4938-b3b8-6e621aceea73](https://github.com/Nithish23013509/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149038138/3a800152-af35-4d1e-8c6c-45254a01ec31)

### TRUTH TABLE
![292768194-21f3b020-6b7d-4e2d-b204-9ccea072377e](https://github.com/Nithish23013509/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149038138/6e7f43e4-d835-4b36-a229-55313c12b867)


### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming.
