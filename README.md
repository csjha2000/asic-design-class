# Table of Contents 
- **TASK 1:** (16/07/24) [Create a simple C program and compile it using GCC.](#task-1)
- **TASK 2:** (16/07/24) [Compiling a C program using RISC-V compiler and optimize the compilation using O1 and Ofast.](#task-2)
- **TASK 3:** (19/07/24) [Perform debugging of the main section of the program and observe the values of register after each step of compilation.](#task-3)
- **TASK 4:** (22/07/24) [Identify various RISC-V instruction type (R, I, S, B, U, J)](#task-4)
- **TASK 5:** (22/07/24) [Execute assembly instructions using a given verilog code for a riscV processor and compare the waveform with Hardcoded instructions.](#task-5)
- **TASK 6:** (13/08/24) [Write a simple application in 'C' that can be compiled using GCC and RISC-V GCC.](#task-6)
      
  
# TASK 1 
( 16/07/2024 )
## AIM : To Create a simple C program and compile it using GCC followed by verification of the program output. 

### Step 1 : Open the text editor followed by assigning the name of the C program.

This can be done by giving the following command: 
```
leafpad sum1ton.c
```

Here leafpad is the text editor, sum1ton is the name of the file and at last .c represents that it is a C program.


![1](https://github.com/user-attachments/assets/188f3dea-68d2-489a-8db9-e4c6e11c8d39)


### Step 2 : Press enter and the text editor (leafpad) opensup as shown in the snapshot given below.


![2](https://github.com/user-attachments/assets/0283e5ea-978e-4200-b594-a206a8ad6a52)


### Step 3 : Write the required C program which calculates the sum from 1 to 5, as shown in the snapshot given below.


![3](https://github.com/user-attachments/assets/7f1386ba-74eb-4ef8-9a9f-0efb83338a0f)


### Step 4 : Press Ctrl + S in order to save the program that has been written.

### Step 5 : Now compile the program using GCC by giving the following command :
```
gcc sum1on.c
```
Press `ENTER`


![4](https://github.com/user-attachments/assets/c78c877c-a870-4ea8-bbca-517f5443fe0f)


### Step 6 : Now check the output of the program by giving the following command : 
```
./a.out
```

![5](https://github.com/user-attachments/assets/ffc1a40f-2449-4c0a-bce0-1c7add7d0427)


 ### Conclusion : In the above snapshot it is verified the program is compiled successfully and the result is also correct, that is 15 (1+2+3+4+5 = 15).


 # TASK 2  
 ( 16/07/2024 )
 ## AIM : To Compiling and executing a C program using RISC - V compiler and optimize the compilation using O1 and Ofast.

 ### Step 1 : Write a simple C program in the text editor (leafpad) and save it. You can see contents of the C program below.

 ![1](https://github.com/user-attachments/assets/a454ed04-8a3a-4d5d-9851-9b65a8e079d2)

 ### Step 2 : Now compile the C program using RISC - V compiler using O1 optimization as shown in the snapshot shown below.

 ![3](https://github.com/user-attachments/assets/8e2a2657-fb13-4f58-9373-45a07489fbb1)

 ### Step 3 : Now create the object file (.o) that is the output of the compiler as shown in the procedure shown below.

 ![4](https://github.com/user-attachments/assets/0831e910-36b1-4f02-a61c-2d25b38d0cd2)

 ### Step 4 : As soon as you enter the above command, a huge list of opcode is shown in the terminal.

 ### But we are interested in main section of the program so type : /main as shown below.
 ```
/main
```

 ![5](https://github.com/user-attachments/assets/445b3e20-13d8-458d-b978-2e23d11617a4)

 ### In the snapshot shown below we can see the opcode of the main section.

 ![6](https://github.com/user-attachments/assets/ee57f363-8fff-4dc3-87d0-623df1000896)

 ## Observation 1 : There are 15 lines of opcode in the main section.

 ### Step 5 : Now again compile the same program using RISC - V compiler but now optimise the compilation using Ofast as shown in the snapshot shown below.

 ![7](https://github.com/user-attachments/assets/9949fb6a-ad86-4898-8cfe-77001e6e8cdb)

### Step 6 : Now create the object file (.o) that is the output of the compiler as shown in the procedure shown below.

![8](https://github.com/user-attachments/assets/e5825259-3559-4278-abe3-634ee3be166b)

 ### Step 7 : As soon as you enter the above command, a huge list of opcode is shown in the terminal.

 ### But we are interested in main section of the program so type : /main as shown below.
```
/main
```

 ![9](https://github.com/user-attachments/assets/c1b48f69-5459-4f66-9489-a43f03a236e4)

  ### In the snapshot shown below we can see the opcode of the main section.

  ![10](https://github.com/user-attachments/assets/b85f864a-57d8-46f3-bc92-5a1a19579da2)

  ## Observation 2 : There are 12 lines of opcode in the main section.

  ## Conclusion : The compilation in the later procedure is optimised.


  # TASK 3  
  ( 19/07/2024 )
  ## AIM : To perform debugging of the main section of the previous program i.e. sum1ton.c and observe the values of register after each step of compilation.

  The assembly level of main section of the program sum1ton.c is shown below in the snapshot for reference.

  ![image](https://github.com/user-attachments/assets/57ba7087-8af4-4a01-a03e-e1d8070c62ba)

  ### Step 1 : First compile the code with Spike simulator. Then compare and verify the result from both the compilation techniques by giving the following code : 

  ```
spike pk sum1ton.o
```
![image](https://github.com/user-attachments/assets/3d9e14f9-ed05-4e2e-b4fc-067cbf7d0a9c)

OBSERVATION : The result from both the compilation techniques is same.

### Step 2 : Execute the sum1ton.o (i.e. object file) in the spike simulator in order to debug the code, by giving the following code :

```
spike -d pk sum1ton.o
```
![image](https://github.com/user-attachments/assets/34336a9b-3fd5-4975-b11d-e422696b8e3e)

 OBSERVATION : The debugging mode has been opened.

 ### Step 3 : Bring the pgrogram counter (pc) at the start of main by givving the following code: 
 ```
until pc 0 100b0
```
NOTE : 0x100b0 is the address of the start of the main function.

![image](https://github.com/user-attachments/assets/087c4b11-bb6d-4e26-b07b-e03910de6c68)

### Step 4 : Execute the following commands in order to check the contents of registor 'a2' before and after of running the instruction:

```
reg 0 a2
```
Press `Enter`

```
reg 0 a2
```
Press `Enter`

```
reg 0 a0
```
Press `Enter`

![image](https://github.com/user-attachments/assets/f24262ab-9aa5-496b-b2ff-90e9d4cc099d)



OBSERVATION : a2 and a0 registor is loaded by the given value and the addition took place.

### Step 5 : Verification of the addition.

Bring the program counter(pc) to address 0x100b8 where the addition will take place.

![image](https://github.com/user-attachments/assets/5afe0f90-8dfa-4744-a3be-543fa1d0809d)

Enter the following instruction : 
```
reg 0 sp
```
Press `Enter`
```
reg 0 sp
```

In the image shown below it is evident that the addition of (-16) took place and the value 10 ( 16 in decimal base and 10 in hexadecimal base ) has been deducted.

![image](https://github.com/user-attachments/assets/fdcc8a14-c367-4919-ba6c-8188eda6e9b6)

## Conclusion : The debugging process has been done and the process of addition has also been seen.

# TASK 4  
( 22/07/2024 )
## AIM : To Identify various RISC-V instruction type (R, I, S, B, U, J) and exact 32-bit instruction code in the instruction type format for the given RISC-V instructions.

### Various format types of RISC-V instruction are:
- R-format
- I-format
- S-format
- B-format
- U-format
- J-format

<img width="772" alt="3808 1535301636" src="https://github.com/user-attachments/assets/d6bb6e93-1cd1-4a3f-8bc1-2841d8d30f11">

### 1. R Type :
Used for arithmetic and logical operations that involve only registers.
![R](https://github.com/user-attachments/assets/5615e6f4-648f-4e0f-a33c-0181d9859e80)

- `funct7` (7 bits): Specifies the function of the instruction (e.g., ADD, SUB).
- `rs2` (5 bits): Source register 2.
- `rs1` (5 bits): Source register 1.
- `funct3` (3 bits): Specifies the function within the operation.
- `rd` (5 bits): Destination register.
- `opcode` (7 bits): Operation code indicating the type of instruction

### 2. I Type :  
Used for instructions that include an immediate value or involve load operations.
![I](https://github.com/user-attachments/assets/13bdecb2-7b55-4c22-afba-7a6fdb8636c9)

- `imm[11:0]` (12 bits): Immediate value, sign-extended to 32 bits.
- `rs1` (5 bits): Source register 1.
- `funct3` (3 bits): Specifies the function of the instruction.
- `rd` (5 bits): Destination register.
- `opcode` (7 bits): Operation code

### 3. S Type : 
Used for store operations
![S](https://github.com/user-attachments/assets/fd39c8cc-0ef8-4745-bd62-a58428aa1d0e)

- `imm[11:5]` (7 bits): Upper part of the immediate value.
- `rs2` (5 bits): Source register 2.
- `rs1` (5 bits): Source register 1.
- `funct3` (3 bits): Specifies the function of the instruction.
- `imm[4:0]` (5 bits): Lower part of the immediate value.
- `opcode` (7 bits): Operation code.

### 4. B Type : 
Used for branch operations.
![B](https://github.com/user-attachments/assets/5faf17d8-47c5-4ae6-8e76-84951ea323ac)

- `imm[12]` (1 bit): Most significant bit of the immediate value.
- `imm[10:5]` (6 bits): Upper part of the immediate value.
- `rs2` (5 bits): Source register 2.
- `rs1` (5 bits): Source register 1.
- `funct3` (3 bits): Specifies the function of the instruction.
- `imm[4:1]` (4 bits): Lower part of the immediate value.
- `imm[11]` (1 bit): Sign bit of the immediate value.
- `opcode` (7 bits): Operation code

### 5. U Type :
Used for instructions involving upper immediate values
![U](https://github.com/user-attachments/assets/3e9c9d86-6e71-46dd-980b-6e048a3494ed)

- `imm[31:12]` (20 bits): Immediate value, shifted left 12 bits.
- `rd` (5 bits): Destination register.
- `opcode` (7 bits): Operation code

### 6. J Type :
Used for jump instructions.
![J](https://github.com/user-attachments/assets/350ce493-7c33-4bfd-8390-5422b3e94e90)

- `imm[19]` (1 bit): Most significant bit of the immediate value.
- `imm[10:1]` (10 bits): Lower part of the immediate value.
- `imm[11]` (1 bit): Sign bit of the immediate value.
- `imm[18:12]` (7 bits): Upper part of the immediate value.
- `rd` (5 bits): Destination register.
- `opcode` (7 bits): Operation code.

## Identify various RISC-V instruction type (R, I, S, B, U, J) and exact 32-bit instruction code in the instruction type format for the given RISC-V instructions :

| S. No. | Assembly Instruction | Instruction format |         32 bit Instruction Code        | Hexadecimal representation|
|--------|----------------------|--------------------|----------------------------------------|---------------------------|
| 1.     | ADD r4, r4, r4       | R                  | 0000000 00100 00100 000 00100 0110011  |        0x00420233         |
| 2.     | SUB r4, r4, r4       | R                  | 0100000 00100 00100 000 00100 0110011  |        0x40420233         |
| 3.     | AND r4, r4, r4       | R                  | 0000000 00100 00100 111 00100 0110011  |        0x00427233         |
| 4.     | OR r8, r4, r5        | R                  | 0000000 00101 00100 110 01000 0110011  |        0x00526433         |
| 5.     | XOR r8, r4, r4       | R                  | 0000000 00100 00100 100 01000 0110011  |        0x00C323B3         |
| 6.     | SLT r00, r1, r4      | R                  | 0000000 00100 00001 010 00000 0110011  |        0x00424433         |
| 7.     | ADDI r02, r2, 5      | I                  | 000000000101 00010 000 00010 0010011   |        0x00510113         |
| 8.     | SW r2, r0, 4         | S                  | 0000000 00000 00010 010 00100 0100011  |        0x00012223         |
| 9.     | SRL r06, r01, r1     | R                  | 0000000 00001 00001 101 00110 0110011  |        0x0010D333         |
| 10.    | BNE r0, r0, 20       | B                  | 0000000 01000 00000 001 00000 1100011  |        0x00801063         |
| 11.    | BEQ r0, r0, 15       | B                  | 0000000 01111 00000 000 00000 1100011  |        0x00F00063         |
| 12.    | LW r03, r01, 2       | I                  | 000000000010 00001 010 00011 0000011   |        0x0020A183         |
| 13.    | SLL r05, r01, r1     | R                  | 0000000 00001 00001 001 00101 0110011  |        0x001092B3         |

## Conclusion : The instruction format type has been idendified for the given instruction and its 32 bit instruction code has also been found.

# TASK 5  
( 22/07/2024 )

## AIM : To execute assembly instructions using a given verilog code for a riscV processor and compare the waveform with Hardcoded instructions.

There is some variations in the ISA followed by RISCV and the hardcoded ISA for the below given instrucions. The differences are shown in the table below : 

|Assembly Instruction	      | Standard  RISCV  ISA	 | Hardcoded  ISA  |
|----------------|-------------------|--------------|
|ADD R4, R4, R4	 |32'h00420233       |32'h02208300  |
|SUB R4, R4, R4	 |32'h40420233       |32'h02209380  |
|AND R4, R4, R4	 |32'h00427233       |32'h0230a400  |
|OR R8, R4, R5	  |32'h00526433	      |32'h02513480  |
|XOR R8, R4, R4  |32'h00C323B3       |32'h0240c500  |
|SLT R00, R1, R4 |32'h00424433	      |32'h02415580  |
|ADDI R02, R2, 5 |32'h00510113	      |32'h00520600  |
|SW R2, R0, 4	 	 |32'h00012223	      |32'h00209181  |
|SRL R06, R01, R1|32'h0010D333	      |32'h00208681  |
|BNE R0, R0, 20  |32'h00801063	      |32'h00f00002  |
|BEQ R0, R0, 15  |32'h00F00063       |32'h00210700  |
|LW R03, R01, 2	 |32'h0020A183 	     |32'h01409002  |
|SLL R05, R01, R1|32'h001092B3 	     |32'h00520601  |

### Note : Since in the program there is Hardcoded ISA which is different from Standard RISC-V ISA, so the resultant waveform has some variation.

So now lets check out the waveform of the given instructions.

- 1. ` ADD R4, R4, R4 `
     The waveform for the above command using the provided verilog code is given below :

     ![1](https://github.com/user-attachments/assets/50c4e52a-2530-4578-9e99-4501a0d672a1)

     The waveform for the hardcoded command present in the code is given below :

     ![1 1](https://github.com/user-attachments/assets/34c51a07-5f64-4a89-9c09-a43ccd5c7418)

- 2. ` SUB R4, R4, R4 `
      The waveform for the above command using the provided verilog code is given below :

        ![2](https://github.com/user-attachments/assets/43dc9c01-ed72-4f49-814c-ffd30469d504)

     The waveform for the hardcoded command present in the code is given below :

     ![2 1](https://github.com/user-attachments/assets/93d006b0-911a-4325-85bc-351ff8efb641)

- 3. ` AND R4, R4, R4 `
     The waveform for the above command using the provided verilog code is given below :

     ![3](https://github.com/user-attachments/assets/e47123f4-6d60-4111-9e12-320ae038e654)

     The waveform for the hardcoded command present in the code is given below :

     ![3 1](https://github.com/user-attachments/assets/10c72c11-80a5-4c37-bb64-cdce287b8ff6)

- 4. ` OR R8, R4, R5 `
     The waveform for the above command using the provided verilog code is given below :

     ![4](https://github.com/user-attachments/assets/ac816748-b03b-48ef-80cf-97787d190f64)

     The waveform for the hardcoded command present in the code is given below :

     ![4 1](https://github.com/user-attachments/assets/2706aaa9-dcd0-4c3e-9a57-b73c4f08164b)

- 5. ` XOR R8, R4, R4 `
     The waveform for the above command using the provided verilog code is given below :

     ![5](https://github.com/user-attachments/assets/421dbaa9-2ded-459f-af46-812b90ae9346)

     The waveform for the hardcoded command present in the code is given below :

     ![5 1](https://github.com/user-attachments/assets/9094c376-87af-4bb5-bfd5-ca3793d11940)

- 6. ` SLT R00, R1, R4 `
     The waveform for the above command using the provided verilog code is given below :

     ![6](https://github.com/user-attachments/assets/5a78a98d-ee70-40cb-88e2-aef14845fb6d)

     The waveform for the hardcoded command present in the code is given below :

     ![6 1](https://github.com/user-attachments/assets/062942fc-251f-4528-810e-e7d93eeaa3f5)

- 7. ` ADDI R02, R2, 5 `

     The waveform for the above command using the provided verilog code is given below :

     ![7](https://github.com/user-attachments/assets/8f479709-ee1b-4c93-a924-ba06b81b7511)

     The waveform for the hardcoded command present in the code is given below :

     ![7 1](https://github.com/user-attachments/assets/b9c46699-f072-44f0-88a1-e705de90a3fd)

- 8. ` SW R2, R0, 4	`
     
     The waveform for the above command using the provided verilog code is given below :

     ![8](https://github.com/user-attachments/assets/a4ea040a-b73c-4974-95f0-7e9703a188a5)

     The waveform for the hardcoded command present in the code is given below :

     ![8 1](https://github.com/user-attachments/assets/6313d281-6508-47be-8310-2fabb739d812)

- 9. ` SRL R06, R01, R1 `

     The waveform for the above command using the provided verilog code is given below :

     ![9](https://github.com/user-attachments/assets/133a376d-feef-41fa-b52f-ba047de1c5c5)


     The waveform for the hardcoded command present in the code is given below :

     ![9 1](https://github.com/user-attachments/assets/7d5a77d6-8bd2-4ddc-ac9f-8f3b8294678b)

- 10. ` BNE R0, R0, 20 `

      The waveform for the above command using the provided verilog code is given below :

      ![10](https://github.com/user-attachments/assets/4babc4cd-33c3-4ca0-af85-7157c391ef93)


      The waveform for the hardcoded command present in the code is given below :

      ![10 1](https://github.com/user-attachments/assets/72791b08-a701-4295-8e63-aa891d5da6fa)

 - 11. ` BEQ R0, R0, 15  `

       The waveform for the above command using the provided verilog code is given below :

       ![11](https://github.com/user-attachments/assets/1279cb15-3891-44f6-bd62-dd6e8693c7ef)


       The waveform for the hardcoded command present in the code is given below :

       ![11 1](https://github.com/user-attachments/assets/2a6bc698-6a99-4165-83e6-bd3575c07ddc)

- 12. ` LW R03, R01, 2 `

      The waveform for the above command using the provided verilog code is given below :

      ![12](https://github.com/user-attachments/assets/8b86050b-b375-4bc9-9523-ad4b69365b33)

- 13. ` SLL R05, R01, R1 `

      The above command was not able to be executed as there was not enough memory spaces and the program was compiled with a warning ( as shown in the snapshot shown below ) :

      ![last](https://github.com/user-attachments/assets/f2ac6cfc-ad31-4562-bd1c-5afd5c8178aa)

  ## Conclusion : The given instruction was executed and the waveform difference was observed.


# TASK 6  
( 13/08/2024 )

## AIM : To write a simple application in 'C' that can be compiled using GCC and RISC-V GCC.
### APPLICATION : SIP CALCULATOR

INTRODUCTION : A Systematic Investment Plan (SIP) calculator in C can help you determine the future value of investments based on regular contributions and a specified rate of return. Below is a simple C program to calculate the future value of an SIP investment.

### Step 1 : Open the text editor and write the program in 'C' that calculates SIP for the given inputs. Save the file with extention '.c'. the snapshot of the code is given below.

```
#include <stdio.h>
#include <math.h>

int main() {
    double principal, annual_rate, amount, interest;
    int times_compounded, years;

    // Get user input
    printf("Enter the principal amount: $");
    scanf("%lf", &principal);

    printf("Enter the annual interest rate (in percentage): ");
    scanf("%lf", &annual_rate);

    printf("Enter the number of times interest is compounded per year: ");
    scanf("%d", &times_compounded);

    printf("Enter the number of years the money is invested or borrowed for: ");
    scanf("%d", &years);

    // Convert annual interest rate from percentage to decimal
    annual_rate = annual_rate / 100.0;

    // Calculate the compound amount
    amount = principal * pow((1 + annual_rate / times_compounded), times_compounded * years);

    // Calculate compound interest
    interest = amount - principal;

    // Display the results
    printf("Compound Interest: $%.2f\n", interest);
    printf("Total Amount after %.2d years: $%.2f\n", years, amount);

    return 0;
}
```
 ![image](https://github.com/user-attachments/assets/b5736332-bbba-446c-b2b5-ae39a10e5234)

 ### Step 2 : Compile it using GCC by giving the following series of command.

 ```
gcc sip_cal.c
```
Press ` ENTER `
```
./a.out
```
Press ` ENTER `

Enter the Inputs and then verify the output.

 ![image](https://github.com/user-attachments/assets/074d7dd9-d83b-4c87-945a-a13b50c3d9a3)

### Step 3 : Compile it using RISC-V GCC and verify the output using SPIKE by giving the following series of command.
```
riscv64-unknown-elf-gcc -O1 -o sip_cal sip_cal.c -lm
```
Press ` ENTER `
```
spike pk sip_cal
```
Press ` ENTER `

Enter the Inputs and then verify the Output.


![image](https://github.com/user-attachments/assets/f2dc6e8c-91ab-4107-b5fd-b76b9e330c0d)



 ### OBSERVATION : The output from both the compilation techniques results to same value for similar inputs given.

 ## CONCLUSION : The above application program has been compiled using GCC and RISC-V GCC which gave same output for the given set of inputs, thereby proving ' __O0=O1__'.


  



     


































 














