# Table of Contents 
- **TASK 1:** [Create a simple C program and compile it using GCC.](#task-1)
- **TASK 2:** [Compiling a C program using RISC-V compiler and optimize the compilation using O1 and Ofast.](#task-2)
- **TASK 3:** [Perform debugging of the main section of the program and observe the values of register after each step of compilation.](#task-3)
- **TASK 4:** [Identify various RISC-V instruction type (R, I, S, B, U, J)](#task-4)
- **TASK 5:** [Execute assembly instructions using a given verilog code for a riscV processor and compare the waveform with Hardcoded instructions.](#task-5)
- **TASK 6:** [Write a simple application in 'C' that can be compiled using GCC and RISC-V GCC.](#task-6)
- **TASK 7:** [Building a 5-stage pipelined RISC-V processor.](#task-7)
- **TASK 8:** [RISC-V Pre synthesis simulation using IVerilog and GTKWave.](#task-8)
- **TASK 9:** [RISC-V Pre synthesis Analog simulation using IVerilog and GTKWave.](#task-9)
- **TASK 10:** [RTL design using Verilog with SKY130 Technology Workshop.](#task-10)
- **TASK 11:** [Synthesize RISC-V and compare output with functional simulations.](#task-11)
- **TASK 12:** [Static Timing Analysis for Synthesized Risc-V Core using OpenSTA. ](#task-12)
- **TASK 13:** [PVT Corner Analysis for Synthesized VSDBabySoC using OpenSTA](#task-13)
- **TASK 14:** [Advanced Physical Design using OpenLane using Sky130](#task-14)
- **TASK 15:** [OPEN-ROAD PHYSICAL DESIGN for VSDBabySoC](#task-15)

# TASK 1      
( 16/07/2024 )

<details>
       <summary>Create a simple C program and compile it using GCC followed by verification of the program output.</summary>

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

</details>

# TASK 2  
( 16/07/2024 )

<details>
      <summary> Compile and execute a C program using RISC - V compiler and optimize the compilation using O1 and Ofast.</summary>
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

</details>

# TASK 3  
( 19/07/2024 )

<details>
      <summary>Perform debugging of the main section of the program i.e. sum1ton.c and observe the values of register after each step of compilation.</summary>
      
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

</details>

# TASK 4  
( 22/07/2024 )

<details>
      <summary>Identify various RISC-V instruction type (R, I, S, B, U, J) and exact 32-bit instruction code in the instruction type format for the given RISC-V instructions.</summary>
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

</details>

# TASK 5  
( 22/07/2024 )

<details>
      <summary>Execute assembly instructions using a given verilog code for a riscV processor and compare the waveform with Hardcoded instructions.</summary>
      
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
Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
Attach files by dragging & dropping, selecting or pasting them.

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
Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
Attach files by dragging & dropping, selecting or pasting them.

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
Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
Attach files by dragging & dropping, selecting or pasting them.

     The waveform for the above command using the provided verilog code is given below :

     ![5](https://github.com/user-attachments/assets/421dbaa9-2ded-459f-af46-812b90ae9346)

     The waveform for the hardcoded command present in the code is given below :

     ![5 1](https://github.com/user-attachments/assets/9094c376-87af-4bb5-bfd5-ca3793d11940)

- 6. ` SLT R00, R1, R4 `
     The waveform for the above command using the provided verilog code is given below :

     ![6](https://github.com/user-attachments/assets/5a78a98d-ee70-40cb-88e2-aef14845fb6d)

     The waveform for the hardcoded command present in the code is given below :

     ![6 1](https://github.com/user-attachments/assets/062942fc-251f-4528-810e-e7d93eeaa3f5)
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
Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
Attach files by dragging & dropping, selecting or pasting them.


     The waveform for the hardcoded command present in the code is given below :

     ![6 1](https://github.com/user-attachments/assets/062942fc-251f-4528-810e-e7d93eeaa3f5)

- 7. ` ADDI R02, R2, 5 `

     The waveform for the above command using the provided verilog code is given below :
Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
Attach files by dragging & dropping, selecting or pasting them.


     The waveform for the hardcoded command present in the code is given below :

     ![6 1](https://github.com/user-attachments/assets/062942fc-251f-4528-810e-e7d93eeaa3f5)

- 7. ` ADDI R02, R2, 5 `

     The waveform for the above command using the provided verilog code is given below :
Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
Attach files by dragging & dropping, selecting or pasting them.


- 7. ` ADDI R02, R2, 5 `

     The waveform for the above command using the provided verilog code is given below :
Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
Attach files by dragging & dropping, selecting or pasting them.

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

</details>

# TASK 6  
( 13/08/2024 )
<details> 
      <summary>Simple application in 'C' that can be compiled using GCC and RISC-V GCC.</summary>
      
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
</details>

# TASK 7  
( 15/08/2024 )

<details>
      <summary> Digital Logic with TL Verilog and Makerchip. (Day 3) </summary>

#  Combinational Logic 
## Implementing a CALCULATOR based on Combinational Logic.

Code snippet is given below:
( Insert this snippet under the TLV section in Makerchip IDE )
```
   $reset = *reset;

   $clk_CHA = *clk;

   //define smaller random numbers 4bit and assign to val1/val2
   // 31-4 bits of val1/val2 will be zero and 0-9 bits will be rand1/rand2 values
   
   $val1[31:0] = $rand1[3:0];
   $val2[31:0] = $rand2[3:0];
   $op[1:0] = $rand3[1:0];
   $sum[31:0] = $val1[31:0] + $val2[31:0];
   $diff[31:0] = $val1[31:0] - $val2[31:0];
   $prod[31:0] = $val1[31:0] * $val2[31:0];
   $quot[31:0] = $val1[31:0] / $val2[31:0];
   $out[31:0] =
         ($op == 0)
           ? $sum[31:0] :
         ($op == 1)
           ? $diff[31:0] :
         ($op == 2)
           ? $prod[31:0] :
         ($op == 3)
           ? $quot[31:0] :
         //default
           32'b0;

   // Assert these to end simulation (before Makerchip cycle limit).
   *passed = *cyc_cnt > 40;
   *failed = 1'b0;
```
The snapshot of the implementation of the above code for combinational circuit in Makerchip platfrom is shown below.

We can also observe the generated block diagram as well as the waveform for the simulation of our circuit.

![Combinational calculator](https://github.com/user-attachments/assets/7b66913c-3495-46df-bcab-cbb965182997)


#  Sequential Logic 
## Implementing a CALCULATOR based on Sequential Logic.

Code snippet is given below:
( Insert this snippet under the TLV section in Makerchip IDE )

```
   |calc
      @0
         $reset = *reset;
         
         $clk_CHA = *clk;
         
         $val1[31:0] = >>1$out[31:0];
         $val2[31:0] = $rand2[3:0];
         $op[1:0] = $rand3[1:0];
   
         $sum[31:0] = $val1[31:0] + $val2[31:0];
         $diff[31:0] = $val1[31:0] - $val2[31:0];
         $prod[31:0] = $val1[31:0] * $val2[31:0];
         $quot[31:0] = $val1[31:0] / $val2[31:0];
      
         $out[31:0] = $reset ? 32'b0 : (($op[1:0]==2'b00) ? $sum :
                                       ($op[1:0]==2'b01) ? $diff :
                                       ($op[1:0]==2'b10) ? $prod : $quot);
                         
   // Assert these to end simulation (before Makerchip cycle limit).
   *passed = *cyc_cnt > 40;
   *failed = 1'b0;
```

The snapshot of the implementation of the above code for sequential circuit in Makerchip platfrom is shown below.

We can also observe the generated block diagram as well as the waveform for the simulation of our circuit.

![image](https://github.com/user-attachments/assets/7d3d8c8b-65bd-42bc-a18d-a9d9fbb11839)

#  Pipelined and Validity Logic 
## Implementing a Error Detector based on Pipelined Logic.

Code snippet is given below:
( Insert this snippet under the TLV section in Makerchip IDE )

```
   $reset = *reset;
   
   $clk_CHA = *reset;
   
   |comp
      ?$valid
         @1
            $err1 = $bad_input | $illegal_op;
         @3
            $err2 = $err1 | $over_flow;
         @6
            $err3 = $err2 | $div_by_zero;

   // Assert these to end simulation (before Makerchip cycle limit).
   *passed = *cyc_cnt > 40;
   *failed = 1'b0;
```

The snapshot of the implementation of the above code for pipeline logic in Makerchip platfrom is shown below.

We can also observe the generated block diagram for the simulation of our circuit.

![image](https://github.com/user-attachments/assets/90c30806-8a88-47bb-9100-e82f9f930f53)

</details>
  
<details>
      <summary> Basic RISC-V CPU Micro-architechture. (Day 4) </summary>
      
# Basic RISC-V CPU micro-architecture

The block diagram of a basic RISC-V microarchitecture is as shown in figure below. Now, using the Makerchip platform the implementation of the RISC-V microarchitecture or core is done. For starting the implementation a starter code present in reference is used. The starter code consist of :

- A simple RISC-V assembler.
- An instruction memory containing the sum 1..10 test program.
- Commented code for register file and memory. 
- Visualization.

![image](https://github.com/user-attachments/assets/5d8f11e1-4e7c-4177-aa88-2f1f5346f7ba)

# Fetch and Decode :

Designing of processor is based on three core steps fetch, decode and execute :

Here we gonna design RiscV Cpu Core for which block diagram is given below :

![image](https://github.com/user-attachments/assets/6ad1bbb8-d6ec-41cc-9f1a-9ee8b2e31b9b)

## Fetch 

During the fetch stage, processors fetches the instruction from the memory to the address pointed by the program counter. The program counters holds the address of the next stage, in our case it is after 4 cycle and the instruction memory holds the set of instruction to be executed. 

Code snippet is given below:
( Insert this snippet under the TLV section in Makerchip IDE )

```
|cpu
      @0
         $reset = *reset;
         $clk_CHA = *clk;
         $pc[31:0] = >>1$reset ? 32'b0 : (>>1$pc + 32'd4);
         
      @1
         $imem_rd_en = !$reset;
         $imem_rd_addr[M4_IMEM_INDEX_CNT-1:0] = $pc[M4_IMEM_INDEX_CNT+1:2];
         $instr[31:0] = $imem_rd_data[31:0]; 
```

Snapshot of Fetch stage in maker chip:

![image](https://github.com/user-attachments/assets/e6c76e4b-ff50-4aa5-834a-900e00f59c39)

## RISC-V instruction file Decode Logic:

Code snippet is given below:
( Insert this snippet under the TLV section in Makerchip IDE )

```
|cpu
      @0
         $reset = *reset;
         $clk_CHA = *clk;
         $pc[31:0] = >>1$reset ? 32'b0 : (>>1$pc + 32'd4);
         
      @1
         $imem_rd_en = !$reset;
         $imem_rd_addr[M4_IMEM_INDEX_CNT-1:0] = $pc[M4_IMEM_INDEX_CNT+1:2];
         $instr[31:0] = $imem_rd_data[31:0]; 
         $is_i_instr = $instr[6:2] ==? 5'b0000x ||
                       $instr[6:2] ==? 5'b001x0 ||
                       $instr[6:2] ==? 5'b11001 ||
                       $instr[6:2] ==? 5'b11100;
         $is_r_instr = $instr[6:2] ==? 5'b01011 ||
                       $instr[6:2] ==? 5'b0x100 ||
                       $instr[6:2] ==? 5'b01110;
         $is_s_instr = $instr[6:2] ==? 5'b0100x;
         $is_b_instr = $instr[6:2] ==? 5'b11000;
         $is_j_instr = $instr[6:2] ==? 5'b11011;
         $is_u_instr = $instr[6:2] ==? 5'b0x101;
         
         $imm[31:0] = $is_i_instr ? { {21{$instr[31]}}, $instr[30:20]} :
                      $is_s_instr ? { {21{$instr[31]}}, $instr[30:25], $instr[11:7]} :
                      $is_b_instr ? { {20{$instr[31]}}, $instr[7], $instr[30:25], $instr[11:8], 1'b0} :
                      $is_u_instr ? { $instr[31:12], 12'b0} :
                      $is_j_instr ? { {12{$instr[31]}}, $instr[19:12], $instr[20], $instr[30:21], 1'b0} : 32'b0;
         
         $rs2_valid = $is_r_instr || $is_s_instr || $is_b_instr;
         ?$rs2_valid
            $rs2[4:0] = $instr[24:20];
         
         $rs1_valid = $is_r_instr || $is_s_instr || $is_b_instr || $is_i_instr;
         ?$rs2_valid
            $rs1[4:0] = $instr[19:15];
         
         $funct3_valid = $is_r_instr || $is_s_instr || $is_b_instr || $is_i_instr;
         ?$rs2_valid
            $funct3[3:0] = $instr[14:12];
   
         $opcode[6:0] = $instr[6:0];
         
         $funct7_valid = $is_r_instr;
         ?$rs2_valid
            $funct7[6:0] = $instr[31:25];
            
         $dec_bits[10:0] = {$funct[5], $funct3, $opcode};
         $is_beq = $dec_bits ==? 11'bx_000_1100011;
         $is_bne = $dec_bits ==? 11'bx_001_1100011;
         $is_blt = $dec_bits ==? 11'bx_100_1100011;
         $is_bge = $dec_bits ==? 11'bx_101_1100011;
         $is_bltu = $dec_bits ==? 11'bx_110_1100011;
         $is_bgeu = $dec_bits ==? 11'bx_111_1100011;
         $is_addi = $dec_bits ==? 11'bx_000_0010011;
         $is_add = $dec_bits == 11'b0_000_0110011;
```

![image](https://github.com/user-attachments/assets/73a7ab06-9792-482f-80a1-f58065b6d58f)


## Register file read/write  and ALU:

The figure below shows the input and output registers.

![image](https://github.com/user-attachments/assets/0df24e9e-692f-4a69-8778-7f47f3a01d46)

Code snippet is given below:
( Insert this snippet under the TLV section in Makerchip IDE )
```
// Register File Read Logic
     ?$rs1_valid
        $rf_rd_en1 = $rs1_valid;
        $rf_rd_index1[4:0] = $rs1[4:0];
     
     ?$rs2_valid
        $rf_rd_en2 = $rs2_valid;
        $rf_rd_index2[4:0] = $rs2[4:0];
     
     $src1_value[31:0] = $rf_rd_data1[31:0];
     $src2_value[31:0] = $rf_rd_data2[31:0];
     
//ALU
     
     $result[31:0] = $is_addi ? $src1_value + $imm :
                     $is_add  ? $src1_value + $src2_value :
                     32'bx;
     
// Register File Write
     $rf_wr_en = ($rd == 5'b0) ? 1'b0 : $rd_valid;
     
     ?$rd_valid
        $rf_wr_index[4:0] = $rd[4:0];
     
     $rf_wr_data[31:0] = $result[31:0];
```
![image](https://github.com/user-attachments/assets/c4c03c0d-6647-4869-80bc-857610a1647b)

## Branch Instruction

Block Diagram :

![image](https://github.com/user-attachments/assets/e231c975-74bc-4e5b-b250-35e9b3e175ce)

Various Branch Instructions :

![image](https://github.com/user-attachments/assets/c17e7c03-65f0-47a1-9a16-a9d60d91ddfe)

CODE ;
```
 $taken_branch = $is_beq ? ($src1_value == $src2_value):
                         $is_bne ? ($src1_value != $src2_value):
                         $is_blt ? (($src1_value < $src2_value) ^ ($src1_value[31] != $src2_value[31])):
                         $is_bge ? (($src1_value >= $src2_value) ^ ($src1_value[31] != $src2_value[31])):
                         $is_bltu ? ($src1_value < $src2_value):
                         $is_bgeu ? ($src1_value >= $src2_value):
                                    1'b0;
```
![image](https://github.com/user-attachments/assets/029064f7-1841-4191-a415-24f21138ceaa)

VIZ :

![image](https://github.com/user-attachments/assets/2cd7840e-bb8f-4600-9832-5930fcfc1c36)

## TESTBENCH 
CODE :
```
//TESTBENCH
          *passed = |cpu/xreg[10]>>5$value == (1+2+3+4+5+6+7+8+9) ;
```

![image](https://github.com/user-attachments/assets/f382c2a4-1c42-422e-b5ba-7d1f68d7bcd6)

![image](https://github.com/user-attachments/assets/44f08397-ca97-4a9b-a713-9810c9eaaa96)

</details>

<details>
      <summary> Complete RISC-V CPU Micro-architechture. (Day 5) </summary>

# Pipelining the CPU

Now pipelining of the CPU core is done, which allows easy retiming and reduces functional bug to a great extent . Pipelining allows faster computaion. For pipelining as mentioned earlier we simply need to add @1, @2 and so on. The snapshot of the pipelining is as shown below. In TL verilog, another advantage is defining of pipeline in systematic order is not necessary

## 3 - Cycle Valid Signal
```
$valid = $reset ? 1'b0 : ($start) ? 1'b1 : (>>3$valid) ;
        $start_int = $reset ? 1'b0 : 1'b1;
        $start = $reset ? 1'b0 : ($start_int && !>>1$start_int);
```
## Generating valid signals for each instruction

```
  //Generate valid signals for each instruction fields
         $rs1_or_funct3_valid    = $is_r_instr || $is_i_instr || $is_s_instr || $is_b_instr;
         $rs2_valid              = $is_r_instr || $is_s_instr || $is_b_instr;
         $rd_valid               = $is_r_instr || $is_i_instr || $is_u_instr || $is_j_instr;
         $funct7_valid           = $is_r_instr;
```
# Completing the RISCV CPU

### Block Diagram

![image](https://github.com/user-attachments/assets/b0611173-d412-4529-a1cf-ca23e437c0f0)

### CODE :
```
\m4_TLV_version 1d: tl-x.org
\SV
   m4_include_lib(['https://raw.githubusercontent.com/shivanishah269/risc-v-core/master/FPGA_Implementation/riscv_shell_lib.tlv'])
   
   // Module interface, either for Makerchip, or not.
   m4_ifelse_block(M4_MAKERCHIP, 1, ['
   // Makerchip module interface.
   m4_makerchip_module
   wire CLK = clk;
   logic [9:0] OUT;
   assign passed = cyc_cnt > 300;
   '], ['
   // Custom module interface for BabySoC.
   module rvmyth(
      output reg [9:0] OUT,
      input CLK,
      input reset
   );
   wire clk = CLK;
   '])
   
\TLV
   // External to function:
   m4_asm(ADD, r10, r0, r0)             // Initialize r10 (a0) to 0.
   // Function:
   m4_asm(ADD, r14, r10, r0)            // Initialize sum register a4 with 0x0
   m4_asm(ADDI, r12, r10, 1010)         // Store count of 10 in register a2.
   m4_asm(ADD, r13, r10, r0)            // Initialize intermediate sum register a3 with 0
   // Loop:
   m4_asm(ADD, r14, r13, r14)           // Incremental addition
   m4_asm(ADDI, r13, r13, 1)            // Increment intermediate register by 1
   m4_asm(BLT, r13, r12, 1111111111000) // If a3 is less than a2, branch to label named <loop>
   m4_asm(ADD, r10, r14, r0)            // Store final result to register a0 so that it can be read by main program
   m4_asm(SW, r0, r10, 10000)           // Store the final result value to byte address 16
   m4_asm(LW, r17, r0, 10000)           // Load the final result value from adress 16 to x17
   //
   m4_define_hier(['M4_IMEM'], M4_NUM_INSTRS)
   //
   |cpu
      @0
         $reset = *reset;
         $clk_CHA = *clk;
         `BOGUS_USE($clk_CHA)
      //Fetch
         // Next PC
         $pc[31:0] = (>>1$reset) ? 32'd0 : 
                     (>>3$valid_taken_br) ? >>3$br_tgt_pc : 
                     (>>3$valid_load) ? >>3$inc_pc : 
                     (>>3$valid_jump && >>3$is_jal) ? >>3$br_tgt_pc :
                     (>>3$valid_jump && >>3$is_jalr) ? >>3$jalr_tgt_pc : >>1$inc_pc;
         
         $imem_rd_en = !$reset;
         $imem_rd_addr[31:0] = $pc[M4_IMEM_INDEX_CNT+1:2];
         
      @1         
         $instr[31:0] = $imem_rd_data[31:0];
         $inc_pc[31:0] = $pc + 32'd4;          
      // Decode   
         $is_i_instr = $instr[6:2] == 5'b00000 ||
                       $instr[6:2] == 5'b00001 ||
                       $instr[6:2] == 5'b00100 ||
                       $instr[6:2] == 5'b00110 ||
                       $instr[6:2] == 5'b11001;
         $is_r_instr = $instr[6:2] == 5'b01011 ||
                       $instr[6:2] == 5'b10100 ||
                       $instr[6:2] == 5'b01100 ||
                       $instr[6:2] == 5'b01101;                       
         $is_b_instr = $instr[6:2] == 5'b11000;
         $is_u_instr = $instr[6:2] == 5'b00101 ||
                       $instr[6:2] == 5'b01101;
         $is_s_instr = $instr[6:2] == 5'b01000 ||
                       $instr[6:2] == 5'b01001;
         $is_j_instr = $instr[6:2] == 5'b11011;
         
         $imm[31:0] = $is_i_instr ? { {21{$instr[31]}} , $instr[30:20] } :
                      $is_s_instr ? { {21{$instr[31]}} , $instr[30:25] , $instr[11:8] , $instr[7] } :
                      $is_b_instr ? { {20{$instr[31]}} , $instr[7] , $instr[30:25] , $instr[11:8] , 1'b0} :
                      $is_u_instr ? { $instr[31:12] , 12'b0} : 
                      $is_j_instr ? { {12{$instr[31]}} , $instr[19:12] , $instr[20] , $instr[30:21] , 1'b0} : 32'b0;
         
         $rs2_valid = $is_r_instr || $is_s_instr || $is_b_instr;
         $rs1_valid = $is_r_instr || $is_s_instr || $is_b_instr || $is_i_instr;
         $rd_valid = $is_r_instr || $is_i_instr || $is_u_instr || $is_j_instr;
         $funct3_valid = $is_r_instr || $is_s_instr || $is_b_instr || $is_i_instr;
         $funct7_valid = $is_r_instr;
         
         ?$rs2_valid
            $rs2[4:0] = $instr[24:20];
         ?$rs1_valid
            $rs1[4:0] = $instr[19:15];
         ?$rd_valid
            $rd[4:0] = $instr[11:7];
         ?$funct3_valid
            $funct3[2:0] = $instr[14:12];
         ?$funct7_valid
            $funct7[6:0] = $instr[31:25];
            
         $opcode[6:0] = $instr[6:0];
         
         $dec_bits[10:0] = {$funct7[5],$funct3,$opcode};
         
         // Branch Instruction
         $is_beq = $dec_bits[9:0] == 10'b000_1100011;
         $is_bne = $dec_bits[9:0] == 10'b001_1100011;
         $is_blt = $dec_bits[9:0] == 10'b100_1100011;
         $is_bge = $dec_bits[9:0] == 10'b101_1100011;
         $is_bltu = $dec_bits[9:0] == 10'b110_1100011;
         $is_bgeu = $dec_bits[9:0] == 10'b111_1100011;
         
         // Arithmetic Instruction
         $is_add = $dec_bits == 11'b0_000_0110011;
         $is_addi = $dec_bits[9:0] == 10'b000_0010011;
         $is_or = $dec_bits == 11'b0_110_0110011;
         $is_ori = $dec_bits[9:0] == 10'b110_0010011;
         $is_xor = $dec_bits == 11'b0_100_0110011;
         $is_xori = $dec_bits[9:0] == 10'b100_0010011;
         $is_and = $dec_bits == 11'b0_111_0110011;
         $is_andi = $dec_bits[9:0] == 10'b111_0010011;
         $is_sub = $dec_bits == 11'b1_000_0110011;
         $is_slti = $dec_bits[9:0] == 10'b010_0010011;
         $is_sltiu = $dec_bits[9:0] == 10'b011_0010011;
         $is_slli = $dec_bits == 11'b0_001_0010011;
         $is_srli = $dec_bits == 11'b0_101_0010011;
         $is_srai = $dec_bits == 11'b1_101_0010011;
         $is_sll = $dec_bits == 11'b0_001_0110011;
         $is_slt = $dec_bits == 11'b0_010_0110011;
         $is_sltu = $dec_bits == 11'b0_011_0110011;
         $is_srl = $dec_bits == 11'b0_101_0110011;
         $is_sra = $dec_bits == 11'b1_101_0110011;
         
         // Load Instruction
         $is_load = $dec_bits[6:0] == 7'b0000011;
         
         // Store Instruction
         $is_sb = $dec_bits[9:0] == 10'b000_0100011;
         $is_sh = $dec_bits[9:0] == 10'b001_0100011;
         $is_sw = $dec_bits[9:0] == 10'b010_0100011;
         
         // Jump Instruction
         $is_lui = $dec_bits[6:0] == 7'b0110111;
         $is_auipc = $dec_bits[6:0] == 7'b0010111;
         $is_jal = $dec_bits[6:0] == 7'b1101111;
         $is_jalr = $dec_bits[9:0] == 10'b000_1100111;
         
         $is_jump = $is_jal || $is_jalr;
         
      @2   
      // Register File Read
         $rf_rd_en1 = $rs1_valid;
         ?$rf_rd_en1
            $rf_rd_index1[4:0] = $rs1[4:0];
         
         $rf_rd_en2 = $rs2_valid;
         ?$rf_rd_en2
            $rf_rd_index2[4:0] = $rs2[4:0];
            
      // Branch Target PC       
         $br_tgt_pc[31:0] = $pc + $imm;
      
      // Jump Target PC
         $jalr_tgt_pc[31:0] = $src1_value + $imm;
         
      // Input signals to ALU
         $src1_value[31:0] = ((>>1$rd == $rs1) && >>1$rf_wr_en) ? >>1$result : $rf_rd_data1[31:0];
         $src2_value[31:0] = ((>>1$rd == $rs2) && >>1$rf_wr_en) ? >>1$result : $rf_rd_data2[31:0];
         
      @3   
         
      // ALU
         $sltu_result = $src1_value < $src2_value ;
         $sltiu_result = $src1_value < $imm ;
         
         $result[31:0] = $is_addi ? $src1_value + $imm :
                         $is_add ? $src1_value + $src2_value : 
                         $is_or ? $src1_value | $src2_value : 
                         $is_ori ? $src1_value | $imm :
                         $is_xor ? $src1_value ^ $src2_value :
                         $is_xori ? $src1_value ^ $imm :
                         $is_and ? $src1_value & $src2_value :
                         $is_andi ? $src1_value & $imm :
                         $is_sub ? $src1_value - $src2_value :
                         $is_slti ? (($src1_value[31] == $imm[31]) ? $sltiu_result : {31'b0,$src1_value[31]}) :
                         $is_sltiu ? $sltiu_result :
                         $is_slli ? $src1_value << $imm[5:0] :
                         $is_srli ? $src1_value >> $imm[5:0] :
                         $is_srai ? ({{32{$src1_value[31]}}, $src1_value} >> $imm[4:0]) :
                         $is_sll ? $src1_value << $src2_value[4:0] :
                         $is_slt ? (($src1_value[31] == $src2_value[31]) ? $sltu_result : {31'b0,$src1_value[31]}) :
                         $is_sltu ? $sltu_result :
                         $is_srl ? $src1_value >> $src2_value[5:0] :
                         $is_sra ? ({{32{$src1_value[31]}}, $src1_value} >> $src2_value[4:0]) :
                         $is_lui ? ({$imm[31:12], 12'b0}) :
                         $is_auipc ? $pc + $imm :
                         $is_jal ? $pc + 4 :
                         $is_jalr ? $pc + 4 : 
                         ($is_load || $is_s_instr) ? $src1_value + $imm : 32'bx;
                         
      // Register File Write
         $rf_wr_en = ($rd_valid && $valid && $rd != 5'b0) || >>2$valid_load;
         ?$rf_wr_en
            $rf_wr_index[4:0] = !$valid ? >>2$rd[4:0] : $rd[4:0];
      
         $rf_wr_data[31:0] = !$valid ? >>2$ld_data[31:0] : $result[31:0];
      
      // Branch
         $taken_br = $is_beq ? ($src1_value == $src2_value) :
                     $is_bne ? ($src1_value != $src2_value) :
                     $is_blt ? (($src1_value < $src2_value) ^ ($src1_value[31] != $src2_value[31])) :
                     $is_bge ? (($src1_value >= $src2_value) ^ ($src1_value[31] != $src2_value[31])) :
                     $is_bltu ? ($src1_value < $src2_value) :
                     $is_bgeu ? ($src1_value >= $src2_value) : 1'b0;
                     
         $valid_taken_br = $valid && $taken_br;
         
      // Load
         $valid_load = $valid && $is_load;
         $valid = !(>>1$valid_taken_br || >>2$valid_taken_br || >>1$valid_load || >>2$valid_load || >>1$valid_jump || >>2$valid_jump);
      
      // Jump
         $valid_jump = $valid && $is_jump;
                  
      @4
         $dmem_rd_en = $valid_load;
         $dmem_wr_en = $valid && $is_s_instr;
         $dmem_addr[3:0] = $result[5:2];
         $dmem_wr_data[31:0] = $src2_value[31:0];
         
      @5   
         $ld_data[31:0] = $dmem_rd_data[31:0];
         
      // Note: Because of the magic we are using for visualisation, if visualisation is enabled below,
      //       be sure to avoid having unassigned signals (which you might be using for random inputs)
      //       other than those specifically expected in the labs. You'll get strange errors for these.

         `BOGUS_USE($is_beq $is_bne $is_blt $is_bge $is_bltu $is_bgeu)
         `BOGUS_USE($is_sb $is_sh $is_sw)
   // Assert these to end simulation (before Makerchip cycle limit).
   \SV_plus
      always @ (posedge CLK) begin
         *OUT = |cpu/xreg[14]>>5$value;                
      end
   
   // Macro instantiations for:
   //  o instruction memory
   //  o register file
   //  o data memory
   //  o CPU visualization
   |cpu
      m4+imem(@1)    // Args: (read stage)
      m4+rf(@2, @3)  // Args: (read stage, write stage) - if equal, no register bypass is required
      m4+dmem(@4)    // Args: (read/write stage)

     
\SV
   
   endmodule

```

### SIMULATION STATUS :

![image](https://github.com/user-attachments/assets/29a5f6c0-bb4f-4fe1-840c-6e0ccff66845)

### BLOCK DIAGRAM :

![image](https://github.com/user-attachments/assets/b6cedc2f-d49d-4015-825d-a5d8b3eeffd6)

### VIZ. :

![image](https://github.com/user-attachments/assets/9e3e528d-17ac-4e30-907a-f81d1f9070e4)

### The waveform including the "named clock : $clk_CHA " is shown below :

![image](https://github.com/user-attachments/assets/71c03f40-86af-4d03-9f90-963765e0c02f)

### The waveform for the /xreg[14] where the sum of this program is store:

![image](https://github.com/user-attachments/assets/e747b683-406d-4138-88db-5e7b77e84587)


</details>      

# TASK 8 
( 22/08/2024 )

<details>
      <summary> RISC-V Pre synthesis simulation using IVerilog and GTKWave </summary>

## AIM : Comparision of RISC-V Pre-Synthesis Simulation outputs using Iverilog GTKwave and Makerchip

The RISC-V processor was designed using TL-Verilog in the Makerchip IDE. To implement it on an FPGA, it needs to be converted to Verilog, which was done using the Sandpiper-SaaS compiler. Pre-synthesis simulations were then performed using the GTKWave simulator.

**Step-by-Step process of simulation:**

**Step 1:** Install the Required Packages:
```
sudo apt install make python python3 python3-pip git iverilog gtkwave docker.io
sudo chmod 666 /var/run/docker.sock
cd ~
pip3 install pyyaml click sandpiper-saas
```
**Step 2:** Now clone the given repository in the home directory :
```
cd ~
git clone https://github.com/manili/VSDBabySoC.git
```

![image](https://github.com/user-attachments/assets/f488129e-6ba1-4c0c-a898-70f5037fb5a5)

**Step 3:** Replace the .tlv file in the VSDBabySoC/src/module folder with our RISC-V .tlv file which we want to convert into verilog.

**Step 4:** Change the working directory to VSDBabySoC.
```
cd VSDBabySoC
```
**Step 5:** Translate .tlv definition of RISC-V into .v definition by giving the following command:
```
sandpiper-saas -i ./src/module/*.tlv -o rvmyth.v --bestsv --noline -p verilog --outdir ./src/module/
```

![image](https://github.com/user-attachments/assets/125c2656-bdaa-4d84-9905-8557cc4f110c)

**Step 6:** Create the pre_synth_sim.vcd file by running the following command:
```
make pre_synth_sim
```
![image](https://github.com/user-attachments/assets/c8d30bdb-16a3-4823-a71d-69eb37406d82)

**Step 7:** Compile and simulate RISC-V design by running the following command:
```
$ iverilog -o output/pre_synth_sim.out -DPRE_SYNTH_SIM src/module/testbench.v -I src/include -I src/module -
```
**Step 8:** The result of the simulation (i.e. pre_synth_sim.vcd) will be stored in the output/pre_synth_sim directory. Therefore change the working directory to output.
```
cd output
./pre_synth_sim.out
```
![image](https://github.com/user-attachments/assets/fa240a85-a340-405a-bc0e-ea2cf590f4ee)


**Step 9:** Open the .vcd simulation file through GTKWave simulation tool by running the following command:
```
gtkwave pre_synth_sim.vcd
```
![image](https://github.com/user-attachments/assets/9e9a0d50-01d5-4f84-88b1-5bbd6a3fa6c2)


**GTKWave Output Waveform**

![image](https://github.com/user-attachments/assets/3e48f3cf-c6a4-485d-8bd5-7039052e7df8)

**Comparison of the Output Waveforms**

![image](https://github.com/user-attachments/assets/5d933f75-b673-42c8-966b-0f7d7297bdb1)


</details>


# TASK 9 
( 29/08/2024 )

<details>
      <summary> RISC-V Pre synthesis Analog simulation using IVerilog and GTKWave. </summary>

## AIM : Analyzing RISC-V Pre-Synthesis Analog Simulation outputs using Iverilog GTKwave.

## SUB-TASK 1 : TOOLS INSTALLATION:

Commands to install Yosys in UBUNTU(Linux) :

```
   $ git clone https://github.com/YosysHQ/yosys.git
    $ cd yosys
    $ sudo apt install make (If make is not installed) 
    $ sudo apt-get install build-essential clang bison flex \
        libreadline-dev gawk tcl-dev libffi-dev git \
        graphviz xdot pkg-config python3 libboost-system-dev \
        libboost-python-dev libboost-filesystem-dev zlib1g-dev
    $ make config-gcc
    $ make 
    $ sudo make install
```

To verify the installation of yosys, type yosys in terminal window :

![Screenshot from 2024-09-02 15-16-25](https://github.com/user-attachments/assets/40c4ce97-7041-4878-9a2d-8d851f52ef40)

Commands to install IVerilog in UBUNTU(Linux) :

  ```
  sudo apt-get install iverilog
  ```
Below screenshot verifies the installation of iverilog in the system :

![Screenshot from 2024-09-02 15-24-43](https://github.com/user-attachments/assets/2f6e8f40-8bb3-4843-a0bc-29f4d39608b1)

Commands to install GTKWave in UBUNTU(Linux) :

```
    sudo apt update
    sudo apt install gtkwave
```

Below screenshot verifies the installation of gtkwave in the system :

![Screenshot from 2024-09-02 15-27-23](https://github.com/user-attachments/assets/9fad1a75-8d3d-4a3e-98c2-88148ad7af18)

Commands to install OpenSTA in UBUNTU(Linux) :

```
git clone https://github.com/The-OpenROAD-Project/OpenSTA.git
cd OpenSTA
mkdir build
cd build
cmake ..
make
sudo make install
```

Below screenshot verifies the installation of OpenSTA in the system :

![Screenshot from 2024-09-02 15-30-29](https://github.com/user-attachments/assets/0fbd69f2-69c0-4680-807f-1f3ea867aebc)


## SUB-TASK 2 : BabySoC Simulation  

VSDBabySoC is a small yet powerful RISCV-based SoC. The main purpose of designing such a small SoC is to test three open-source IP cores together for the first time and calibrate the analog part of it. VSDBabySoC contains one RVMYTH microprocessor, an 8x-PLL to generate a stable clock, and a 10-bit DAC to communicate with other analog devices.


___Phase-Locked-Loop (PLL)___

A Phase-Locked Loop (PLL) is an electronic circuit that synchronizes an output signal's phase and frequency with a reference signal. It typically consists of three main components:

- Phase Detector: Compares the phase of the reference signal with the output signal and generates an error signal based on the difference.

- Loop Filter: Processes the error signal to smooth it out, reducing noise and improving stability.

- Voltage-Controlled Oscillator (VCO): Adjusts its output frequency based on the filtered error signal to minimize the phase difference.

The PLL is widely used in applications such as clock generation, frequency synthesis, and data recovery in communication systems.

___Digital-to-Analog Converter (DAC)___

A Digital-to-Analog Converter (DAC) is an electronic device that converts digital signals (typically binary) into analog signals (such as voltage or current).

This conversion is crucial in systems where digital data needs to be interpreted by analog devices or for output to be perceived by humans, like in audio and video equipment.

DACs are commonly used in applications like audio playback, video display, and signal processing.


Commands to Run the `rvmyth.v` File
```
cd VSDBabySoC
```
```
iverilog -o ./pre_synth_sim.out -DPRE_SYNTH_SIM src/module/testbench.v -I src/include -I src/module/
```

```
./pre_synth_sim.out
```
```
gtkwave pre_synth_sim.vcd
```
In the below screenshot, the output of the sum 1 to 9 can be observed after simulation.

![Screenshot from 2024-09-02 15-53-06](https://github.com/user-attachments/assets/fb1fd210-daf3-4cb0-8543-43ddd375dc97)

- **CLK** is the output clk signal from the PLL module.
- **clk_CHA** is the clock used by the RISC-V CPU for the operations.
- **reset** is the reset signal for the RISC-V CPU.
- **REF** is the input clk reference signal to the PLL module.  
- **OUT** is the DAC output signal.


Th **ZOOMED OUT** image of the waveform is shown below: 

![Screenshot from 2024-09-04 14-36-43](https://github.com/user-attachments/assets/5f67ea71-9beb-4d35-981b-706148b7a861)



</details>



# TASK 10
( 15/10/2024 )

<details>
      <summary> LAB 1 (Day 1) : Downloading of the files from the GitHub Repository  </summary>
      
## LAB 1 - AIM : Downloading of the files from the GitHub Repository 

Steps to follow: 
```
sudo -i
sudo apt-get install git
cd /home/chandra-shekhar-jha/VLSI     # go to your home directory
git clone https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git
cd sky130RTLDesignAndSynthesisWorkshop
cd verilog_files
ls
```
Below is the Snapshot of the above commands :

![lab1](https://github.com/user-attachments/assets/59a9ec3d-3990-4ae9-922b-614f6a1e7446)


</details>



<details>
      <summary> LAB 2 (Day 1) : Simulation of '2:1 MULTIPLEXER' using IVerilog and GTKWave. </summary>
      
## LAB 2 - AIM : Simulation of a ' 2:1 MULTIPLEXER ' using IVerilog and GTKWave. 

### Block Diagram of Simulation Flow in IVerilog :

![lab2 2](https://github.com/user-attachments/assets/16693310-2d05-41c2-86f5-b43c80589113)
Simulator continuously checks for changes in the input. If there is any change in input, the output is evaluated else the simulator will never evaluate the output.


The .v files of 2:1 multiplexer and its testbench is already present in the 'verilog_file' folder.

![lab2 1](https://github.com/user-attachments/assets/bf029fe5-a7a8-430d-9f60-e1a361b20513)

We just need to put few commands as stated below in order to see the waveforms.

```
iverilog good_mux.v tb_good_mux.v
ls
```
After giving the above command the IVerilog stores the output as ' a.out '

Now let's execute the ' a.out ' file and observe the waveforms.

```
./a.out
gtkwave tb_good_mux.vcd
```
Below is the Snapshot of the above commands:

![lab2](https://github.com/user-attachments/assets/a7245c37-0a50-42f2-897d-e88155183693)

</details>


<details>
      <summary> LAB 3 (Day 1) : Synthesis of 2:1 Multiplexer using Yosys and Logic Synthesis.  </summary>
      
## LAB 3 - AIM : Synthesis of 2:1 Multiplexer using Yosys and Logic Synthesis.

### Yosys

Synthesizer is a tool for converting the RTL to Netlist and here we are using the Yosys as the Synthesizer.

A synthesizer plays a key role in digital design by transforming RTL (Register Transfer Level) code into a gate-level netlist. This netlist provides a detailed description of the circuit, outlining the logical gates and their interconnections, and serves as the foundation for later stages like place and route. In this design flow, the synthesizer being used is Yosys, an open-source tool for Verilog HDL synthesis. Yosys applies several optimization techniques to generate an efficient gate-level implementation from the RTL code.

### Block Diagram of Yosys setup :

![3 1](https://github.com/user-attachments/assets/4bb86a05-c226-486f-9b89-01610cb188a2)

### Block Diagram of Systhesis Verification :

![3 2](https://github.com/user-attachments/assets/918ab5b7-25c6-4c82-8e82-54a27c8846c7)

Note: The set of primary inputs and primary outputs remains unchanged between the RTL design and the synthesized netlist. Therefore, the same test bench can be used for both.

### Logic Systhesis

RTL Design: The design is described using a behavioral representation in Hardware Description Language (HDL) based on the required specifications.

Synthesis: The RTL (Register Transfer Level) code is translated into a gate-level representation. This process converts the design into gates and interconnections, resulting in a file known as the netlist.

![3 3](https://github.com/user-attachments/assets/d491f91a-9f97-4a17-bf44-b26df28b6d5a)

#### Command steps for Yosys

This will invoke/start the yosys
```
yosys       
```
Load the sky130 standard library.
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib      
```
Read the design files
```
read_verilog good_mux.v        
```
![3 4](https://github.com/user-attachments/assets/6067a3d7-1513-4ec8-9801-e2e492ac18ee)

Synthesize the top level module
```
synth -top good_mux     
```
![3 5](https://github.com/user-attachments/assets/b743ec0d-f297-4f16-8444-eaa142c69829)

Map to the standard library
```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
![3 6](https://github.com/user-attachments/assets/22f988c7-2749-4497-a0e8-50e433edd7ba)
![3 7](https://github.com/user-attachments/assets/806e0200-b1e4-43d5-bb87-2d50e8cbe1d1)

In order to see graphical version of the logic it has realized just type :
```
show
```
![3 8](https://github.com/user-attachments/assets/4fa8d8bb-9c7e-4fc7-a728-008355e14b57)

Now, To write the result netlist to a file use the write_veriog command. 
This will output the netlist to a file in the current directory.
```
write_verilog -noattr good_mux_netlist.v
!gvim good_mux_netlist.v

```
![3 9](https://github.com/user-attachments/assets/5e4f7796-5f55-4e1d-89de-95968321fd6c)


</details>


<details>
      <summary> LAB 4 (Day 2) : Introduction to timing.lib </summary>
      
## LAB 4 - AIM : Introduction and Walkthrough to ' dot lib '.

'.lib' is like a collection of standard cells. It contains slow cells, fast cells and many more things.
In order to view the '.lib' files, Enter the following command : 

```
sudo -i
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib
gvim sky130_fd_sc_hd__tt_025C_1v80.lib

```
Press ` Shift + : syn off `

![4 1](https://github.com/user-attachments/assets/aabbb278-8824-4b42-953a-62486871930d)
It gives information about the type of process (like here it is 130nm tech) and the process condition like temperature, voltage, etc
It also define various constraints like the units of the variables, type of technology:

   - technology("cmos").
   - delay_model : "table_lookup".
   - bus_naming_style : "%s[%d]".
   - time_unit : "1ns".
   - voltage_unit : "1V".
   - leakage_power_unit : "1nW".
   - current_unit : "1mA".
   - pulling_resistance_unit : "1kohm".
   - capacitive_load_unit(1.0000000000, "pf").

It also tells about the features of different cells like leakage power, power consumption, area, input capacitance and delay for different input combination

#### Lets observe the simple 2 input AND gate

![4 2](https://github.com/user-attachments/assets/b42b133f-32f2-43cb-846a-7ffa331a71ae)


</details>


<details>
      <summary> LAB 5 (Day 2) : Hierarchial synthesis vs Flat synthesis and Various D - FlipFlop. </summary>
      
## LAB 5 - AIM : Hierarchial synthesis vs Flat synthesis and Various D - FlipFlop.

### Hierarchial synthesis

#### Command steps :

Go to the required directory
```
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog multiple_modules.v
```
![4 3](https://github.com/user-attachments/assets/16e8dd47-178d-4db1-ac93-6c6641938a9e)

Synthesize the Design
```
synth -top multiple_modules
```
"When running ` synth -top multiple_modules ` in Yosys, a hierarchical synthesis is performed, meaning that the hierarchy between modules is preserved.

![4 4](https://github.com/user-attachments/assets/ad1fac31-9889-43b3-a1ba-8c372ed5cbfa)  

Multiple Modules: - 2 SubModules 

Now Generate the Netlist
```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Now let's Create a Graphical Representation of Logic for Multiple Modules
```
show multiple_modules
```
![4 5](https://github.com/user-attachments/assets/ab5cf897-ec7e-497c-aaa0-f06772111130)

Writing the netlist and then viewing
```
write_verilog -noattr multiple_modules_hier.v
!vim multiple_modules_hier.v
```
NETList file 

![4 6](https://github.com/user-attachments/assets/b41012a2-9c98-4b94-9c47-526fbcc190e7)



- Use of Flattening: Merges all hierarchical modules in the design into a single module to create a flat netlist.
for this just type
```
flatten
```
Writing the netlist and then viewing
```
write_verilog -noattr multiple_modules_hier.v
!vim multiple_modules_hier.v
```

![4 7](https://github.com/user-attachments/assets/478b4ce3-7549-4a03-b8aa-37d137cccc06)


NETList file 

![4 8](https://github.com/user-attachments/assets/918e97da-fd70-413b-b566-215af29496af)

Now let's Create a Graphical Representation of Logic for Multiple Modules
```
show 
```
![4 9](https://github.com/user-attachments/assets/0b9abcec-881c-4229-9b3a-8ec445a1b7dc)




      
## Various D Flops coding styles, Simulation using Iverilog and GTKWave followed by Synthesis using Yosys.


### Simulation of D-Flipflop using Iverilog and GTKWave. Performed simulations for 3 types of D-Flipflops 

- Asynchronous Reset
- Asynchronous Set
- Synchronous Reset.

#### 1. Asynchronous Reset

The velilog code for the asynchronous reset is given below :
```
module dff_asyncres(input clk, input async_reset, input d, output reg q);
	always@(posedge clk, posedge async_reset)
	begin
		if(async_reset)
			q <= 1'b0;
		else
			q <= d;
	end
endmodule
```

Testbench code is as follows:
```
module tb_dff_asyncres; 
	reg clk, async_reset, d;
	wire q;
	dff_asyncres uut (.clk(clk),.async_reset (async_reset),.d(d),.q(q));

	initial begin
		$dumpfile("tb_dff_asyncres.vcd");
		$dumpvars(0,tb_dff_asyncres);
		// Initialize Inputs
		clk = 0;
		async_reset = 1;
		d = 0;
		#3000 $finish;
	end
		
	always #10 clk = ~clk;
	always #23 d = ~d;
	always #547 async_reset=~async_reset; 
endmodule
```

##### Command steps :

Go to the required directory
```
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```
We just need to put few commands as stated below in order to see the waveforms.

```
iverilog dff_asyncres.v tb_dff_asyncres.v
ls
```
After giving the above command the IVerilog stores the output as ' a.out '

Now let's execute the ' a.out ' file and observe the waveforms.

```
./a.out
gtkwave tb_dff_asyncres.vcd
```
Below is the Snapshot of the above commands and the resultant Waveforms:

![6 1](https://github.com/user-attachments/assets/0c582f91-baac-4c18-94fc-17c79a9eb3f5)

OBSERVATION : From the waveform, it can be observed that the Q output changes to zero when the asynchronous reset is set high, independent of the positive/negative clock edge.


#### 2. Asynchronous Set

The velilog code for the Asynchronous set is given below :
```
module dff_async_set(input clk, input async_set, input d, output reg q);
	always@(posedge clk, posedge async_set)
	begin
		if(async_set)
			q <= 1'b1;
		else
			q <= d;
	end
endmodule
```

Testbench code is as follows:
```
module tb_dff_async_set; 
	reg clk, async_set, d;
	wire q;
	dff_async_set uut (.clk(clk),.async_set (async_set),.d(d),.q(q));

	initial begin
		$dumpfile("tb_dff_async_set.vcd");
		$dumpvars(0,tb_dff_async_set);
		// Initialize Inputs
		clk = 0;
		async_set = 1;
		d = 0;
		#3000 $finish;
	end
		
	always #10 clk = ~clk;
	always #23 d = ~d;
	always #547 async_set=~async_set; 
endmodule
```

##### Command steps :

Go to the required directory
```
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```
We just need to put few commands as stated below in order to see the waveforms.

```
iverilog dff_async_set.v tb_dff_async_set.v
ls
```
After giving the above command the IVerilog stores the output as ' a.out '

Now let's execute the ' a.out ' file and observe the waveforms.

```
./a.out
gtkwave tb_dff_async_set.vcd
```
Below is the Snapshot of the above commands and the resultant Waveforms:

![6 2](https://github.com/user-attachments/assets/d270402e-4c53-4baa-852f-c512a487e767)

OBSERVATION : From the waveform, it can be observed that the Q output changes to one when the asynchronous set is set high, independent of the positive/negative clock edge.


#### 3. Synchronous Reset

The velilog code for the Synchronous reset is given below :
```
module dff_syncres(input clk, input sync_reset, input d, output reg q);
	always@(posedge clk)
	begin
		if(sync_reset)
			q <= 1'b0;
		else
			q <= d;
	end
endmodule
```

Testbench code is as follows:
```
module tb_dff_syncres; 
	reg clk, syncres, d;
	wire q;
	dff_asyncres uut (.clk(clk),.sync_reset (sync_reset),.d(d),.q(q));

	initial begin
		$dumpfile("tb_dff_syncres.vcd");
		$dumpvars(0,tb_dff_syncres);
		// Initialize Inputs
		clk = 0;
		sync_reset = 1;
		d = 0;
		#3000 $finish;
	end
		
	always #10 clk = ~clk;
	always #23 d = ~d;
	always #547 sync_reset=~async_reset; 
endmodule
```

##### Command steps :

Go to the required directory
```
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```
We just need to put few commands as stated below in order to see the waveforms.

```
iverilog dff_syncres.v tb_dff_syncres.v
ls
```
After giving the above command the IVerilog stores the output as ' a.out '

Now let's execute the ' a.out ' file and observe the waveforms.

```
./a.out
gtkwave tb_dff_syncres.vcd
```
Below is the Snapshot of the above commands and the resultant Waveforms:

![6 3](https://github.com/user-attachments/assets/3f2e8a4e-39a6-42eb-a914-47cc32773699)

OBSERVATION : From the waveform, it can be observed that the Q output changes to zero when the synchronous reset is set high, only at the positive clock edge.



### Synthesis of Various D-Flipflop using Yosys. Performed simulations for 3 types of D-Flipflops 

- Asynchronous Reset
- Asynchronous Set
- Synchronous Reset.

#### 1. Asynchronous Reset

#### Command steps :

Go to the required directory
```
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog dff_asyncres.v
```
Synthesize the Design
```
synth -top dff_asyncres
```
Now Generate the Netlist
```
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Now let's Create a Graphical Representation of Asynchronous Reset - D FlipFlop

```
show
```

![6 4](https://github.com/user-attachments/assets/64e4eb6d-50c0-4d05-b864-2ca3d030eab5)


#### 2. Asynchronous Set

#### Command steps :

Go to the required directory
```
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog dff_async_set.v
```
Synthesize the Design
```
synth -top dff_async_set
```
Now Generate the Netlist
```
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Now let's Create a Graphical Representation of Asynchronous Set - D FlipFlop

```
show
```
![6 5](https://github.com/user-attachments/assets/b6003c30-bd42-4db5-9c27-cfcbf1cc68c1)


#### 3. Synchronous Reset

#### Command steps :

Go to the required directory
```
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog dff_syncres.v
```
Synthesize the Design
```
synth -top dff_syncres
```
Now Generate the Netlist
```
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Now let's Create a Graphical Representation of Synchronous Reset - D FlipFlop

```
show
```
![6 6](https://github.com/user-attachments/assets/6e8fac8e-98c9-4ee8-97a1-57ee3fc667ca)





## Multiplication by 2: 

This tutorial, we get to know that specific multiplier hardware is not required for multiplication of a number by 2. It can simply be achieved by concatenating the number itself with a zero in the LSB. 
VERILOG CODE :
```
//Design
module mul2(input [2:0]a, output [3:0]y);
	assign y=a*2;
endmodule
```
Command Steps:
```
1. yosys
2. read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
3. read_verilog mult_2.v
4. synth -top mul2
5. abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
6. show
7. write_verilog -noattr mul2_net.v
8. gvim mul2_net.v
```
![Screenshot from 2024-10-22 11-04-41](https://github.com/user-attachments/assets/8c919235-3c14-48f0-ac96-a3d85d564560)

![Screenshot from 2024-10-22 11-06-16](https://github.com/user-attachments/assets/44748cf4-4fa3-44b8-a7ea-6669336fa18b)

![Screenshot from 2024-10-22 11-07-18](https://github.com/user-attachments/assets/958caee6-736d-4a6d-b7db-25252595e407)


## Multiplication by 9:
This tutorial, we get to know that specific multiplier hardware is not required for multiplication of a number by 9. It can simply be achieved by concatenating the number with itself.

```
//Design
module mul8(input [2:0]a, output [5:0]y);
	assign y=a*9;
endmodule
```
Command Steps:
```
1. yosys
2. read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
3. read_verilog mult_8.v
4. synth -top mul8
5. abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
6. show
7. write_verilog -noattr mul8_net.v
8. !vim mul8_net.v
```
![Screenshot from 2024-10-22 11-13-50](https://github.com/user-attachments/assets/b4a9698d-c792-4dde-a059-234c210254b9)

</details>


<details>
      <summary> LAB 6 (Day 3) : Optimization of various Combinational Designs </summary>
      
## LAB 6 - AIM : Optimization of various Combinational Designs 

### Optimization of various Combinational Designs 

- 2 input AND gate.
- 2 input OR gate.
- 3 input AND gate.
- 2 input XNOR Gate (3 input Boolean Logic)
- Multiple Module Optimization-1 
- Multiple Module Optimization-2

  
### 1. 2 input AND gate.

  The velilog code is given below :

```
module opt_check(input a, input b, output y);
	assign y = a?b:0;
endmodule
```
#### Command steps :

Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog opt_check.v
```
Synthesize the Design
```
synth -top opt_check
```

![6 7](https://github.com/user-attachments/assets/a06c1ae8-7b6c-49e1-a5d4-2018bd16d609)


Now Generate the Netlist
```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Removes unused or redundant logic in the design and purges any dangling wires or gates.
```
opt_clean -purge
```
Now let's Create a Graphical Representation 

```
show
```
![6 8](https://github.com/user-attachments/assets/1757827b-c54e-4f7b-a342-bf55ee4fe423)


### 2.  2 input OR gate.

  The velilog code is given below :

```
module opt_check2(input a, input b, output y);
	assign y = a?1:b;
endmodule
```

  #### Command steps :

Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog opt_check2.v
```
Synthesize the Design
```
synth -top opt_check2
```

![6 9](https://github.com/user-attachments/assets/0bbccf98-598d-42dc-a840-3d239973820b)


Now Generate the Netlist
```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Removes unused or redundant logic in the design and purges any dangling wires or gates.
```
opt_clean -purge
```
Now let's Create a Graphical Representation 

```
show
```
![6 10](https://github.com/user-attachments/assets/cfa8b4f5-3c2a-48ce-87e6-20c4d4f7c64d)



### 3.  3 input AND gate.

  The velilog code is given below :

```
module opt_check2(input a, input b, input c, output y);
	assign y = a?(b?c:0):0;
endmodule
```

  #### Command steps :

Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog opt_check3.v
```
Synthesize the Design
```
synth -top opt_check3
```

![6 11](https://github.com/user-attachments/assets/9c492893-2958-44dc-b974-962fce69d56b)



Now Generate the Netlist
```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Removes unused or redundant logic in the design and purges any dangling wires or gates.
```
opt_clean -purge
```
Now let's Create a Graphical Representation 

```
show
```
![6 12](https://github.com/user-attachments/assets/5daef2f7-6b4e-4a4b-b8c7-70bc620c4091)


### 4.  2 input XNOR Gate (3 input Boolean Logic)

  The velilog code is given below :

```
module opt_check2(input a, input b, input c, output y);
	assign y = a ? (b ? ~c : c) : ~c;
endmodule
```

  #### Command steps :

Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog opt_check4.v
```
Synthesize the Design
```
synth -top opt_check4
```

![6 13](https://github.com/user-attachments/assets/09459887-3925-40c0-ad92-01f4a4f0b0a1)


Now Generate the Netlist
```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Removes unused or redundant logic in the design and purges any dangling wires or gates.
```
opt_clean -purge
```
Now let's Create a Graphical Representation 

```
show
```
![6 14](https://github.com/user-attachments/assets/8468f875-6fcb-4bb1-b908-b0bced05c4a4)





### 5.  Multiple Module Optimization-1 

  The velilog code is given below :

```
module sub_module1(input a, input b, output y);
	assign y = a & b;
endmodule

module sub_module2 (input a, input b output y);
	assign y = a^b;
endmodule

module multiple_module_opt(input a, input b input c, input d output y);
	wire n1,n2, n3;

	sub_module1 U1 (.a(a), .b(1'b1), .y(n1));
	sub_module2 U2 (.a(n1), .b(1'b0), .y(n));
	sub_module2 U3 (.a(b), .b(d), .y(n3));

	assign y = c | (b & n1);
endmodule
```

  #### Command steps :

Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog multiple_module_opt.v
```
Synthesize the Design
```
synth -top multiple_module_opt
```

![6 15](https://github.com/user-attachments/assets/259e1099-a8bb-41cb-bc54-5b1aab2fb855)



Now Generate the Netlist
```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Removes unused or redundant logic in the design and purges any dangling wires or gates.
```
opt_clean -purge
```
Use of Flattening: Merges all hierarchical modules in the design into a single module to create a flat netlist for this just type
```
flatten
```

Now let's Create a Graphical Representation 

```
show
```
![6 16](https://github.com/user-attachments/assets/db4a0df2-5357-4c83-b17f-80a164e70c58)






### 6. Multiple Module Optimization-2 

  The velilog code is given below :

```
module sub_module(input a input b output y);
	assign y = a & b;
endmodule

module multiple_module_opt2(input a, input b input c, input d, output y);
	wire n1,n2, n3;

	sub_module U1 (.a(a), .b(1'b0), y(n));
	sub_module U2 (.a(b), .b(c), .y(n2));
	sub_module U3 (.a(n2), .b(d), .y(n));
	sub_module U4 (.a(n3), .b(n1), .y(y));
endmodule
```

  #### Command steps :

Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog multiple_module_opt2.v
```
Synthesize the Design
```
synth -top multiple_module_opt2
```

![6 17](https://github.com/user-attachments/assets/06e193bb-a307-4dc4-90aa-4ce4851fc7a4)


Now Generate the Netlist
```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Removes unused or redundant logic in the design and purges any dangling wires or gates.
```
opt_clean -purge
```

Use of Flattening: Merges all hierarchical modules in the design into a single module to create a flat netlist for this just type
```
flatten
```

Now let's Create a Graphical Representation 

```
show
```
![6 18](https://github.com/user-attachments/assets/ab77a558-89b1-4f08-9e7a-f977d7c4b1b3)



</details>




<details>
      <summary> LAB 7 (Day 3) : Optimization of various Sequential Designs </summary>
      
## LAB 7 - AIM : Optimization of various Sequential Designs 

### Optimization of various Sequential Designs 

- D-Flipflop Constant 1 with Asynchronous Reset (active low) 
- D-Flipflop Constant 2 with Asynchronous Reset (active high) 
- D-Flipflop Constant 3 with Synchronous Reset (active low) 
- D-Flipflop Constant 4 with Synchronous Reset (active high) 
- D-Flipflop Constant 5 with Synchronous Reset 
- Counter Optimization 1
- Counter Optimization 2

  
### 1. D-Flipflop Constant 1 with Asynchronous Reset (active low) 



The velilog code for the asynchronous reset (active low) is given below :
```
module dff_const1(input clk, input reset, output reg q); 
always @(posedge clk, posedge reset)
begin
	if(reset)
		q <= 1'b0;
	else
		q <= 1'b1;
end
endmodule
```

Testbench code is as follows:
```
module tb_dff_const1; 
	reg clk, reset;
	wire q;

	dff_const1 uut (.clk(clk),.reset(reset),.q(q));

	initial begin
		$dumpfile("tb_dff_const1.vcd");
		$dumpvars(0,tb_dff_const1);
		// Initialize Inputs
		clk = 0;
		reset = 1;
		#3000 $finish;
	end

	always #10 clk = ~clk;
	always #1547 reset=~reset;
endmodule
```

##### Command steps :

Go to the required directory
```
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```
We just need to put few commands as stated below in order to see the waveforms.

```
iverilog dff_const1.v tb_dff_const1.v
ls
```
After giving the above command the IVerilog stores the output as ' a.out '

Now let's execute the ' a.out ' file and observe the waveforms.

```
./a.out
gtkwave tb_dff_const1.vcd
```
Below is the Snapshot of the above commands and the resultant Waveforms:

![7 1 1](https://github.com/user-attachments/assets/960a1f0a-fae1-491c-9763-f88adeeffcd2)

OBSERVATION : From the waveform, it can be observed that the Q output is always high when reset is zero, and reset doesn't depend on clock edge.


### SYNTHESIS :

Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog dff_const1.v
```
Synthesize the Design
```
synth -top dff_const1
```

![7 2](https://github.com/user-attachments/assets/5a016f72-c01f-4f37-8cd9-74c901b062a0)



Now Generate the Netlist
```
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```

Now let's Create a Graphical Representation 

```
show
```
![7 3](https://github.com/user-attachments/assets/d425e026-786b-4c1f-84a3-481d4bddfcd6)


OBSERVATION : Since reset doesn't depend on clock edge, therefore the D Flip Flop has not been removed.




### 2. D-Flipflop Constant 2 with Asynchronous Reset (active high) 



The velilog code for the asynchronous reset (active high) is given below :
```
module dff_const1(input clk, input reset, output reg q); 
always @(posedge clk, posedge reset)
begin
	if(reset)
		q <= 1'b1;
	else
		q <= 1'b1;
end
endmodule
```

Testbench code is as follows:
```
module tb_dff_const2; 
	reg clk, reset;
	wire q;

	dff_const2 uut (.clk(clk),.reset(reset),.q(q));

	initial begin
		$dumpfile("tb_dff_const1.vcd");
		$dumpvars(0,tb_dff_const1);
		// Initialize Inputs
		clk = 0;
		reset = 1;
		#3000 $finish;
	end

	always #10 clk = ~clk;
	always #1547 reset=~reset;
endmodule
```

##### Command steps :

Go to the required directory
```
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```
We just need to put few commands as stated below in order to see the waveforms.

```
iverilog dff_const2.v tb_dff_const2.v
ls
```
After giving the above command the IVerilog stores the output as ' a.out '

Now let's execute the ' a.out ' file and observe the waveforms.

```
./a.out
gtkwave tb_dff_const2.vcd
```
Below is the Snapshot of the above commands and the resultant Waveforms:

![7 4](https://github.com/user-attachments/assets/19d5fd4b-97e1-4754-b661-2d2b9f882ad3)


OBSERVATION : From the waveform, it can be observed that the Q output is always high irrespective of reset.

### SYNTHESIS :

Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog dff_const2.v
```
Synthesize the Design
```
synth -top dff_const2
```
![7 5](https://github.com/user-attachments/assets/5687c6d2-81eb-4350-8f40-284a4e110b23)

OBSERVATION : None D Flip Flop has been synthesised.


Now Generate the Netlist
```
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```

Now let's Create a Graphical Representation 

```
show
```
![7 6](https://github.com/user-attachments/assets/78dbc377-8b1c-4887-8716-a7df71e45cec)



OBSERVATION : Since output q doesn't depend on reset edgeand is always 1, therefore the D Flip Flop has been removed.


### 3. D-Flipflop Constant 3 with Synchronous Reset (active low) 



The velilog code for the synchronous reset (active low) is given below :
```
module dff_const3(input clk, input reset, output reg q); 
	reg q1;

	always @(posedge clk, posedge reset)
	begin
		if(reset)
		begin
			q <= 1'b1;
			q1 <= 1'b0;
		end
		else
		begin	
			q1 <= 1'b1;
			q <= q1;
		end
	end
endmodule
```

Testbench code is as follows:
```
module dff_const3(input clk, input reset, output reg q); 
	reg q1;

	always @(posedge clk, posedge reset)
	begin
		if(reset)
		begin
			q <= 1'b1;
			q1 <= 1'b0;
		end
		else
		begin	
			q1 <= 1'b1;
			q <= q1;
		end
	end
endmodule
```


### SYNTHESIS :



##### Command steps :


Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog dff_const3.v
```
Synthesize the Design
```
synth -top dff_const3
```

![7 7](https://github.com/user-attachments/assets/301ea84d-04a9-4122-9501-9e5205878161)




Now Generate the Netlist
```
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```

Now let's Create a Graphical Representation 

```
show
```

![7 8](https://github.com/user-attachments/assets/e4c3335c-5ab3-4759-a725-388468554fc3)



OBSERVATION : This module defines a D flip-flop, for a positive edge of reset, q is set to 1 and q1 is set to 0. On each clock cycle, q1 is set to 1, and q is updated with the value of q1.

When synthesized, the design will result in a flip-flop where q becomes 1 after the first clock cycle post-reset and stays 1 afterward.



### 4. D-Flipflop Constant 4 with Synchronous Reset (active high) 



The velilog code for the synchronous reset (active high) is given below :
```
module dff_const4(input clk, input reset, output reg q); 
	reg q1;

	always @(posedge clk, posedge reset)
	begin
		if(reset)
		begin
			q <= 1'b1;
			q1 <= 1'b1;
		end
		else
		begin	
			q1 <= 1'b1;
			q <= q1;
		end
	end
endmodule
```




### SYNTHESIS :



##### Command steps :


Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog dff_const4.v
```
Synthesize the Design
```
synth -top dff_const4
```
![7 9](https://github.com/user-attachments/assets/e8047d94-d12e-4bf4-aed6-8d89cc526e87)





Now Generate the Netlist
```
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```

Now let's Create a Graphical Representation 

```
show
```

![7 10](https://github.com/user-attachments/assets/3967c1cd-3e5d-4833-8f3f-8494ad9c221c)




OBSERVATION : This module defines a D flip-flop that sets both q and q1 to 1 on a positive edge of reset. On each clock cycle, q1 remains 1, and q is updated with the value of q1 (which is always 1).

When synthesized, the design will result in a flip-flop where q is always 1, regardless of the reset or clock state.




### 5. D-Flipflop Constant 5 with Synchronous Reset 



The velilog code for the synchronous reset is given below :
```
module dff_const5(input clk, input reset, output reg q); 
	reg q1;

	always @(posedge clk, posedge reset)
	begin
		if(reset)
		begin
			q <= 1'b0;
			q1 <= 1'b0;
		end
		else
		begin	
			q1 <= 1'b1;
			q <= q1;
		end
	end
endmodule
```




### SYNTHESIS :



##### Command steps :


Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog dff_const5.v
```
Synthesize the Design
```
synth -top dff_const5
```
![7 11](https://github.com/user-attachments/assets/d2600ce5-c6e0-40ea-b9d8-2eaf2f9211f5)





Now Generate the Netlist
```
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```

Now let's Create a Graphical Representation 

```
show
```

![7 12](https://github.com/user-attachments/assets/45062df5-1ba3-4758-86be-0814aa9b46d6)





OBSERVATION : This module defines a D flip-flop that resets both q and q1 to 0 on a positive edge of reset. On each clock cycle, it sets q1 to 1 and then updates q with the value of q1 (which will always be 1 after the first cycle).

When synthesized, the design will result in a flip-flop where q is always 1 after the first clock cycle post-reset.



### 6. Counter Optimization 1



The velilog code for the Counter Optimization 1 is given below :
```
module counter_opt (input clk, input reset, output q);
	reg [2:0] count;
	assign q = count[0];
	
	always @(posedge clk,posedge reset)
	begin
		if(reset)
			count <= 3'b000;
		else
			count <= count + 1;
	end
endmodule
```




### SYNTHESIS :



##### Command steps :


Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog counter_opt.v
```
Synthesize the Design
```
synth -top counter_opt
```
![7 13](https://github.com/user-attachments/assets/863ddf5e-772b-4269-9311-0c833a39a1ed)






Now Generate the Netlist
```
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```

Now let's Create a Graphical Representation 

```
show
```
![7 14](https://github.com/user-attachments/assets/386dcafb-b067-4e3a-af78-e00a56d1c80a)


### 7. Counter Optimization 2



The velilog code for the synchronous reset (active high) is given below :
```
module counter_opt2 (input clk, input reset, output q);
	reg [2:0] count;
	assign q = (count[2:0] == 3'b100);
	
	always @(posedge clk,posedge reset)
	begin
		if(reset)
			count <= 3'b000;
		else
			count <= count + 1;
	end
endmodule
```




### SYNTHESIS :



##### Command steps :


Go to the required directory
```
cd ~
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog counter_opt2.v
```
Synthesize the Design
```
synth -top counter_opt2
```


Now Generate the Netlist
```
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```

Now let's Create a Graphical Representation 

```
show
```
![7 15](https://github.com/user-attachments/assets/079da7f8-fb5b-4ad7-adcb-9e0ff187cc7e)

</details>








<details>
      <summary> LAB 8 (Day 4) : GLS, Synthesis-Simulation mismatch, non - blocking and blocking statements. </summary>
      
## LAB 8 - AIM : GLS, Synthesis-Simulation mismatch, non - blocking and blocking statements.

#### Gate Level Simulation (GLS) 

Gate Level Simulation (GLS) is a crucial step in the verification process of digital circuits. It involves simulating the synthesized netlist, which is a lower-level representation of the design, using a testbench to verify its logical correctness and timing behavior. By comparing the simulated outputs to the expected outputs, GLS ensures that the synthesis process has not introduced any errors and that the design meets its performance requirements.

![8 1](https://github.com/user-attachments/assets/10326a9f-b394-4414-b146-22b84d053742)

Sensitivity lists are crucial for accurate circuit behavior. If a sensitivity list is incomplete, it can lead to unexpected latches. Blocking and non-blocking assignments within always blocks have different execution behaviors. Incorrect use of blocking assignments can unintentionally create latches, causing synthesis and simulation mismatches. To avoid these issues, it's essential to carefully analyze circuit behavior and ensure that the sensitivity list and assignments align with the desired functionality.


#### GLS Simulation

- ### Example 1: 2 x 1 MUX using ternary operator

Verilog code:
```
module ternary_operator_mux (input i0 , input i1 , input sel , output y);
assign y = sel?i1:i0;
endmodule
```
Command steps for Simulation:

```
iverilog ternary_operator_mux.v tb_ternary_operator_mux.v
./a.out
gtkwave tb_ternary_operator_mux.vcd
```

![8 2](https://github.com/user-attachments/assets/71d48e0e-780e-4dd6-8ce8-0d1f0816f8d2)


#### Synthesis: 

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog ternary_operator_mux.v
```
Synthesize the Design
```
synth -top ternary_operator_mux
```

Now Generate the Netlist
```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
```

Now let's Create a Graphical Representation 

```
show
```

![8 3](https://github.com/user-attachments/assets/a1a2b22b-7b23-4658-9b54-d8012bdcae34)

To see the Netlist
```
write_verilog -noattr ternary_operator_mux_net.v
!gvim ternary_operator_mux_net.v
```

![8 4](https://github.com/user-attachments/assets/4cd08852-37e3-4ccf-8bcc-2d8740cdadd3)

#### Gate Level Synthesis (GLS)

##### Command steps :

Go to the required directory
```
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```
We just need to put few commands as stated below in order to see the waveforms.

```
iverilog ../my_lib/verilog_model/primitives.v ../my_lib/verilog_model/sky130_fd_sc_hd.v ternary_operator_mux_net.v tb_ternary_operator_mux.v
ls
```
After giving the above command the IVerilog stores the output as ' a.out '

Now let's execute the ' a.out ' file and observe the waveforms.

```
./a.out
gtkwave tb_ternary_operator_mux.vcd
```
Below is the Snapshot of the above commands and the resultant Waveforms:

![8 5](https://github.com/user-attachments/assets/82f920b2-6478-4759-8f71-a5ea6d58b167)

These waveforms correspond to the GATE LEVEL SYNTHESIS for the Ternary Operator MUX.


- ### Example 2: Design of a 2:1 Bad MUX

Verilog code:
```
module bad_mux(input i0, input i1, input sel, output reg y);
	always@(sel)
	begin
		if(sel)
			y <= i1;
		else
			y <= i0;
	end
endmodule
```
Command steps for Simulation:

```
iverilog bad_mux.v tb_bad_mux.v
./a.out
gtkwave tb_bad_mux.vcd
```

![8 6](https://github.com/user-attachments/assets/7364da41-eda0-4255-8d6c-32ecdc3a6f07)

From the waveform it can be observed that the output y changes only when there is a change in select line, completely ignoring the change in i0 and i1, which should also change the output y. Thus, this design is that of a bad MUX.

#### Synthesis: 

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog bad_mux.v
```
Synthesize the Design
```
synth -top bad_mux
```

Now Generate the Netlist
```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
```

Now let's Create a Graphical Representation 

```
show
```

![8 7](https://github.com/user-attachments/assets/aa8e8bb1-2a08-4a9e-87cb-7f9d095158b8)


To see the Netlist
```
write_verilog -noattr bad_mux_net.v
!gvim bad_mux_net.v
```

![8 8](https://github.com/user-attachments/assets/8112e953-0364-468e-9217-4b767db01e26)

From the waveform it can be observed that the output y changes only when there is a change in select line, completely ignoring the change in i0 and i1, which should also change the output y. Thus, this design is that of a bad MUX.


#### Gate Level Synthesis (GLS)

##### Command steps :

Go to the required directory
```
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```
We just need to put few commands as stated below in order to see the waveforms.

```
iverilog ../my_lib/verilog_model/primitives.v ../my_lib/verilog_model/sky130_fd_sc_hd.v bad_mux.v tb_bad_mux.v
ls
```
After giving the above command the IVerilog stores the output as ' a.out '

Now let's execute the ' a.out ' file and observe the waveforms.

```
./a.out
gtkwave tb_bad_mux.vcd
```
Below is the Snapshot of the above commands and the resultant Waveforms:

![8 9](https://github.com/user-attachments/assets/a2b59280-1910-4b91-aa7f-0cc1e2394b40)

These waveforms correspond to the GATE LEVEL SYNTHESIS for the Bad MUX.



- ### Example 3: Blocking Caveat


Verilog code:
```
module blocking_caveat(input a, input b, input c, output reg d);
	reg x;

	always@(*)
	begin
		d = x & c;
		x = a | b;
	end
endmodule
```
Command steps for Simulation:

```
iverilog blocking_caveat.v tb_blocking_caveat.v
./a.out
gtkwave tb_blocking_caveat.vcd
```

![8 10](https://github.com/user-attachments/assets/ab22f0c2-befc-4ba6-a513-1b4457d712b7)


As depicted, when A and B go zero, the OR gate output should be zero (X equal to zero), and the AND gate output should also be zero (same as D output). But, the AND gate input of X takes the previous value of A|B equal to one, based on the design created by the blocking statement, hence the discrepancy in the output.


#### Synthesis: 

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files
```
read_verilog blocking_caveat.v
```
Synthesize the Design
```
synth -top blocking_caveat
```

Now Generate the Netlist
```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
```

Now let's Create a Graphical Representation 

```
show
```
![8 11](https://github.com/user-attachments/assets/203389e6-0374-41d6-b98f-fd6ae21a34f9)



To see the Netlist
```
write_verilog -noattr blocking_caveat_net.v
!gvim blocking_caveat_net.v
```
![8 12](https://github.com/user-attachments/assets/3f888c1b-3b1b-498a-9920-a33531cea4c1)




#### Gate Level Synthesis (GLS)

##### Command steps :

Go to the required directory
```
sudo -i
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files
```
We just need to put few commands as stated below in order to see the waveforms.

```
iverilog ../my_lib/verilog_model/primitives.v ../my_lib/verilog_model/sky130_fd_sc_hd.v blocking_caveat_net.v tb_blocking_caveat.v
ls
```
After giving the above command the IVerilog stores the output as ' a.out '

Now let's execute the ' a.out ' file and observe the waveforms.

```
./a.out
gtkwave tb_blocking_caveat.vcd
```
Below is the Snapshot of the above commands and the resultant Waveforms:

![8 14](https://github.com/user-attachments/assets/a0249fde-a9c6-4651-be4f-4d5f87f53dd1)

These waveforms correspond to the GATE LEVEL SYNTHESIS for the Blocking Caveat.


</details>



# TASK 11      
( 22/10/2024 )

<details>
       <summary> Synthesize RISC-V and compare output with functional simulations. </summary>

## AIM : To Synthesize RISC-V and compare output with functional simulations.  </summary>


## Steps 

Copy the src folder from your VSDBabySoC folder to your VLSI folder.
Now copy the src folder into the sky130RTLDesignAndSynthesisWorkshop folder by giving the following command:
```
sudo -i
cd /home/chandra-shekhar-jha/VLSI/
cp -r src sky130RTLDesignAndSynthesisWorkshop/
```
Now go the required Directory: 

```
cd ~
cd /home/chandra-shekhar-jha/VLSI/sky130RTLDesignAndSynthesisWorkshop/src/module
```

# Synthesis: 

This will invoke/start the yosys
```
yosys       
```
Read the library 
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
Read the design verilog files :
```
read_verilog clk_gate.v
read_verilog rvmyth.v

```
Synthesize the Design
```
synth -top rvmyth
```
![new1](https://github.com/user-attachments/assets/270f0624-4c87-48d4-8d5f-bc126c16c323)

Now Generate the Netlist
```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
```

Now let's Create a Graphical Representation 

```
show
```
![Screenshot 2024-10-23 225930](https://github.com/user-attachments/assets/611443cb-d750-409e-88c9-3d6d1fc0053a)


To View the Netlist
```
write_verilog -noattr rvmyth.v
!gvim rvmyth.v
exit
```
![new2](https://github.com/user-attachments/assets/06a186f0-9580-49cb-b226-8edd6b9fd454)



Now let`s Observe the output waveform of synthesised RISC-V
```
iverilog ../../my_lib/verilog_model/primitives.v ../../my_lib/verilog_model/sky130_fd_sc_hd.v rvmyth.v testbench.v vsdbabysoc.v avsddac.v avsdpll.v clk_gate.v
ls
./a.out
gtkwave dump.vcd
```
![Screenshot from 2024-10-23 20-09-56](https://github.com/user-attachments/assets/c6db6f2a-6a7b-4827-9416-fbabba5ea513)

![Untitled](https://github.com/user-attachments/assets/f471cd9f-fb86-4801-89b2-a7265eca0b47)


# Functional Simulations ( Previously done in TASK-9 )

 ### Command Steps :
 ```
cd ~
cd VSDBabySoC
iverilog -o ./pre_synth_sim.out -DPRE_SYNTH_SIM src/module/testbench.v -I src/include -I src/module/
./pre_synth_sim.out
gtkwave pre_synth_sim.vcd
```
![Screenshot from 2024-10-23 19-21-41](https://github.com/user-attachments/assets/990fa4dd-fb8b-4bab-8c92-3092bc7c2a24)



# COMPARISON of Functionality vs Synthesized output waveform 

![Untitled0](https://github.com/user-attachments/assets/67a35d2e-75f0-4935-b47c-7f957c13485e)

## CONCLUSION : The Functionality vs Synthesized output waveform matches.  

</details>






# TASK 12      
( 24/10/2024 )

<details>
       <summary>  Static Timing Analysis for Synthesized Risc-V Core using OpenSTA </summary>

## AIM :  Static Timing Analysis for Synthesized Risc-V Core using OpenSTA  </summary>

### What is STA?
Static Timing Analysis (STA) is a method used in digital circuit design to verify the timing performance of a circuit without requiring dynamic simulation. It checks whether the circuit meets its timing constraints by analyzing the timing paths in the design. Here are some key aspects of STA:

1. Timing Paths: STA evaluates all possible paths through a circuit from input to output, taking into account the propagation delays of gates and interconnects.
2. Setup and Hold Times: It checks for setup and hold time violations. The setup time is the minimum time before the clock edge that the input data must be stable, while the hold time is the minimum time after the clock edge that the data must remain stable.
3. Clock Constraints: STA incorporates clock definitions, including the clock frequency, period, and any variations (like skew or jitter).
4. Worst-case Scenario: STA assumes worst-case conditions for delay values (like maximum load, temperature, and voltage) to ensure that the circuit will perform correctly under all expected operating conditions.
5. Tools: There are various tools for performing STA, such as Synopsys PrimeTime, Cadence Tempus, and others, which automate the process and provide detailed reports on timing violations.
Overall, STA is crucial for ensuring that digital circuits operate reliably at the intended speeds and for identifying potential timing issues early in the design process.
### Why STA is performed ?
Static Timing Analysis (STA) is performed for several critical reasons in digital circuit design:
1. Timing Verification: STA ensures that the design meets its specified timing constraints. It verifies that data signals can propagate through the circuit within the required time limits, ensuring that outputs are stable and valid when needed.
2. Identify Timing Violations: It helps identify setup and hold time violations, which can lead to incorrect operation of flip-flops and other sequential elements. Detecting these violations is crucial to ensure the reliability of the circuit.
3. Performance Optimization: By analyzing the timing paths, designers can identify critical paths that limit the maximum operating frequency. This information can be used to optimize the design by resizing gates, adjusting the layout, or modifying the clock strategy.
4. Early Detection of Issues: STA allows for early detection of timing issues during the design process, reducing the risk of costly iterations and revisions in later stages, such as post-layout or during fabrication.
5. Power Consumption Analysis: Timing analysis can also help in understanding the impact of clock frequency on power consumption. By ensuring that the design runs at optimal speeds, designers can balance performance and power efficiency.
6. Design Validation: STA provides a level of assurance that the design will work correctly under the specified operating conditions. It validates the design against its intended specifications and requirements.
7. Automation: STA tools can automatically analyze complex designs, making it more efficient than traditional dynamic simulations, especially for large-scale integrated circuits.
8. Support for Variability: STA can incorporate variations in manufacturing processes, temperature, and voltage (PVT variations) to ensure robust performance across different conditions.
In summary, STA is essential for ensuring the functionality, reliability, and performance of digital circuits, enabling designers to create high-quality, efficient designs.
### What is reg2reg Path ?
A reg2reg path (register-to-register path) refers to a timing path in a digital circuit that connects two sequential elements, specifically flip-flops or registers. This path is crucial in the context of Static Timing Analysis (STA) because it represents the flow of data from one register to another through combinational logic.
Reg2reg paths are essential for ensuring proper data flow and synchronization in digital circuits, especially in designs with pipelining or sequential operations. Analyzing these paths helps in verifying that the data processing occurs correctly across clock cycles, thereby ensuring the overall functionality and reliability of the circuit.
#### Key characteristics of reg2reg Path
1. **Sequential Logic**: Reg2reg paths are part of sequential circuits where data is stored in registers and passed from one register to another after being processed by combinational logic.
2. **Setup and Hold Timing**:
   * **Hold Time**: Reg2reg paths are analyzed for setup time constraints to ensure that the data output from the first register (FF1) arrives at the second register (FF2) before the clock edge that triggers FF2.
   * **Hold Time**: These paths are also evaluated for hold time constraints to ensure that the data remains stable at the input of FF2 for a specified period after the clock edge that triggers FF1.
3. **Combinational Logic Delay**: The timing analysis of a reg2reg path includes the propagation delay through the combinational logic that connects the two registers. This delay can vary based on the logic elements and their configuration.
4. **Critical Paths**: Reg2reg paths can often be critical paths if they take longer than other paths in the design, which can limit the maximum operating frequency of the circuit.
5. **Path Analysis**: STA tools evaluate reg2reg paths to check for timing violations, allowing designers to optimize the circuit by adjusting the logic, resizing gates, or modifying the layout.
6. **Clock Domain Crossing**: If the two registers belong to different clock domains, additional considerations for metastability and synchronization are needed, which complicates the reg2reg timing analysis.
### What is clk2reg Path ?
A clk2reg path (clock-to-register path) refers to a timing path in a digital circuit that connects the clock signal to a register (flip-flop). This path is crucial for ensuring that the register operates correctly in response to clock events. Here are the key aspects of clk2reg paths:
1. **Clock Signal Propagation**: The clk2reg path represents the time it takes for the clock signal to reach the register from the clock source, including any delays introduced by clock buffers or routing.
2. **Setup Timing**: In the context of setup timing analysis, the clk2reg path is important for determining when the data signal must arrive at the register relative to the clock edge. The analysis ensures that the clock arrives at the register before the data input becomes stable, meeting the setup time requirement.
3. **Clock Delay**: This path is evaluated for the delay introduced by any clock distribution elements, such as buffers and inverters, that may be part of the clock tree. The total delay impacts the timing of when the register captures the input data.
4. **Critical Paths**: A clk2reg path can become a critical path if the delay through this path is significant enough to affect the maximum frequency of operation for the circuit.
5. **Hold Timing**: Although clk2reg paths are primarily associated with setup time analysis, they can also be relevant for hold time analysis, especially in cases where the clock signal may have some jitter or variations that could affect timing margins.
6. **Clock Diagram Crossing**: If the register is part of a different clock domain, the clk2reg analysis will also involve considerations for synchronization and potential metastability issues.
### STA for the synthesized RISC-V Core
Here, in this activity we will be generating setup and hold timing reports for our Synthesized RISC-V Core module.


Following are the commands to generate the reports,

```
cd OpenSTA/app
./sta

read_liberty -min ./lib/sta/sky130_fd_sc_hd__tt_025C_1v80.lib
read_liberty -max ./lib/sta/sky130_fd_sc_hd__tt_025C_1v80.lib
read_liberty -min ./lib/avsdpll.lib
read_liberty -max ./lib/avsdpll.lib
read_liberty -min ./lib/avsddac.lib
read_liberty -max ./lib/avsddac.lib
read_verilog ./src/module/vsdbabysoc_synth.v
link_design vsdbabysoc

create_clock -name clk -period 9.65 [get_ports clk]
set_clock_uncertainty [expr 0.05 * 9.65] -setup [get_clocks clk]
set_clock_uncertainty [expr 0.08 * 9.65] -hold [get_clocks clk]
set_clock_transition [expr 0.05 * 9.65] [get_clocks clk]
set_input_transition [expr 0.08 * 9.65] [all_inputs]
```


- The clock period has been specified as 9.65 ns.
- The setup uncertainity is 5% of the defined clock period
- The clock transition is defined as 5% of the defined clock period
- The hold uncertainity is set as 8% of the clock period
- The input data transition is set as 8% of the defined clock period




![111111111](https://github.com/user-attachments/assets/62e51b76-0db8-40bb-b65c-d977c3623219)


```
report_checks -path_delay max

```
In the below screenshot, we can observe the timing report for a reg2reg max path,
![Screenshot from 2024-10-28 22-52-46](https://github.com/user-attachments/assets/74a01fe3-20ac-4e66-a600-28f45697c7f2)


```
report_checks -path_delay min
```
Below screenshot shows the reg2reg min path report,

![22222222222](https://github.com/user-attachments/assets/b07578e9-26b4-4b3f-b814-34f73ad1c422)

The max path report is for the Setup Slack and the min path report is for the Hold Slack.

</details>





# TASK 13      
( 29/10/2024 )

<details>
       <summary>  PVT Corner Analysis for Synthesized VSDBabySoC using OpenSTA </summary>

## AIM :  PVT Corner Analysis for Synthesized VSDBabySoC using OpenSTA  </summary>


The PVT corner refers to the combination of Process, Voltage, and Temperature variations that a semiconductor chip might encounter during its operation. These variations can affect the performance, power consumption, and reliability of the chip, so they are simulated to ensure the chip functions correctly under different conditions The below tcl script sta_pvt.tcl can be run to performt the STA across the PVT corners for which the sky130 lib files are available:

The below tcl script sta_pvt.tcl can be run to performt the STA across the PVT corners for which the sky130 lib files are available:

```
set list_of_lib_files(1) "sky130_fd_sc_hd__ff_100C_1v65.lib"
set list_of_lib_files(2) "sky130_fd_sc_hd__ff_100C_1v95.lib"
set list_of_lib_files(3) "sky130_fd_sc_hd__ff_n40C_1v56.lib"
set list_of_lib_files(4) "sky130_fd_sc_hd__ff_n40C_1v65.lib"
set list_of_lib_files(5) "sky130_fd_sc_hd__ff_n40C_1v76.lib"
set list_of_lib_files(6) "sky130_fd_sc_hd__ff_n40C_1v95.lib"
set list_of_lib_files(7) "sky130_fd_sc_hd__ff_n40C_1v95_ccsnoise.lib.part1"
set list_of_lib_files(8) "sky130_fd_sc_hd__ff_n40C_1v95_ccsnoise.lib.part2"
set list_of_lib_files(9) "sky130_fd_sc_hd__ff_n40C_1v95_ccsnoise.lib.part3"
set list_of_lib_files(10) "sky130_fd_sc_hd__ss_100C_1v40.lib"
set list_of_lib_files(11) "sky130_fd_sc_hd__ss_100C_1v60.lib"
set list_of_lib_files(12) "sky130_fd_sc_hd__ss_n40C_1v28.lib"
set list_of_lib_files(13) "sky130_fd_sc_hd__ss_n40C_1v35.lib"
set list_of_lib_files(14) "sky130_fd_sc_hd__ss_n40C_1v40.lib"
set list_of_lib_files(15) "sky130_fd_sc_hd__ss_n40C_1v44.lib"
set list_of_lib_files(16) "sky130_fd_sc_hd__ss_n40C_1v60.lib"
set list_of_lib_files(17) "sky130_fd_sc_hd__ss_n40C_1v60_ccsnoise.lib.part1"
set list_of_lib_files(18) "sky130_fd_sc_hd__ss_n40C_1v60_ccsnoise.lib.part2"
set list_of_lib_files(19) "sky130_fd_sc_hd__ss_n40C_1v60_ccsnoise.lib.part3"
set list_of_lib_files(20) "sky130_fd_sc_hd__ss_n40C_1v76.lib"
set list_of_lib_files(21) "sky130_fd_sc_hd__tt_025C_1v80.lib"
set list_of_lib_files(22) "sky130_fd_sc_hd__tt_100C_1v80.lib"

for {set i 1} {$i <= [array size list_of_lib_files]} {incr i} {
read_liberty lib/$list_of_lib_files($i)
read_verilog module/vsdbabysoc_synth.v
link_design vsdbabysoc
read_sdc sdc/vsdbabysoc_synthesis.sdc
check_setup -verbose
report_checks -path_delay min_max -fields {nets cap slew input_pins fanout} -digits {4} > /home/chandra-shekhar-jha/VSDBabySoC/src/sta_output/min_max_$list_of_lib_files($i).txt

exec echo "$list_of_lib_files($i)" >> /home/chandra-shekhar-jha/VSDBabySoC/src/sta_output/sta_worst_max_slack.txt
report_worst_slack -max -digits {4} >> /home/chandra-shekhar-jha/VSDBabySoC/src/sta_output/sta_worst_max_slack.txt

exec echo "$list_of_lib_files($i)" >> /home/chandra-shekhar-jha/VSDBabySoC/src/sta_output/sta_worst_min_slack.txt
report_worst_slack -min -digits {4} >> /home/chandra-shekhar-jha/VSDBabySoC/src/sta_output/sta_worst_min_slack.txt

exec echo "$list_of_lib_files($i)" >> /home/chandra-shekhar-jha/VSDBabySoC/src/sta_output/sta_tns.txt
report_tns -digits {4} >> /home/chandra-shekhar-jha/VSDBabySoC/src/sta_output/sta_tns.txt

exec echo "$list_of_lib_files($i)" >> /home/chandra-shekhar-jha/VSDBabySoC/src/sta_output/sta_wns.txt
report_wns -digits {4} >> /home/chandra-shekhar-jha/VSDBabySoC/src/sta_output/sta_wns.txt



```
The SDC file used for generating clock and data constraints is given below:

```
set PERIOD 9.65

set_units -time ns
create_clock [get_ports clk] -name clk -period $PERIOD
set_clock_uncertainty -setup  [expr $PERIOD * 0.05] [get_clocks clk]
set_clock_transition [expr $PERIOD * 0.05] [get_clocks clk]
set_clock_uncertainty -hold [expr $PERIOD * 0.08] [get_clocks clk]
set_input_transition [expr $PERIOD * 0.08] [get_ports ENb_CP]
set_input_transition [expr $PERIOD * 0.08] [get_ports ENb_VCO]
set_input_transition [expr $PERIOD * 0.08] [get_ports REF]
set_input_transition [expr $PERIOD * 0.08] [get_ports VCO_IN]
set_input_transition [expr $PERIOD * 0.08] [get_ports VREFH]
```

Run below commands on terminal to source the sta_pvt.tcl file:

![Screenshot from 2024-11-04 23-30-33](https://github.com/user-attachments/assets/e8fa571d-3da1-4edb-b6bf-35a55f7eb864)


A table comprising of the slacks report is shown below: 
![Screenshot from 2024-11-05 00-01-30](https://github.com/user-attachments/assets/948954ea-e638-4565-a4e5-743696034741)



Total Negative Slack:Column1

![Screenshot from 2024-11-05 00-08-33](https://github.com/user-attachments/assets/cc310cfb-daae-46d9-8675-747b8534de10)


Worst (Negative slack)Setup Slack:Column2
![Screenshot from 2024-11-05 00-12-10](https://github.com/user-attachments/assets/bb48cfde-7f63-453a-81e8-ba4c668e23ea)


Worst Setup Slack:Column3
![Screenshot from 2024-11-05 00-24-39](https://github.com/user-attachments/assets/ab16ed0e-ca7a-4d83-bed2-4d436b477465)


Worst Hold Slack:Column4
![Screenshot from 2024-11-05 00-27-14](https://github.com/user-attachments/assets/afd69f00-2081-474f-914d-f4894193590d)



### Conclusion:

#### From the above analysis we can conclude that

- sky130_fd_sc_hd__ss_n40C_1v28.lib Library file has the worst setup slack
- sky130_fd_sc_hd__ff_100C_1v95.lib Library file has the worst hold slack

</details>







# TASK 14      
( 07/11/2024 )

<details>
       <summary>DAY 1 :  Inception of open-source EDA, OpenLane and Sky130 PDK. </summary>

## AIM :Advanced Physical Design using OpenLane using Sky130. 

**QFN-48 Package:** A Quad Flat No-leads (QFN) 48 package is a leadless IC package with 48 connection pads around the perimeter. It offers good thermal and electrical performance in a compact form, making it ideal for high-density applications.

![image](https://github.com/user-attachments/assets/2237a9ef-dc38-444f-97a5-ceb4e983c8f0)


**Chip:** An integrated circuit (IC) that contains various functional blocks like memory, processing units, and I/O in a silicon substrate, typically used for specific applications in electronics.

![image](https://github.com/user-attachments/assets/7503bcea-4654-4bc9-b77a-de9ced7929be)


**Pads:** Small metallic areas on a chip or package used to connect internal circuitry to external connections, enabling signals to be transferred to and from the IC.

**Core:** The central part of a chip containing the main processing unit and functional logic, often optimized for power and performance.

**Die:** The section of a silicon wafer containing an individual IC before it is packaged, housing all active circuits and elements for the chip's functions.

![image](https://github.com/user-attachments/assets/cfa2c482-59c5-4ad5-b74c-a027bfdf16b8)


**IPs (Intellectual Properties):** Pre-designed functional blocks or modules within a chip, such as USB controllers or memory interfaces, licensed for reuse across various designs to save time and cost.

![image](https://github.com/user-attachments/assets/1039a7d9-0286-42c7-8da7-17136c3da5aa)


**From Software Applications to Hardware Flow**

To run an application on hardware, several processes take place. First, the application enters a layer known as the system software, which prepares it for execution by translating the application program into binary format, understandable by hardware. Key components within system software include the Operating System (OS), Compiler, and Assembler.

The process starts with the OS, which breaks down application functions written in high-level languages such as C, C++, Java, or Visual Basic. These functions are passed to a suitable compiler, which translates them into low-level instructions. The syntax and format of these instructions are tailored to the specific hardware architecture in use.

Next, the assembler converts these hardware-specific instructions into binary format, known as machine language. This binary code is then fed to the hardware, enabling it to perform specific tasks as defined by the received instructions.

![image](https://github.com/user-attachments/assets/14788472-7c91-4860-82c6-2bccb49f91d2)

For example, consider a stopwatch app running on a RISC-V core. Here, the OS might generate a small function in C, which is then passed to a compiler. The compiler outputs RISC-V-specific instructions, tailored to the architecture. These instructions are subsequently processed by the assembler, which converts them into binary code. This binary code then flows into the chip layout, where the hardware executes the desired functionality.

![image](https://github.com/user-attachments/assets/cabbd8f7-f0c4-4a13-bf2e-d6d67392910e)

For the above stopwatch the below figure shows the input and output of the compiler and assembler.

![image](https://github.com/user-attachments/assets/63f2e771-eed8-4953-b501-dd9ff0d209f7)

The compiler generates architecture-specific instructions, while the assembler produces the corresponding binary patterns. To execute these instructions on hardware, an RTL (written in a Hardware Description Language) is used to interpret and implement the instructions. This RTL design is then synthesized into a netlist, represented as interconnected logic gates. Finally, the netlist undergoes physical design implementation to be fabricated onto the chip.

![image](https://github.com/user-attachments/assets/ae0a287d-8bb4-4535-b6b0-5b1baf09008d)

**Components of ASIC Design**

![image](https://github.com/user-attachments/assets/560b728b-8e75-4c9d-a3c8-5b640318c4aa)

- RTL IPs: Pre-designed, verified digital circuit blocks (like adders, flip-flops, memory) in HDL (e.g., Verilog, VHDL). They save design time by providing ready-to-use components for complex circuits.

- EDA Tools: Software that automates ASIC design tasks (e.g., synthesis, optimization, placement, timing analysis). Essential for improving productivity and ensuring performance and power requirements are met.

- PDK Data: A set of files and parameters from a semiconductor foundry, detailing its manufacturing process (e.g., transistor models, design rules). PDKs ensure ASIC designs are compatible with the foundry’s fabrication process.

**Simplified RTL to GDS flow**

![image](https://github.com/user-attachments/assets/1f2a5455-d83e-46fe-92e3-531ade2a9add)

- **RTL Design:** Describes the circuit's functional behavior using HDLs like Verilog or VHDL, defining its logic and data paths.

- **RTL Synthesis:** Converts RTL code to a gate-level netlist which is a collection of standard cells like AND gates, flip-flops, and multiplexers by mapping it to standard cells and optimizing for area, power, and timing. 

- **Floor and Power Planning:** Partitions chip area, places major components, and defines power grid and I/O placement to optimize area, power distribution, and signal flow. This step optimizes the physical layout, aiming to reduce power consumption and improve signal integrity by considering the placement of I/O pads and power distribution cells

- **Placement:** Assigns physical locations to cells, aiming to minimize wirelength, reduce signal delay, and meet design constraints. The placement tool carefully arranges the cells to balance the overall chip design for optimal performance and area utilization.

- **Clock Tree Synthesis (CTS):** Clock Tree Synthesis (CTS) is a critical step that focuses on creating an optimized clock distribution network. CTS ensures the clock is distributed evenly to all flip-flops and registers. It builds an optimized clock network to balance clock signal distribution and reduce clock skew.

- **Routing:** Connects components based on placement, optimizing wire paths to ensure signal integrity, minimize congestion, and meet design rules.

- **Sign-off:** Final verification stage, ensuring the design meets functionality, performance, power, and reliability targets. Timing analysis is performed to check setup and hold times, power analysis ensures the design doesn’t exceed power limits, and physical verification checks ensure that the layout meets manufacturing rules. This stage confirms the design is ready for fabrication.

- **GDSII File Generation:** Creates the GDSII file containing the complete layout details needed for chip fabrication. This file represents the final physical design and is used by manufacturers to create the photomasks required for chip production. The GDSII file serves as the blueprint for the actual fabrication of the chip.

**OpenLane ASIC Flow:**

![image](https://github.com/user-attachments/assets/cdd04b14-fbfe-44a3-8d4e-8fbfe443bd74)

1. RTL Synthesis, Technology Mapping, and Formal Verification: The tools used are Yosys (for RTL synthesis), ABC (for technology mapping and formal verification).
2. Static Timing Analysis: The tools used are OpenSTA (for static timing analysis).
3. Floor Planning: The tools used are init_fp (initial floorplanning), ioPlacer (I/O placement), pdn (power distribution network planning), tapcell (tap cell insertion).
4. Placement: The tools used are RePLace (global placement), Resizer (optional for resizing cells), OpenPhySyn (formerly used for placement), OpenDP (detailed placement).
5. Clock Tree Synthesis: The tools used are TritonCTS (for clock tree synthesis).
6. Fill Insertion: The tools used are OpenDP (for filler placement).
7. Routing: The tools used for global routing are FastRoute or CU-GR (formerly used) and for the detailed routing , we use TritonRoute (for detailed routing) or DR-CU (formerly used).
8. SPEF Extraction: The tools used are OpenRCX (or SPEF-Extractor, formerly used) for Standard Parasitic Exchange Format (SPEF) extraction.
9. GDSII Streaming Out: The tools used are Magic and KLayout (for viewing and editing GDSII files).
10. Design Rule Checking (DRC) Checks: The tools used are Magic and KLayout (for DRC checks).
11. Layout vs. Schematic (LVS) Check: The tools used are Netgen (for LVS checks).
12. Antenna Checks: The tools used are Magic (for antenna checks).

**OpenLANE Directory structure**

``` 
├── OOpenLane             -> directory where the tool can be invoked (run docker first)
│   ├── designs          -> All designs must be extracted from this folder
│   │   │   ├── picorv32a -> Design used as case study for this workshop
│   |   |   ├── ...
|   |   ├── ...
├── pdks                 -> contains pdk related files 
│   ├── skywater-pdk     -> all Skywater 130nm PDKs
│   ├── open-pdks        -> contains scripts that makes the commerical PDK (which is normally just compatible to commercial tools) to also be compatible with the open-source EDA tool
│   ├── sky130A          -> pdk variant made especially compatible for open-source tools
│   │   │  ├── libs.ref  -> files specific to node process (timing lib, cell lef, tech lef) for example is `sky130_fd_sc_hd` (Sky130nm Foundry Standard Cell High Density)  
│   │   │  ├── libs.tech -> files specific for the tool (klayout,netgen,magic...) 
```

**Synthesis in Openlane:**

Go to VSD Virtual Box and run the following commands:

```
cd Desktop/work/tools/openlane_working_dir/openlane
docker
./flow.tcl -interactive
package require openlane 0.9
prep -design picorv32a
run_synthesis

```

![1 1](https://github.com/user-attachments/assets/5e8f58ee-4596-4520-a5de-5ee9a381e8e0)

![1 2](https://github.com/user-attachments/assets/bc74f88e-f1c7-4797-b93d-e90e29aa5e5d)

```
exit
exit
```

To view the netlist:

```
cd designs/picorv32a/runs/12-11_12-32/results/synthesis/
gedit picorv32a.synthesis.v
```



Netlist code:

![1 3](https://github.com/user-attachments/assets/157e0bc3-19bf-44a7-9abc-53e924dfc4fd)


To view the yosys report:

```
cd ../..
cd reports/synthesis
gedit 1-yosys_4.stat.rpt
```

![image](https://github.com/user-attachments/assets/5709959c-4250-4fb7-8a16-ded20261f1c4)



Report:

```
28. Printing statistics.

=== picorv32a ===

   Number of wires:              14596
   Number of wire bits:          14978
   Number of public wires:        1565
   Number of public wire bits:    1947
   Number of memories:               0
   Number of memory bits:            0
   Number of processes:              0
   Number of cells:              14876
     sky130_fd_sc_hd__a2111o_2       1
     sky130_fd_sc_hd__a211o_2       35
     sky130_fd_sc_hd__a211oi_2      60
     sky130_fd_sc_hd__a21bo_2      149
     sky130_fd_sc_hd__a21boi_2       8
     sky130_fd_sc_hd__a21o_2        57
     sky130_fd_sc_hd__a21oi_2      244
     sky130_fd_sc_hd__a221o_2       86
     sky130_fd_sc_hd__a22o_2      1013
     sky130_fd_sc_hd__a2bb2o_2    1748
     sky130_fd_sc_hd__a2bb2oi_2     81
     sky130_fd_sc_hd__a311o_2        2
     sky130_fd_sc_hd__a31o_2        49
     sky130_fd_sc_hd__a31oi_2        7
     sky130_fd_sc_hd__a32o_2        46
     sky130_fd_sc_hd__a41o_2         1
     sky130_fd_sc_hd__and2_2       157
     sky130_fd_sc_hd__and3_2        58
     sky130_fd_sc_hd__and4_2       345
     sky130_fd_sc_hd__and4b_2        1
     sky130_fd_sc_hd__buf_1       1656
     sky130_fd_sc_hd__buf_2          8
     sky130_fd_sc_hd__conb_1        42
     sky130_fd_sc_hd__dfxtp_2     1613
     sky130_fd_sc_hd__inv_2       1615
     sky130_fd_sc_hd__mux2_1      1224
     sky130_fd_sc_hd__mux2_2         2
     sky130_fd_sc_hd__mux4_1       221
     sky130_fd_sc_hd__nand2_2       78
     sky130_fd_sc_hd__nor2_2       524
     sky130_fd_sc_hd__nor2b_2        1
     sky130_fd_sc_hd__nor3_2        42
     sky130_fd_sc_hd__nor4_2         1
     sky130_fd_sc_hd__o2111a_2       2
     sky130_fd_sc_hd__o211a_2       69
     sky130_fd_sc_hd__o211ai_2       6
     sky130_fd_sc_hd__o21a_2        54
     sky130_fd_sc_hd__o21ai_2      141
     sky130_fd_sc_hd__o21ba_2      209
     sky130_fd_sc_hd__o21bai_2       1
     sky130_fd_sc_hd__o221a_2      204
     sky130_fd_sc_hd__o221ai_2       7
     sky130_fd_sc_hd__o22a_2      1312
     sky130_fd_sc_hd__o22ai_2       59
     sky130_fd_sc_hd__o2bb2a_2     119
     sky130_fd_sc_hd__o2bb2ai_2     92
     sky130_fd_sc_hd__o311a_2        8
     sky130_fd_sc_hd__o31a_2        19
     sky130_fd_sc_hd__o31ai_2        1
     sky130_fd_sc_hd__o32a_2       109
     sky130_fd_sc_hd__o41a_2         2
     sky130_fd_sc_hd__or2_2       1088
     sky130_fd_sc_hd__or2b_2        25
     sky130_fd_sc_hd__or3_2         68
     sky130_fd_sc_hd__or3b_2         5
     sky130_fd_sc_hd__or4_2         93
     sky130_fd_sc_hd__or4b_2         6
     sky130_fd_sc_hd__or4bb_2        2

   Chip area for module '\picorv32a': 147712.918400
```

```
Flop ratio       =   Number of D Flip flops     =     1613      =      0.1084
	             ______________________           _____
	             Total Number of cells            14876
```

</details>





<details>
       <summary>DAY 2 :  Good floorplan vs bad floorplan and introduction to library cells </summary>

## AIM : Good floorplan vs bad floorplan and introduction to library cells

**Utilization Factor and Aspect Ratio**: In IC floor planning, utilization factor and aspect ratio are key parameters. The utilization factor is the ratio of the area occupied by the netlist to the total core area. While a perfect utilization of 1 (100%) is ideal, practical designs target a factor of 0.5 to 0.6 to allow space for buffer zones, routing channels, and future adjustments. The aspect ratio, defined as height divided by width, indicates the chip’s shape; an aspect ratio of 1 denotes a square, while other values result in a rectangular layout. The aspect ratio is chosen based on functional, packaging, and manufacturing needs.

```
Utilisation Factor =  Area occupied by netlist
                     __________________________
                         Total area of core
                         
Aspect Ratio =  Height
               ________
                Width
```

**Pre-placed cells** : Pre-placed cells are essential functional blocks, such as memory, custom processors, and analog circuits, positioned manually in fixed locations. These blocks are crucial for the chip’s performance and remain fixed during placement and routing to preserve their functionality and layout integrity.

**Decoupling Capacitors** : Decoupling capacitors are placed near logic circuits to stabilize power supply voltages during transient events. Acting as local energy reserves, they help reduce voltage fluctuations, crosstalk, and electromagnetic interference (EMI), ensuring reliable power delivery to sensitive circuits.

**Power Planning**: A robust power planning strategy includes creating a power and ground mesh to distribute VDD and VSS evenly across the chip. This setup ensures stable power delivery, minimizes voltage drops, and improves overall efficiency. Multiple power and ground points reduce the risk of instability and voltage drop issues, supporting the design’s power needs effectively.

**Pin Placement**: Pin placement (I/O planning) is crucial for functionality and reliability. Strategic pin assignment minimizes signal degradation, preserves data integrity, and helps manage heat dissipation. Proper positioning of power and ground pins supports thermal management and enhances signal strength, contributing to overall system stability and manufacturability.

Floorplaning using OpenLANE:

Run the following commands:

```
cd Desktop/work/tools/openlane_working_dir/openlane
docker
```

```
./flow.tcl -interactive
package require openlane 0.9
prep -design picorv32a
run_synthesis
run_floorplan
```

![image](https://github.com/user-attachments/assets/dff37f6a-0039-4309-9307-09008c550c15)


![image](https://github.com/user-attachments/assets/153617a3-455d-49f0-b12a-f97930ada98a)


Now, run the below commands in a new terminal:

```
cd designs/picorv32a/runs/12-11_13-40/results/floorplan
gedit picorv32a.floorplan.def
```
![image](https://github.com/user-attachments/assets/2702908e-8728-4ad6-b1c2-219c7c1b2fd2)


According to floorplan definition:

1000 Unit Distance = 1 Micron  

Die width in unit distance = 660685−0 = 660685 

Die height in unit distance = 671405−0 = 671405  

Distance in microns = Value in Unit Distance/1000  

​Die width in microns = 660685/1000 = 660.685 Microns  

Die height in microns = 671405/1000 = 671.405 Microns  

Area of die in microns = 660.685 × 671.405 = 443587.212425 Square Microns



To view the floorplan in magic. Open a new terminal/tab and run the below commands:

```
cd designs/picorv32a/runs/12-11_13-40/results/floorplan
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```

![image](https://github.com/user-attachments/assets/9feef09d-993b-4ca0-a639-5420cccd7e86)


Decap and Tap Cells:

![image](https://github.com/user-attachments/assets/639c7990-086e-455f-8813-f9e28e1a70ce)


Unplaces standard cells at origin:

![image](https://github.com/user-attachments/assets/f801854d-6362-4d7d-bfe1-d2bb98de0bdd)

Diagonally equidistant Tap cells

![image](https://github.com/user-attachments/assets/93b925c6-f3d1-487b-a59e-cb895590b648)


Command to run placement:

```
run_placement
```

![image](https://github.com/user-attachments/assets/ef2386f5-0042-4802-ab5d-aee8b014ebd1)


To view the placement in magic:

```
cd designs/picorv32a/runs/12-11_13-40/results/placement/
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &
```

![image](https://github.com/user-attachments/assets/c07df0f2-48b6-4ee6-a958-d54611c84a51)


![image](https://github.com/user-attachments/assets/241f8ba6-25f0-436b-bbae-d4e02496a84a)


**Cell design and Characterization Flow**

Library is a place where we get information about every cell. It has differents cells with different size, functionality,threshold voltages. There is a typical cell design flow steps.

Inputs : PDKS(process design kit) : DRC & LVS, SPICE Models, library & user-defined specs.
Design Steps :Circuit design, Layout design (Art of layout Euler's path and stick diagram), Extraction of parasitics, Characterization (timing, noise, power).
Outputs: CDL (circuit description language), LEF, GDSII, extracted SPICE netlist (.cir), timing, noise and power .lib files

**Standard Cell Characterization Flow**

A typical standard cell characterization flow that is followed in the industry includes the following steps:

- Read in the models and tech files
- Read extracted spice Netlist
- Recognise behavior of the cells
- Read the subcircuits
- Attach power sources
- Apply stimulus to characterization setup
- Provide neccesary output capacitance loads
- Provide neccesary simulation commands
- Now all these 8 steps are fed in together as a configuration file to a characterization software called GUNA. This software generates timing, noise, power models. These .libs are classified as Timing characterization, power characterization and noise characterization.

**Timing parameters**

| Timing definition | Value |
|---|---|
| slew_low_rise_thr | 20% value |
| slew_high_rise_thr | 80% value |
| slew_low_fall_thr | 20% value |
| slew_high_fall_thr | 80% value |
| in_rise_thr | 50% value |
| in_fall_thr | 50% value |
| out_rise_thr | 50% value |
| out_fall_thr | 50% value |

**Propagation Delay**: It refers to the time it takes for a change in an input signal to reach 50% of its final value to produce a corresponding change in the output signal to reach 50% of its final value of a digital circuit.

```
rise delay =  time(out_fall_thr) - time(in_rise_thr)
```

**Transistion time**: The time it takes the signal to move between states is the transition time , where the time is measured between 10% and 90% or 20% to 80% of the signal levels.

```
Fall transition time: time(slew_high_fall_thr) - time(slew_low_fall_thr)
Rise transition time: time(slew_high_rise_thr) - time(slew_low_rise_thr)
```

</details>






<details>
       <summary>DAY 3 : Design library cell using Magic Layout and ngspice characterization </summary>


## AIM : Design library cell using Magic Layout and ngspice characterization

**CMOS inverter ngspice simulations**

Creating a SPICE Deck for a CMOS Inverter Simulation

- Netlist Creation: Define the component connections (netlist) for a CMOS inverter circuit. Ensure each node is labeled appropriately for easy identification in the SPICE simulation. Typical nodes include input, output, ground, and supply nodes.
- Device Sizing: Specify the Width-to-Length (W/L) ratios for both the PMOS and NMOS transistors.For proper operation, the PMOS width should be larger than the NMOS width, usually 2x to 3x, to balance the drive strength
- Voltage Levels: Set gate and supply voltages, often in multiples of the transistor length. 
- Node Naming: Assign node names to each connection point around the components to clearly identify each element in the SPICE netlist (e.g., VDD, GND, IN, OUT). This helps SPICE recognize each component and simulate the circuit effectively.

![image](https://github.com/user-attachments/assets/b61efcf4-cd1f-4080-b4dc-4606afc3a2e5)


```
***syntax for PMOS and NMOS desription***
[component name] [drain] [gate] [source] [substrate] [transistor type] W=[width] L=[length]
 ***simulation commands***
.op --- is the start of SPICE simulation operation where Vin sweeps from 0 to 2.5 with 0.5 steps
tsmc_025um_model.mod  ----  model file which contains the technological parameters for the 0.25um NMOS and PMOS 
```
Commands to simulate in SPICE:

```
source [filename].cir
run
setplot 
dc1 
plot out vs in 
```

![image](https://github.com/user-attachments/assets/49f1ed28-c601-4954-a3aa-077a2c650650)

The switching threshold Vm is like a critical voltage level for a component called a CMOS inverter. It's the point at which this inverter switches between sending out a "0" or a "1" in a computer chip. This the point where both PMOS and NMOS is in saturation or kind of turned on, and leakage current is high. If PMOS is thicker than NMOS, the CMOS will have higher switching threshold (1.2V vs 1V) while threshold will be lower when NMOS becomes thicker.

At this point, both the transistors are in saturation region, means both are turned on and have high chances of current flowing directly from VDD to Ground called Leakage current.

To find the switching threshold

```
Vin in 0 2.5
*** Simulation Command ***
.op
.dc Vin 0 2.5 0.05
```
![image](https://github.com/user-attachments/assets/61d07ded-adf6-4b6d-8e79-936512557edd)

Transient analysis is used for finding propagation delay. SPICE transient analysis uses pulse input shown below:

![image](https://github.com/user-attachments/assets/af0c7120-e946-4c8f-95c2-c66b130ef415)

The simulation commands:

```
Vin in 0 0 pulse 0 2.5 0 10p 10p 1n 2n 
*** Simulation Command ***
.op
.tran 10p 4n
```

Result of SPICE simulation for transient analysis:

![image](https://github.com/user-attachments/assets/16ca9925-420a-4417-b3fe-21e909750dff)



Now, we clone the custom inverter

```
cd Desktop/work/tools/openlane_working_dir/openlane
git clone https://github.com/nickson-jose/vsdstdcelldesign
cd vsdstdcelldesign
cp /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech .
ls
magic -T sky130A.tech sky130_CHA_inv.mag &
```

![image](https://github.com/user-attachments/assets/93132797-2daa-4c92-85dd-b7290dbad7a7)




![image](https://github.com/user-attachments/assets/c7a53688-ad82-48f2-8379-559d6e1a52cd)




**Inception of Layout CMOS fabrication process**

The 16-mask CMOS design fabrication process:

1. Substrate Preparation: The process begins with preparing a silicon wafer as the foundational substrate for the circuit.
2. N-Well Formation: The N-well regions are created on the substrate by introducing impurities, typically phosphorus, through ion implantation or diffusion
3. P-Well Formation: Similar to the N-well formation, P-well regions are created using ion implantation or diffusion with boron or other suitable dopants.
4. Gate Oxide Deposition: A thin silicon dioxide layer is deposited to form the gate oxide, which insulates the gate from the channel.
5. Poly-Silicon Deposition: A layer of polysilicon is deposited on the gate oxide to serve as the gate electrode.
6. Poly-Silicon Masking and Etching: A photoresist mask defines areas where polysilicon should remain, and etching removes exposed portions.
7. N-Well Masking and Implantation: A photoresist mask is used to define the areas where the N-well regions should be preserved. Phosphorus or other suitable impurities are then implanted into the exposed regions.
8. P-Well Masking and Implantation: Similarly, a photoresist mask is used to define the areas where the P-well regions should be preserved. Boron or other suitable impurities are implanted into the exposed regions.
9. Source/Drain Implantation: Using photoresist masks, dopants are implanted to create source and drain regions (e.g., arsenic for NMOS, boron for PMOS).
10. Gate Formation: The gate electrode is defined by etching the poly-silicon layer using a photoresist mask.
11. Source/Drain Masking and Etching: A photoresist mask is applied to define the source and drain regions followed by etching to remove the oxide layer in those areas.
12. Contact/Via Formation: Contact holes or vias are etched through the oxide layer to expose the underlying regions, such as the source/drain regions or poly-silicon gates.
13. Metal Deposition: A layer of metal, typically aluminum or copper, is deposited on the wafer surface to form the interconnects.
14. Metal Masking and Etching: A photoresist mask is used to define the metal interconnects, and etching is performed to remove the exposed metal, leaving behind the desired interconnect patterns.
15. Passivation Layer Deposition: A protective layer, often made of silicon dioxide or nitride, is deposited to isolate and shield the metal interconnects.
16. Final Testing and Packaging: The fabricated wafer undergoes rigorous testing to ensure the functionality of the integrated circuits. The working chips are then separated, packaged, and prepared for use in various electronic devices.

![image](https://github.com/user-attachments/assets/d24e7009-a71a-437f-94c8-8233c633f775)

Inverter layout:

Identify NMOS:

![image](https://github.com/user-attachments/assets/2bfefe78-f597-46c2-aa8b-0253b476b75a)



Identify PMOS:

![image](https://github.com/user-attachments/assets/caab3a52-b6fe-4a11-b9e6-e254d33f5b78)



Output Y:

![image](https://github.com/user-attachments/assets/832da4ee-5af8-4081-9b32-676dd59bf97c)



PMOS source connected to Vpwr:

![image](https://github.com/user-attachments/assets/6347465a-b591-41b0-81d4-505415e59b5e)



NMOS source connected to Ground:

![image](https://github.com/user-attachments/assets/8c436070-1f63-49cf-97da-9610d4e0f343)



Spice extraction of inverter in Magic. Run these in the tkcon window:

```
# Check current directory
pwd
extract all
ext2spice cthresh 0 rthresh 0
ext2spice
```

![image](https://github.com/user-attachments/assets/54215727-ef69-4557-8da0-be12c78ac0b7)



To view the spice file:
```
ls -ltr
gedit sky130_CHA_inv.spice
```
![image](https://github.com/user-attachments/assets/39d36119-5aea-4d86-8bfc-cc3c0c02455e)


![image](https://github.com/user-attachments/assets/1f3021c9-9dce-4207-b273-67fccf915944)




The contents of spice file:

```
* SPICE3 file created from sky130_inv.ext - technology: sky130A
.option scale=10n
.subckt sky130_CHA_inv A Y VPWR VGND
X0 Y A VGND VGND sky130_fd_pr__nfet_01v8 ad=1.37n pd=0.148m as=1.37n ps=0.148m w=35 l=23
X1 Y A VPWR VPWR sky130_fd_pr__pfet_01v8 ad=1.44n pd=0.152m as=1.52n ps=0.156m w=37 l=23
C0 VPWR Y 0.11fF
C1 A Y 0.754fF
C2 A VPWR 0.277fF
C3 Y VGND 0.279fF
C4 A VGND 0.45fF
C5 VPWR VGND 0.781fF
.ends
```

Now modify the `sky130_CHA_inv.spice` file to find the transient respone:

```
* SPICE3 file created from sky130_CHA_inv.ext - technology: sky130A
.option scale=0.01u
.include ./libs/pshort.lib
.include ./libs/nshort.lib
//.subckt sky130_inv A Y VPWR VGND
M1000 Y A VGND VGND nshort_model.0 w=35 l=23
+  ad=1.44n pd=0.152m as=1.37n ps=0.148m
M1001 Y A VPWR VPWR pshort_model.0 w=37 l=23
+  ad=1.44n pd=0.152m as=1.52n ps=0.156m
VDD VPWR 0 3.3V
VSS VGND 0 0V
Va A VGND PULSE(0V 3.3V 0 0.1ns 0.1ns 2ns 4ns)
C0 A VPWR 0.0774f
C1 VPWR Y 0.117f
C2 A Y 0.0754f
C3 Y VGND 2f
C4 A VGND 0.45f
C5 VPWR VGND 0.781f
//.ends
.tran 1n 20n
.control
run
.endc
.end
```

![image](https://github.com/user-attachments/assets/6809a9c8-d819-45f4-a5b8-eb5dcf73c622)



Now, simulate the spice netlist
```
ngspice sky130_CHA_inv.spice
```

![image](https://github.com/user-attachments/assets/4a965ab4-08e2-4c33-83da-61e90e552d09)



To plot the waveform:

```
plot y vs time a
```



![image](https://github.com/user-attachments/assets/9e178e70-8616-42f2-b7de-0572ef7bf805)

![image](https://github.com/user-attachments/assets/6bd1e378-c9c6-42f9-90af-f00596154630)



Using this transient response, we will now characterize the cell's slew rate and propagation delay:

Rise Transition: Time taken for the output to rise from 20% to 80% of max value
Fall Transition: Time taken for the output to fall from 80% to 20% of max value
Cell Rise delay: difference in time(50% output rise) to time(50% input fall)
Cell Fall delay: difference in time(50% output fall) to time(50% input rise)


20 % Rise Screenshot
![image](https://github.com/user-attachments/assets/79833d37-07f0-4ad4-812d-2cb4d6305d57)



80 % Rise  Screenshot

![image](https://github.com/user-attachments/assets/b79646c7-b7a7-4f9e-b7cf-addf4b1399bb)



```
Rise Transition Time = 2.23969 - 2.17993 = 0.05976 ns = 59.76 ps
```
80% fall ScreenShot

![image](https://github.com/user-attachments/assets/854732a4-b239-4852-8b91-b9e6e0b279cb)

20% fall ScreenShot

![image](https://github.com/user-attachments/assets/5245f53c-eb1c-4ba7-99f4-2f702989d363)


```
Fall Transition Time = 4.09396 - 4.05069 = 0.04327 ns = 43.27 ps
```
Rise Cell Delay : Time taken by output to rise to 50% − Time taken by input to fall to 50%
50 % of 3.3V = 1.65V

50% Screenshots

![image](https://github.com/user-attachments/assets/3b938c5e-8525-4d4a-b64c-2409637ae090)


```
Rise cell delay = 2.20711 - 2.15 = 0.05711 ns = 57.11 ps
```
Fall Cell Delay : Time taken by output to fall to 50% − Time taken by input to rise to 50%
50 % of 3.3V = 1.65V

50% Screenshots
![image](https://github.com/user-attachments/assets/f42e0ed1-d9e8-4544-9a46-b7393e930131)




```
Fall cell delay = 4.0756 - 4.0498 = 0.0258 ns = 25.8 ps
```


Magic Tool options and DRC Rules:


Now, go to home directory and run the below commands:

```
cd
wget http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz
tar xfz drc_tests.tgz
cd drc_tests
ls -al
gvim .magicrc
magic -d XR &
```

![image](https://github.com/user-attachments/assets/44478c52-ecef-4ae1-ad9a-ec171260bb0d)

![image](https://github.com/user-attachments/assets/f297e7c9-332c-4228-bf3f-60e092996719)


First load the poly file by load poly.mag on tkcon window.

![image](https://github.com/user-attachments/assets/526124f5-b92c-4cdd-a122-1dfa56b42a61)

We can see that Poly.9 is incorrect.

Screenshot of poly rules

![image](https://github.com/user-attachments/assets/a8260270-a35d-4104-9929-3a057b81d19c)

Add the below commands in the sky130A.tech

![image](https://github.com/user-attachments/assets/eda07ffc-6d4c-438d-9e49-31deb982140d)


![image](https://github.com/user-attachments/assets/8e7d7af0-89c4-484d-b3fb-63d4a3628475)


Run the commands in tkcon window:

```
tech load sky130A.tech
drc check
drc why
```

![image](https://github.com/user-attachments/assets/29f72049-28e6-4d87-ac46-29e9bbe97241)

</details>











<details>
       <summary>DAY 4 : Pre-layout timing analysis and importance of good clock tree </summary>


## AIM : Pre-layout timing analysis and importance of good clock tree

Commands to extract `tracks.info` file:

```
cd Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign
cd ../../pdks/sky130A/libs.tech/openlane/sky130_fd_sc_hd/
less tracks.info
```
![image](https://github.com/user-attachments/assets/cef5e058-bbe3-4d1b-b1d5-cbaf47d04d59)

Commands to open the custom inverter layout
```

cd Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign
magic -T sky130A.tech sky130_inv.mag &
```

Commands for tkcon window to set grid as tracks of locali layer

```
help grid
grid 0.46um 0.34um 0.23um 0.17um
```

![image](https://github.com/user-attachments/assets/879860f3-b355-4209-a1e8-ffc0d4a01715)


The grids show where the routing for the local-interconnet layer can only happen, the distance of the grid lines are the required pitch of the wire. Below, we can see that the guidelines are satisfied:

![image](https://github.com/user-attachments/assets/c3b753ec-85e4-413e-9d22-f6a8ebc584d4)


Now, save it by giving a custon name

```
save sky130_CHA_inv.mag
```

![image](https://github.com/user-attachments/assets/a3044280-447f-4a9f-ac66-b4ba18e16c1c)


Now, open it by using the following commands:

```
magic -T sky130A.tech sky130_CHA_inv.mag &
```

![image](https://github.com/user-attachments/assets/550232de-86c5-407b-aa0f-1aa077d75850)


Now, type the following command in tkcon window:

```
lef write
```
![image](https://github.com/user-attachments/assets/5ba7c908-f8f4-4707-a4fa-e8d34df2ea09)


![image](https://github.com/user-attachments/assets/345cc568-6055-46fe-8c29-e4dbd0985246)

![image](https://github.com/user-attachments/assets/a6f008af-4840-4b3c-8463-4001781c3f6f)

Modify config.tcl:

```
# Design
set ::env(DESIGN_NAME) "picorv32a"
set ::env(VERILOG_FILES) "./designs/picorv32a/src/picorv32a.v"
set ::env(SDC_FILES) "./designs/picorv32a/src/picorv32a.sdc"
set ::env(CLOCK_PERIOD) "5.000"
set ::env(CLOCK_PORT) "clk"
set ::env(CLOCK_NET) $::env(CLOCK_PORT) 
set ::env(LIB_SYNTH) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__typical.lib "
set ::env(LIB_FASTEST) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__fast.lib"
set ::env(LIB_SLOWEST) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__slow.lib "
set ::env(LIB_TYPICAL) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__typical.lib"
set ::env(EXTRA_LEFS) [glob $::env(OPENLANE_ROOT)/designs/$::env(DESIGN_NAME)/src/*.lef]   ## this is the new line added to the existing config.tcl file
set filename $::env(OPENLANE_ROOT)/designs/$::env(DESIGN_NAME)/$::env(PDK)_$::env(STD_CELL_LIBRARY)_config.tcl
if { [file exists $filename] == 1 } {
  source $filename
}
```
![image](https://github.com/user-attachments/assets/1da44ab2-acb4-47e7-976e-6ef2e6bd5aab)

Now, run openlane flow synthesis:

```
cd Desktop/work/tools/openlane_working_dir/openlane
docker
```

```
./flow.tcl -interactive
package require openlane 0.9
prep -design picorv32a
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs
run_synthesis
```

![image](https://github.com/user-attachments/assets/9170d63d-fe84-4e25-a1bd-df41cd9af1aa)


![image](https://github.com/user-attachments/assets/a93a8b24-8b2d-46e6-8d07-e40c5492d949)



![image](https://github.com/user-attachments/assets/18df35a5-7c4f-4f36-b1e8-03e75893e739)


**Delay Tables**

Delay plays a crucial role in cell timing, impacted by input transition and output load. Cells of the same type can have different delays depending on wire length due to resistance and capacitance variations. To manage this, "delay tables" are created, using 2D arrays with input slew and load capacitance for each buffer size as timing models. Algorithms compute buffer delays from these tables, interpolating where exact data isn’t available to estimate delays accurately, preserving signal integrity across varying load conditions.

![image](https://github.com/user-attachments/assets/095a59e1-158c-4870-88e3-b73cb3a3692c)

Fixing slack:

```
./flow.tcl -interactive
package require openlane 0.9
prep -design picorv32a -tag 24-03_10-03 -overwrite
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs
echo $::env(SYNTH_STRATEGY)
set ::env(SYNTH_STRATEGY) "DELAY 3"
echo $::env(SYNTH_BUFFERING
echo $::env(SYNTH_SIZING)
set ::env(SYNTH_SIZING) 1
echo $::env(SYNTH_DRIVING_CELL)
run_synthesis
```
![image](https://github.com/user-attachments/assets/fda6e1ec-a9fd-49bc-9818-416a14f53834)

![image](https://github.com/user-attachments/assets/523691b9-3219-4c19-9835-00d796be9b73)

![image](https://github.com/user-attachments/assets/2a2e5394-6fb9-4e4d-a799-82d1a34e4d89)

![image](https://github.com/user-attachments/assets/5487ee4d-27ee-4159-bfbf-584f794a6376)





Now, run floorplan

```
run_floorplan
```

![image](https://github.com/user-attachments/assets/4a06019a-8c4b-4866-ad6c-47b6f3f7aebc)


![image](https://github.com/user-attachments/assets/44eebd5e-be74-4cbc-9a92-de0c45e31c3e)

Since we are facing unexpected un-explainable error while using run_floorplan command, we can instead use the following set of commands available based on information from `Desktop/work/tools/openlane_working_dir/openlane/scripts/tcl_commands/floorplan.tcl` and also based on Floorplan Commands section in `Desktop/work/tools/openlane_working_dir/openlane/docs/source/OpenLANE_commands.md`

```
init_floorplan
place_io
tap_decap_or
```

Now, do placement

```
run_placement
```

![image](https://github.com/user-attachments/assets/978e67f5-9b5e-4cc2-b76d-9b5074806d50)


![image](https://github.com/user-attachments/assets/6136d8c2-9e17-4c34-8905-c090eddd89ed)


Now, open a new terminal and run the below commands to load placement def in magic

```
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/12-11_13-40/results/placement/
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &
```

![image](https://github.com/user-attachments/assets/908be0e4-0e37-448e-be80-abf188cb25ff)

Custom inverter inserted in placement def

![image](https://github.com/user-attachments/assets/c17f911c-440a-4b22-988d-88144d83d4ad)


Now, select the cell and type expand in tkcon window to view internal layers of cells (your custom inverter)

![image](https://github.com/user-attachments/assets/eadcc7a2-19f0-4c0f-a396-9a415e64085d)

![image](https://github.com/user-attachments/assets/2197d436-8069-4bd5-acd9-42be400def16)


**Timing analysis with ideal clocks using openSTA**

Pre-layout STA will include effects of clock buffers and net-delay due to RC parasitics (wire delay will be derived from PDK library wire model).

![image](https://github.com/user-attachments/assets/a74af227-70dd-4812-930d-b6e9e787a27f)

Since we are getting 0 wns after improved timing run, we will be doing the timing analysis on initial run of synthesis which has lots of violations and no parameters added to improve timing.

Commands to invoke the OpenLANE flow include new lef and perform synthesis:

```
cd Desktop/work/tools/openlane_working_dir/openlane
docker
./flow.tcl -interactive
package require openlane 0.9set
prep -design picorv32a
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs
set ::env(SYNTH_SIZING) 1
run_synthesis
```

Go, to `Desktop/work/tools/openlane_working_dir/openlane` and create a file `pre_sta.conf`. The contents of the file are:

```
set_cmd_units -time ns -capacitance pF -current mA -voltage V -resistance kOhm -distance um
read_liberty -max /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/sky130_fd_sc_hd__slow.lib
read_liberty -min /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/sky130_fd_sc_hd__fast.lib
read_verilog /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/12-11_13-40/results/synthesis/picorv32a.synthesis.v
link_design picorv32a
read_sdc /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/my_base.sdc
report_checks -path_delay min_max -fields {slew trans net cap input_pin}
report_tns
report_wns
```

Contents of `my_base.sdc`:

```
set ::env(CLOCK_PORT) clk
set ::env(CLOCK_PERIOD) 12.000
set ::env(SYNTH_DRIVING_CELL) sky130_fd_sc_hd__inv_8
set ::env(SYNTH_DRIVING_CELL_PIN) Y
set ::env(SYNTH_CAP_LOAD) 17.65
create_clock [get_ports $::env(CLOCK_PORT)]  -name $::env(CLOCK_PORT)  -period $::env(CLOCK_PERIOD)
set IO_PCT  0.2
set input_delay_value [expr $::env(CLOCK_PERIOD) * $IO_PCT]
set output_delay_value [expr $::env(CLOCK_PERIOD) * $IO_PCT]
puts "\[INFO\]: Setting output delay to: $output_delay_value"
puts "\[INFO\]: Setting input delay to: $input_delay_value"
set clk_indx [lsearch [all_inputs] [get_port $::env(CLOCK_PORT)]]
#set rst_indx [lsearch [all_inputs] [get_port resetn]]
set all_inputs_wo_clk [lreplace [all_inputs] $clk_indx $clk_indx]
#set all_inputs_wo_clk_rst [lreplace $all_inputs_wo_clk $rst_indx $rst_indx]
set all_inputs_wo_clk_rst $all_inputs_wo_clk
# correct resetn
set_input_delay $input_delay_value  -clock [get_clocks $::env(CLOCK_PORT)] $all_inputs_wo_clk_rst
#set_input_delay 0.0 -clock [get_clocks $::env(CLOCK_PORT)] {resetn}
set_output_delay $output_delay_value  -clock [get_clocks $::env(CLOCK_PORT)] [all_outputs]
# TODO set this as parameter
set_driving_cell -lib_cell $::env(SYNTH_DRIVING_CELL) -pin $::env(SYNTH_DRIVING_CELL_PIN) [all_inputs]
set cap_load [expr $::env(SYNTH_CAP_LOAD) / 1000.0]
puts "\[INFO\]: Setting load to: $cap_load"
set_load  $cap_load [all_outputs]
```

Commands to run STA:

```
cd Desktop/work/tools/openlane_working_dir/openlane
sta pre_sta.conf
```

![image](https://github.com/user-attachments/assets/ab908256-ab8f-444d-9121-baf2ded209be)


![image](https://github.com/user-attachments/assets/33940dd4-5a07-47d5-92e4-aab309c2e9ac)




Clock Tree Synthesis (CTS) techniques vary based on design needs:

- Balanced Tree CTS: Uses a balanced binary-like tree for equal path lengths, minimizing clock skew but with moderate power efficiency.
- H-tree CTS: Employs an "H"-shaped structure, good for large areas and power efficiency.

   ![image](https://github.com/user-attachments/assets/d1b13f19-a87f-41b6-8f29-a4e00a8e7216)

- Star CTS: Distributes the clock from a central point, minimizing skew but requiring more buffers near the source.
- Global-Local CTS: Combines star and tree topologies, with a global tree for clock domains and local trees within domains, balancing global and local timing.
- Mesh CTS: Uses a grid pattern ideal for structured designs, balancing simplicity and skew.
- Adaptive CTS: Dynamically adjusts based on timing and congestion, offering flexibility but with added complexity.

**Crosstalk**

Crosstalk is interference from overlapping electromagnetic fields between adjacent circuits, causing unwanted signals. In VLSI, it can lead to data corruption, timing issues, and higher power consumption. Mitigation strategies include optimized layout and routing, shielding, and clock gating to reduce dynamic power and minimize crosstalk effects.

![image](https://github.com/user-attachments/assets/21df4ac0-57aa-492e-adfa-7e04ce385680)

**Clock Net Shielding**

Clock net shielding prevents glitches by isolating the clock network, using shields connected to VDD or GND that don’t switch. It reduces interference by isolating clocks from other signals, often with dedicated routing layers and clock buffers. Additionally, clock domain isolation helps prevent cross-domain interference, avoiding metastability and maintaining synchronization.

![image](https://github.com/user-attachments/assets/bf85dd84-dc29-4962-877a-ce4f535bab2c)

Now to insert this updated netlist to PnR flow and we can use write_verilog and overwrite the synthesis netlist but before that we are going to make a copy of the old old netlist:

Run the following commands:

```
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/12-11_13-40/results/synthesis/
ls
cp picorv32a.synthesis.v picorv32a.synthesis_old.v
ls
```

Commands to write verilog:

```
write_verilog /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/12-11_13-40/results/synthesis/picorv32a.synthesis.v
exit
```
Verified that the netlist is overwritten

![image](https://github.com/user-attachments/assets/80767a72-9618-48e8-8d34-b18f6c9a0b1e)





Now, run the following commands:

```
cd Desktop/work/tools/openlane_working_dir/openlane
docker
./flow.tcl -interactive
prep -design picorv32a -tag 12-11_13-40 -overwrite
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs
set ::env(SYNTH_STRATEGY) "DELAY 3"
set ::env(SYNTH_SIZING) 1
run_synthesis
init_floorplan
place_io
tap_decap_or
run_placement
run_cts
```
![image](https://github.com/user-attachments/assets/61fec8bb-4ba8-40b4-a5e7-df3af2b84b7c)


![image](https://github.com/user-attachments/assets/f1521010-6aa6-4eae-9b30-2710c93b854b)


The cts is succesfull as shown below:

![image](https://github.com/user-attachments/assets/d5446bf8-1ff3-4003-b5a1-83aead356fca)


![image](https://github.com/user-attachments/assets/3dc8e3e1-b853-46e9-816d-e71d66e6c4f4)


**Setup timing analysis using real clocks**

A real clock in timing analysis accounts for practical factors like clock skew and clock jitter. Clock skew is the difference in arrival times of the clock signal at different parts of the circuit due to physical delays, which affects setup and hold timing margins. Clock jitter is the variability in the clock period caused by power, temperature, and noise fluctuations, leading to uncertainty in clock edge timing. Both factors are crucial for accurate timing analysis, ensuring the design performs reliably in real-world conditions.

![image](https://github.com/user-attachments/assets/3526c927-e1a9-445a-9dae-22bc7e0446c7)

![image](https://github.com/user-attachments/assets/0c766405-5f9b-4700-a4cd-6fd19e9ea6cc)

Now, enter the following commands for Post-CTS OpenROAD timing analysis:

```
openroad
read_lef /openLANE_flow/designs/picorv32a/runs/12-11_13-40/tmp/merged.lef
read_def /openLANE_flow/designs/picorv32a/runs/12-11_13-40/results/cts/picorv32a.cts.def
write_db pico_cts.db
read_db pico_cts.db
read_verilog /openLANE_flow/designs/picorv32a/runs/12-11_13-40/results/synthesis/picorv32a.synthesis_cts.v
read_liberty $::env(LIB_SYNTH_COMPLETE)
link_design picorv32a
read_sdc /openLANE_flow/designs/picorv32a/src/my_base.sdc
set_propagated_clock [all_clocks]
report_checks -path_delay min_max -fields {slew trans net cap input_pins} -format full_clock_expanded -digits 4
exit
```

![image](https://github.com/user-attachments/assets/abd617e3-654d-4e3e-832c-d338b0568ec1)


![image](https://github.com/user-attachments/assets/b3cd1478-55ba-4c6b-b669-74f26536f253)

![image](https://github.com/user-attachments/assets/a690f083-68eb-4e17-af67-6ba962b260c8)


Now, enter the following commands for exploring post-CTS OpenROAD timing analysis by removing 'sky130_fd_sc_hd__clkbuf_1' cell from clock buffer list variable 'CTS_CLK_BUFFER_LIST':

```
echo $::env(CTS_CLK_BUFFER_LIST)
set ::env(CTS_CLK_BUFFER_LIST) [lreplace $::env(CTS_CLK_BUFFER_LIST) 0 0]
echo $::env(CTS_CLK_BUFFER_LIST)
echo $::env(CURRENT_DEF)
set ::env(CURRENT_DEF) /openLANE_flow/designs/picorv32a/runs/25-03_18-52/results/placement/picorv32a.placement.def
run_cts
echo $::env(CTS_CLK_BUFFER_LIST)
openroad
read_lef /openLANE_flow/designs/picorv32a/runs/25-03_18-52/tmp/merged.lef
read_def /openLANE_flow/designs/picorv32a/runs/25-03_18-52/results/cts/picorv32a.cts.def
write_db pico_cts1.db
read_db pico_cts.db
read_verilog /openLANE_flow/designs/picorv32a/runs/25-03_18-52/results/synthesis/picorv32a.synthesis_cts.v
read_liberty $::env(LIB_SYNTH_COMPLETE)
link_design picorv32a
read_sdc /openLANE_flow/designs/picorv32a/src/my_base.sdc
set_propagated_clock [all_clocks]
report_checks -path_delay min_max -fields {slew transd net cap input_pins} -format full_clock_expanded -digits 4
report_clock_skew -hold
report_clock_skew -setup
exit
echo $::env(CTS_CLK_BUFFER_LIST)
set ::env(CTS_CLK_BUFFER_LIST) [linsert $::env(CTS_CLK_BUFFER_LIST) 0 sky130_fd_sc_hd__clkbuf_1]
echo $::env(CTS_CLK_BUFFER_LIST)
```

![image](https://github.com/user-attachments/assets/f9167d26-747b-4c5d-bcd8-39e8bc353451)


![image](https://github.com/user-attachments/assets/a1f03b56-a87d-4a41-a0ea-1da6d7a76dea)


![image](https://github.com/user-attachments/assets/79404c79-913c-4ac9-9136-c570762b8838)


</details>


<details>
       <summary> DAY 5 : Final steps for RTL2GDS using tritonRoute and openSTA </summary>


### AIM- Final steps for RTL2GDS using tritonRoute and openSTA

**Maze Routing and Lee's algorithm**

Routing establishes a physical connection between pins, and algorithms like Maze Routing (e.g., the Lee algorithm) are used to find efficient paths on a routing grid. The Lee algorithm starts at a source pin, assigning incremental labels to neighboring cells until reaching the target pin, prioritizing L-shaped routes and using zigzag paths if needed. While effective for finding the shortest path between two pins, the Lee algorithm can be slow for large-scale designs, prompting the use of faster alternatives for handling complex routing tasks.

![image](https://github.com/user-attachments/assets/9016ae8d-1a9f-4b22-ba5f-a445af7bc92d)

**Design Rule Check**

Command to generate Power Distribution Network (PDN):

```
# Change directory to openlane flow directory
cd Desktop/work/tools/openlane_working_dir/openlane

# alias docker='docker run -it -v $(pwd):/openLANE_flow -v $PDK_ROOT:$PDK_ROOT -e PDK_ROOT=$PDK_ROOT -u $(id -u $USER):$(id -g $USER) efabless/openlane:v0.21'
# Since we have aliased the long command to 'docker' we can invoke the OpenLANE flow docker sub-system by just running this command
docker
# Now that we have entered the OpenLANE flow contained docker sub-system we can invoke the OpenLANE flow in the Interactive mode using the following command
./flow.tcl -interactive

# Now that OpenLANE flow is open we have to input the required packages for proper functionality of the OpenLANE flow
package require openlane 0.9

# Now the OpenLANE flow is ready to run any design and initially we have to prep the design creating some necessary files and directories for running a specific design which in our case is 'picorv32a'
prep -design picorv32a

# Addiitional commands to include newly added lef to openlane flow merged.lef
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Command to set new value for SYNTH_STRATEGY
set ::env(SYNTH_STRATEGY) "DELAY 3"

# Command to set new value for SYNTH_SIZING
set ::env(SYNTH_SIZING) 1

# Now that the design is prepped and ready, we can run synthesis using following command
run_synthesis

# Following commands are alltogather sourced in "run_floorplan" command
init_floorplan
place_io
tap_decap_or

# Now we are ready to run placement
run_placement

# Incase getting error
unset ::env(LIB_CTS)

# With placement done we are now ready to run CTS
run_cts

# Now that CTS is done we can do power distribution network
gen_pdn

```
![image](https://github.com/user-attachments/assets/e27f4721-943e-46d8-b5bf-1f0639f2f72d)


![image](https://github.com/user-attachments/assets/11a3cad7-c2eb-4a4c-9c5f-cfcfa5f8e567)


![image](https://github.com/user-attachments/assets/f0d74d0c-c431-4962-a65d-26a8dd05a126)


Now, in a new terminal

```
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/13-11_22-33/tmp/floorplan/
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read 18-pdn.def &
```
![image](https://github.com/user-attachments/assets/e6732218-d670-426e-a79a-f15bb3274788)


![image](https://github.com/user-attachments/assets/bcb16862-cac5-4ad5-a1f9-915651d8a9e3)


When the power distribution network (PDN) generation command is issued, the system creates the PDN using the design_cts.def file as input.

The PDN consists of power rings, straps, and rails:

- Power is initially drawn from the VDD and VSS pads to the power rings.
- Horizontal and vertical straps are connected to the rings to further distribute power, with these straps channeling power to the rails connected to standard cells.
- Rails are placed at standard cell height intervals, which align with multiples of the track pitch (2.72 in this design), allowing proper power delivery to all standard cells.

In this design:

-Straps are placed on metal layers 4 and 5, while standard cell rails are on metal layer 1.
-Vias are used to interconnect these layers, ensuring seamless power flow from pads to cells across the different metal levels.

![image](https://github.com/user-attachments/assets/1c9f164b-9414-4d71-a9f7-6eef3cb1fe5a)

Now, we perfrom detailed routing using TritonRoute:

```
echo $::env(CURRENT_DEF)
echo $::env(ROUTING_STRATEGY)
run_routing
```

![image](https://github.com/user-attachments/assets/eff9a773-89eb-46fd-875c-709a5526b227)

![image](https://github.com/user-attachments/assets/54cc64b5-5e82-4f8b-9d14-5c536c90f4d4)



Now, in a new terminal

```
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/13-11_22-33/results/routing/
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.def &
```

![image](https://github.com/user-attachments/assets/30e206e6-beeb-4353-8a4a-977c80ecd0bf)



![image](https://github.com/user-attachments/assets/45ab9113-5985-472b-a153-51bf95404bff)

Fast route guide present in `openlane/designs/picorv32a/runs/13-11_22-33/tmp/routing` 

![image](https://github.com/user-attachments/assets/6f182733-d5cc-4952-95f5-314113704dbc)




#### 4. Post-Route OpenSTA timing analysis with the extracted parasitics of the route.

Commands to be run in OpenLANE flow to do OpenROAD timing analysis with integrated OpenSTA in OpenROAD

```tcl
# Command to run OpenROAD tool
openroad
# Reading lef file
read_lef /openLANE_flow/designs/picorv32a/runs/13-11_22-33/tmp/merged.lef
# Reading def file
read_def /openLANE_flow/designs/picorv32a/runs/13-11_22-33/results/routing/picorv32a.def
# Creating an OpenROAD database to work with
write_db pico_route.db
# Loading the created database in OpenROAD
read_db pico_route.db
# Read netlist post CTS
read_verilog /openLANE_flow/designs/picorv32a/runs/13-11_22-33/results/synthesis/picorv32a.synthesis_preroute.v
# Read library for design
read_liberty $::env(LIB_SYNTH_COMPLETE)
# Link design and library
link_design picorv32a
# Read in the custom sdc we created
read_sdc /openLANE_flow/designs/picorv32a/src/my_base.sdc
# Setting all cloks as propagated clocks
set_propagated_clock [all_clocks]
# Read SPEF
read_spef /openLANE_flow/designs/picorv32a/runs/13-11_22-33/results/routing/picorv32a.spef
# Generating custom timing report
report_checks -path_delay min_max -fields {slew trans net cap input_pins} -format full_clock_expanded -digits 4
# Exit to OpenLANE flow
exit
```

Screenshots of commands run and timing report generated
![image](https://github.com/user-attachments/assets/bbb97f10-cdb7-4538-be9c-01797d29eb60)

![image](https://github.com/user-attachments/assets/83f64ce4-896f-427a-ab94-6b25c5f9cab5)


![image](https://github.com/user-attachments/assets/0f47ff1f-c2b7-411f-8237-1d161a4744d5)


![image](https://github.com/user-attachments/assets/0e57d4a4-5a8f-47cb-8377-fd0bbf72f213)



</details>









# TASK 15      
( 19/11/2024 )

<details>
       <summary> OpenROAD PHYSICAL DESIGN </summary>

## Installing and setting up ORFS

```
git clone --recursive https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts
```

![1](https://github.com/user-attachments/assets/2f9a6fd0-9122-45be-a73e-4deafeb2bd86)

```
cd OpenROAD-flow-scripts
sudo ./setup.sh
```
![2](https://github.com/user-attachments/assets/9d49983c-43b0-4ee6-ab11-8b4058995263)
![3](https://github.com/user-attachments/assets/8d5ce225-cf68-4320-9889-e58af1aa2481)

```
./build_openroad.sh --local
```

![4](https://github.com/user-attachments/assets/592018b3-5434-4998-88a7-2b7fe50b5fc0)


![5](https://github.com/user-attachments/assets/3c83b73e-c8f5-400a-9a1a-e15726096f6b)




## Verify Installation

```
source ./env.sh
yosys -help
```
![6](https://github.com/user-attachments/assets/db53d47f-8f01-48ef-92bd-26bd26c1668f)


```
openroad -help
cd flow
make
```
![7](https://github.com/user-attachments/assets/9dd913c8-f003-46e2-bc29-4b311ab2a549)


![8](https://github.com/user-attachments/assets/04f4c28f-9617-4a90-a8d9-41774001ec9d)



```
make gui_final
```
![9](https://github.com/user-attachments/assets/d3532218-c97e-46ff-8e9a-0a4c0c527b7e)


![10](https://github.com/user-attachments/assets/8afba1bb-3c40-4f5c-b76b-6841fd6dbb90)





## ORFS Directory Structure And File Formats 

![Screenshot from 2024-11-25 21-14-15](https://github.com/user-attachments/assets/868d2230-a909-4eff-b8c8-981d0167b066)


```
├── OpenROAD-flow-scripts             
│   ├── docker           -> It has Docker based installation, run scripts and all saved here
│   ├── docs             -> Documentation for OpenROAD or its flow scripts.  
│   ├── flow             -> Files related to run RTL to GDS flow  
|   ├── jenkins          -> It contains the regression test designed for each build update
│   ├── tools            -> It contains all the required tools to run RTL to GDS flow
│   ├── etc              -> Has the dependency installer script and other things
│   ├── setup_env.sh     -> Its the source file to source all our OpenROAD rules to run the RTL to GDS flow
```
### Now, go to flow directory
```
cd flow
ls
```

![Screenshot from 2024-11-25 21-16-18](https://github.com/user-attachments/assets/666952b4-4f15-49c4-bfb6-74ec0900aa78)

```
├── flow           
│   ├── design           -> It has built-in examples from RTL to GDS flow across different technology nodes
│   ├── makefile         -> The automated flow runs through makefile setup
│   ├── platform         -> It has different technology note libraries, lef files, GDS etc 
|   ├── tutorials        
│   ├── util            
│   ├── scripts             
```


Automated RTL2GDS Flow for VSDBabySoC:

Initial Steps:

- We need to create a directory `vsdbabysoc` inside `OpenROAD-flow-scripts/flow/designs/sky130hd`
- Now create a directory `vsdbabysoc` inside `OpenROAD-flow-scripts/flow/designs/src` and include all the verilog files here.
- Now copy the folders `gds`, `include`, `lef` and `lib` from the VSDBabySoC folder in your system into this directory.
  - The `gds` folder would contain the files `avsddac.gds` and `avsdpll.gds`
  - The `include` folder would contain the files `sandpiper.vh`, `sandpiper_gen.vh`, `sp_default.vh` and `sp_verilog.vh`
  - The `gds` folder would contain the files `avsddac.lef` and `avsdpll.lef`
  - The `lib` folder would contain the files `avsddac.lib` and `avsdpll.lib`
- Now copy the constraints file(`vsdbabysoc_synthesis.sdc`) from the VSDBabySoC folder in your system into this directory.
- Now copy the files(`macro.cfg` and `pin_order.cfg`) from the VSDBabySoC folder in your system into this directory.

  
- ### Now, create a `config.mk` file whose contents are shown below:

```
export DESIGN_NICKNAME = vsdbabysoc
export DESIGN_NAME = vsdbabysoc
export PLATFORM    = sky130hd

# export VERILOG_FILES_BLACKBOX = $(DESIGN_HOME)/src/$(DESIGN_NICKNAME)/IPs/*.v
# export VERILOG_FILES = $(sort $(wildcard $(DESIGN_HOME)/src/$(DESIGN_NICKNAME)/*.v))
# Explicitly list the Verilog files for synthesis
export VERILOG_FILES = /home/chandra-shekhar-jha/VLSI/ORFS/OpenROAD-flow-scripts/flow/designs/sky130hd/VSDBabySoC/src/module/vsdbabysoc.v \
                       /home/chandra-shekhar-jha/VLSI/ORFS/OpenROAD-flow-scripts/flow/designs/sky130hd/VSDBabySoC/src/module/rvmyth.v \
                       /home/chandra-shekhar-jha/VLSI/ORFS/OpenROAD-flow-scripts/flow/designs/sky130hd/VSDBabySoC/src/module/clk_gate.v

export SDC_FILE      = /home/chandra-shekhar-jha/VLSI/ORFS/OpenROAD-flow-scripts/flow/designs/sky130hd/VSDBabySoC/src/sdc/vsdbabysoc_synthesis.sdc

#export DIE_AREA   = 0 0 1500 1500
# export CORE_AREA  = 10 10 2910 3510

# export PLACE_DENSITY ?= 0.23

export vsdbabysoc_DIR = /home/chandra-shekhar-jha/VLSI/ORFS/OpenROAD-flow-scripts/flow/designs/sky130hd/VSDBabySoC

export VERILOG_INCLUDE_DIRS = /home/chandra-shekhar-jha/VLSI/ORFS/OpenROAD-flow-scripts/flow/designs/sky130hd/VSDBabySoC/src/include

# export SDC_FILE      = $(wildcard $(vsdbabysoc_DIR)/sdc/*.sdc)
export ADDITIONAL_GDS  =/home/chandra-shekhar-jha/VLSI/ORFS/OpenROAD-flow-scripts/flow/designs/sky130hd/VSDBabySoC/src/gds
export ADDITIONAL_LEFS  = /home/chandra-shekhar-jha/VLSI/ORFS/OpenROAD-flow-scripts/flow/designs/sky130hd/VSDBabySoC/src/lef

export ADDITIONAL_LIBS = /home/chandra-shekhar-jha/VLSI/ORFS/OpenROAD-flow-scripts/flow/designs/sky130hd/VSDBabySoC/src/lib/avsddac.lib \
				         /home/chandra-shekhar-jha/VLSI/ORFS/OpenROAD-flow-scripts/flow/designs/sky130hd/VSDBabySoC/src/lib/avsdpll.lib
# Clock Configuration (vsdbabysoc specific)
# export CLOCK_PERIOD = 20.0
export CLOCK_PORT = CLK
export CLOCK_NET = $(CLOCK_PORT)

# Floorplanning Configuration (vsdbabysoc specific)
export FP_PIN_ORDER_CFG = /home/chandra-shekhar-jha/VLSI/ORFS/OpenROAD-flow-scripts/flow/designs/sky130hd/VSDBabySoC/src/layout_conf/vsdbabysoc/pin_order.cfg
export FP_SIZING = absolute
export DIE_AREA = 0 0 2000 2000
export CORE_AREA = 10 10 1800 1800


# export PL_RESIZER_HOLD_MAX_BUFFER_PERCENT = 80
# export PL_RESIZER_HOLD_MAX_BUFFER_COUNT = 5000  # Set the buffer limit to a higher value if needed
# export GLB_RESIZER_HOLD_MAX_BUFFER_PERCENT = 80

# Hold Slack Margin Configuration
# export PL_RESIZER_HOLD_SLACK_MARGIN = 0.01
# export GLB_RESIZER_HOLD_SLACK_MARGIN = 0.01


export BOTTOM_MARGIN_MULT = 50
export TOP_MARGIN_MULT = 50
export LEFT_MARGIN_MULT = 200
export RIGHT_MARGIN_MULT = 200

# Placement Configuration (vsdbabysoc specific)
export MACRO_PLACEMENT_CFG = /home/chandra-shekhar-jha/VLSI/ORFS/OpenROAD-flow-scripts/flow/designs/sky130hd/VSDBabySoC/src/layout_conf/vsdbabysoc/macro.cfg

# Magic Tool Configuration
export MAGIC_ZEROIZE_ORIGIN = 0
export MAGIC_EXT_USE_GDS = 1

export SYNTH_HIERARCHICAL = 1

# export RTLMP_BOUNDARY_WT = 0
#  MACRO_PLACE_HALO = 100 100
# export MACRO_PLACE_CHANNEL = 200 200

# CTS tuning
# export CTS_BUF_DISTANCE = 600
# export SKIP_GATE_CLONING = 1

# export SETUP_SLACK_MARGIN = 0.2

# This is high, some SRAMs should probably be converted
# to real SRAMs and not instantiated as flops
# export SYNTH_MEMORY_MAX_BITS ?= 42000

  
```






## Commands for synthesis:
```
make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.mk synth
```

![Screenshot from 2024-11-25 22-37-16](https://github.com/user-attachments/assets/dbf8fac9-fb1c-47c8-b3b7-ed272ccea512)



![Screenshot from 2024-11-25 22-52-08](https://github.com/user-attachments/assets/a757dcd9-c004-4866-8124-fc6d2eea09a9)



### Synthesis netlist:

![Screenshot from 2024-11-25 22-54-25](https://github.com/user-attachments/assets/a6126f49-2774-4643-a665-de4292726ed5)


### Synthesis log:
![Screenshot from 2024-11-25 22-57-07](https://github.com/user-attachments/assets/da478802-d8d1-44b0-bd68-a78883820b1e)

### Synthesis Check:

![Screenshot from 2024-11-25 22-59-15](https://github.com/user-attachments/assets/cc3a9682-77f7-49bd-98d8-a139a688be31)


### Synthesis Stats:



![Screenshot from 2024-11-25 23-06-25](https://github.com/user-attachments/assets/e3df56d0-d74f-4fdb-99f9-e3e7e47315d0)


![Screenshot from 2024-11-25 23-07-01](https://github.com/user-attachments/assets/746ce87a-111c-470c-842d-5062032b48d1)


![Screenshot from 2024-11-25 23-07-31](https://github.com/user-attachments/assets/cd46a1de-c7dc-4647-bee7-e4076ab9d85a)



![Screenshot from 2024-11-25 23-07-58](https://github.com/user-attachments/assets/efdd17f3-ce5d-41ab-bfb4-614c14220022)


```

24. Printing statistics.

=== vsdbabysoc ===

   Number of wires:               9843
   Number of wire bits:           9843
   Number of public wires:        1930
   Number of public wire bits:    1930
   Number of ports:                  7
   Number of port bits:              7
   Number of memories:               0
   Number of memory bits:            0
   Number of processes:              0
   Number of cells:               9699
     avsddac                         1
     avsdpll                         1
     sky130_fd_sc_hd__a2111o_1       1
     sky130_fd_sc_hd__a2111oi_0      2
     sky130_fd_sc_hd__a2111oi_2      1
     sky130_fd_sc_hd__a2111oi_4      1
     sky130_fd_sc_hd__a211o_1        5
     sky130_fd_sc_hd__a211oi_1      28
     sky130_fd_sc_hd__a211oi_2       1
     sky130_fd_sc_hd__a21bo_2        2
     sky130_fd_sc_hd__a21boi_0       6
     sky130_fd_sc_hd__a21o_1        24
     sky130_fd_sc_hd__a21oi_1     1100
     sky130_fd_sc_hd__a21oi_2        2
     sky130_fd_sc_hd__a21oi_4        1
     sky130_fd_sc_hd__a221oi_1     225
     sky130_fd_sc_hd__a22o_1       222
     sky130_fd_sc_hd__a22oi_1      494
     sky130_fd_sc_hd__a311oi_1     128
     sky130_fd_sc_hd__a31o_2         1
     sky130_fd_sc_hd__a31oi_1       63
     sky130_fd_sc_hd__a31oi_2        2
     sky130_fd_sc_hd__a32oi_2        1
     sky130_fd_sc_hd__a41oi_1        1
     sky130_fd_sc_hd__a41oi_2        2
     sky130_fd_sc_hd__and2_0         2
     sky130_fd_sc_hd__and2_1         8
     sky130_fd_sc_hd__and3_1        40
     sky130_fd_sc_hd__and3b_1        1
     sky130_fd_sc_hd__and4_1         3
     sky130_fd_sc_hd__buf_1         72
     sky130_fd_sc_hd__buf_2        103
     sky130_fd_sc_hd__buf_4         23
     sky130_fd_sc_hd__buf_6          1
     sky130_fd_sc_hd__clkbuf_1     779
     sky130_fd_sc_hd__clkbuf_2       1
     sky130_fd_sc_hd__conb_1         1
     sky130_fd_sc_hd__dfxtp_1     1787
     sky130_fd_sc_hd__fa_1           3
     sky130_fd_sc_hd__ha_1         135
     sky130_fd_sc_hd__inv_1        141
     sky130_fd_sc_hd__inv_2          1
     sky130_fd_sc_hd__inv_6          1
     sky130_fd_sc_hd__mux2_2         4
     sky130_fd_sc_hd__mux2_4         1
     sky130_fd_sc_hd__mux2i_1       11
     sky130_fd_sc_hd__nand2_1     2071
     sky130_fd_sc_hd__nand2b_1      35
     sky130_fd_sc_hd__nand3_1      461
     sky130_fd_sc_hd__nand3b_1      38
     sky130_fd_sc_hd__nand4_1      153
     sky130_fd_sc_hd__nand4b_1       1
     sky130_fd_sc_hd__nor2_1       345
     sky130_fd_sc_hd__nor2_2        17
     sky130_fd_sc_hd__nor2_4        11
     sky130_fd_sc_hd__nor2b_1       53
     sky130_fd_sc_hd__nor3_1        68
     sky130_fd_sc_hd__nor3_2         2
     sky130_fd_sc_hd__nor3_4         8
     sky130_fd_sc_hd__nor3b_1        2
     sky130_fd_sc_hd__nor4_1        33
     sky130_fd_sc_hd__nor4_2         1
     sky130_fd_sc_hd__nor4_4         1
     sky130_fd_sc_hd__nor4b_1        2
     sky130_fd_sc_hd__o2111a_1       1
     sky130_fd_sc_hd__o2111ai_1      3
     sky130_fd_sc_hd__o211ai_1      91
     sky130_fd_sc_hd__o211ai_4       1
     sky130_fd_sc_hd__o21a_1        10
     sky130_fd_sc_hd__o21ai_0      399
     sky130_fd_sc_hd__o21ai_1       55
     sky130_fd_sc_hd__o21ai_2        1
     sky130_fd_sc_hd__o21bai_1      11
     sky130_fd_sc_hd__o221ai_1     138
     sky130_fd_sc_hd__o22a_1        33
     sky130_fd_sc_hd__o22ai_1       31
     sky130_fd_sc_hd__o2bb2ai_1      3
     sky130_fd_sc_hd__o311ai_0      35
     sky130_fd_sc_hd__o311ai_2       1
     sky130_fd_sc_hd__o31a_1         1
     sky130_fd_sc_hd__o31ai_1       16
     sky130_fd_sc_hd__o32a_1        15
     sky130_fd_sc_hd__o32ai_1       18
     sky130_fd_sc_hd__o41ai_1        2
     sky130_fd_sc_hd__or2_2         12
     sky130_fd_sc_hd__or3_1         16
     sky130_fd_sc_hd__or3_4          3
     sky130_fd_sc_hd__or4_1         12
     sky130_fd_sc_hd__xnor2_1       49
     sky130_fd_sc_hd__xor2_1         7

   Area for cell type \avsddac is unknown!
   Area for cell type \avsdpll is unknown!

   Chip area for module '\vsdbabysoc': 78474.012800
     of which used for sequential elements: 35774.310400 (45.59%)

```

## Commands for floorplan:

```
make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.mk floorplan
```

![Screenshot from 2024-11-25 23-21-58](https://github.com/user-attachments/assets/4602adf8-3a94-4cba-bf0e-3dc1111f4096)

![Screenshot from 2024-11-26 04-26-28](https://github.com/user-attachments/assets/c31d5815-10e7-4226-9336-b36908ee2396)



```
make gui_floorplan
```
![Screenshot from 2024-11-26 04-28-35](https://github.com/user-attachments/assets/c24e2454-226e-4dfe-aec3-088eed6cb996)

![Screenshot from 2024-11-26 04-29-49](https://github.com/user-attachments/assets/c65ffca9-41ba-49c7-893f-98081b9beada)


```
make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.mk gui_floorplan
```
![Screenshot from 2024-11-26 04-31-39](https://github.com/user-attachments/assets/a4299117-1498-4a04-a015-981da24b3f97)


![Screenshot from 2024-11-26 04-32-13](https://github.com/user-attachments/assets/ee5845aa-edcf-48ae-8c02-f9da4d6559e5)

![Screenshot from 2024-11-26 04-32-55](https://github.com/user-attachments/assets/701b5abe-e84b-409d-9f91-dfc52883a176)


### FLOORPLAN TIMING REPORT

```

==========================================================================
floorplan final report_tns
--------------------------------------------------------------------------
tns 0.00

==========================================================================
floorplan final report_wns
--------------------------------------------------------------------------
wns 0.00

==========================================================================
floorplan final report_worst_slack
--------------------------------------------------------------------------
worst slack INF

==========================================================================
floorplan final report_checks -path_delay min
--------------------------------------------------------------------------
No paths found.

==========================================================================
floorplan final report_checks -path_delay max
--------------------------------------------------------------------------
No paths found.

==========================================================================
floorplan final report_checks -unconstrained
--------------------------------------------------------------------------
Startpoint: core.CPU_reset_a3$_DFF_P_ (rising edge-triggered flip-flop)
Endpoint: core.CPU_Xreg_value_a4[10][13]$_SDFFE_PP0P_
          (rising edge-triggered flip-flop)
Path Group: unconstrained
Path Type: max

Fanout     Cap    Slew   Delay    Time   Description
-----------------------------------------------------------------------------
                  0.00    0.00    0.00 ^ core.CPU_reset_a3$_DFF_P_/CLK (sky130_fd_sc_hd__dfxtp_1)
   591    1.46   13.42    9.67    9.67 ^ core.CPU_reset_a3$_DFF_P_/Q (sky130_fd_sc_hd__dfxtp_1)
                                         core.CPU_reset_a3 (net)
                 13.42    0.00    9.67 ^ _10124_/A (sky130_fd_sc_hd__inv_1)
   464    1.04    0.00   21.17   30.85 v _10124_/Y (sky130_fd_sc_hd__inv_1)
                                         _04513_ (net)
                  0.00    0.00   30.85 v _10227_/A (sky130_fd_sc_hd__nand3_1)
    31    0.08    0.78    0.52   31.37 ^ _10227_/Y (sky130_fd_sc_hd__nand3_1)
                                         _04613_ (net)
                  0.78    0.00   31.37 ^ _10232_/B1 (sky130_fd_sc_hd__o221ai_1)
     1    0.00    0.20    0.22   31.59 v _10232_/Y (sky130_fd_sc_hd__o221ai_1)
                                         _00548_ (net)
                  0.20    0.00   31.59 v core.CPU_Xreg_value_a4[10][13]$_SDFFE_PP0P_/D (sky130_fd_sc_hd__dfxtp_1)
                                 31.59   data arrival time
-----------------------------------------------------------------------------
(Path is unconstrained)



==========================================================================
floorplan final report_power
--------------------------------------------------------------------------
Group                  Internal  Switching    Leakage      Total
                          Power      Power      Power      Power (Watts)
----------------------------------------------------------------
Sequential             7.92e-12   3.67e-12   1.45e-08   1.45e-08  58.0%
Combinational          1.01e-11   1.77e-11   1.04e-08   1.05e-08  42.0%
Clock                  0.00e+00   0.00e+00   0.00e+00   0.00e+00   0.0%
Macro                  0.00e+00   0.00e+00   0.00e+00   0.00e+00   0.0%
Pad                    0.00e+00   0.00e+00   0.00e+00   0.00e+00   0.0%
----------------------------------------------------------------
Total                  1.80e-11   2.13e-11   2.49e-08   2.49e-08 100.0%
                           0.1%       0.1%      99.8%

```





## Commands for Placement:

```

make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.mk place

```
![Screenshot from 2024-11-25 23-59-42](https://github.com/user-attachments/assets/3968b903-60e8-4ef0-af51-4dba778d0165)

![Screenshot from 2024-11-26 00-01-17](https://github.com/user-attachments/assets/c883d461-d66e-4c96-afbc-61a309970393)



```
make gui_place

```


![Screenshot from 2024-11-26 04-43-10](https://github.com/user-attachments/assets/97ae2943-a818-498d-b2e2-ec866dd72605)

![Screenshot from 2024-11-26 04-43-46](https://github.com/user-attachments/assets/c19054f1-0f90-43b7-aa03-7349eba0ba2d)


### DETAILED PLACE TIMING REPORT



```

==========================================================================
detailed place report_tns
--------------------------------------------------------------------------
tns 0.00

==========================================================================
detailed place report_wns
--------------------------------------------------------------------------
wns 0.00

==========================================================================
detailed place report_worst_slack
--------------------------------------------------------------------------
worst slack INF

==========================================================================
detailed place report_checks -path_delay min
--------------------------------------------------------------------------
No paths found.

==========================================================================
detailed place report_checks -path_delay max
--------------------------------------------------------------------------
No paths found.

==========================================================================
detailed place report_checks -unconstrained
--------------------------------------------------------------------------
Startpoint: core.CPU_valid_taken_br_a4$_DFF_P_ (rising edge-triggered flip-flop)
Endpoint: core.CPU_Xreg_value_a4[15][18]$_SDFFE_PP0P_
          (rising edge-triggered flip-flop)
Path Group: unconstrained
Path Type: max

Fanout     Cap    Slew   Delay    Time   Description
-----------------------------------------------------------------------------
                  0.76    0.00    0.00 ^ core.CPU_valid_taken_br_a4$_DFF_P_/CLK (sky130_fd_sc_hd__dfxtp_1)
     2    0.01    0.04    0.46    0.46 v core.CPU_valid_taken_br_a4$_DFF_P_/Q (sky130_fd_sc_hd__dfxtp_1)
                                         core.CPU_valid_taken_br_a4 (net)
                  0.04    0.00    0.46 v _07913_/B (sky130_fd_sc_hd__or4_4)
    41    0.23    0.36    0.84    1.30 v _07913_/X (sky130_fd_sc_hd__or4_4)
                                         _02930_ (net)
                  0.36    0.02    1.31 v load_slew103/A (sky130_fd_sc_hd__buf_16)
    36    0.28    0.15    0.35    1.66 v load_slew103/X (sky130_fd_sc_hd__buf_16)
                                         net103 (net)
                  0.15    0.01    1.68 v max_cap102/A (sky130_fd_sc_hd__buf_16)
    24    0.27    0.14    0.26    1.94 v max_cap102/X (sky130_fd_sc_hd__buf_16)
                                         net102 (net)
                  0.16    0.04    1.97 v _07915_/A (sky130_fd_sc_hd__clkinv_16)
    43    0.48    0.31    0.25    2.22 ^ _07915_/Y (sky130_fd_sc_hd__clkinv_16)
                                         _02932_ (net)
                  0.37    0.11    2.33 ^ _09981_/C (sky130_fd_sc_hd__nor3_2)
     2    0.02    0.10    0.13    2.46 v _09981_/Y (sky130_fd_sc_hd__nor3_2)
                                         _04371_ (net)
                  0.10    0.00    2.46 v _09982_/B1 (sky130_fd_sc_hd__a21oi_4)
     6    0.10    0.69    0.57    3.02 ^ _09982_/Y (sky130_fd_sc_hd__a21oi_4)
                                         _04372_ (net)
                  0.69    0.00    3.02 ^ _09988_/A2 (sky130_fd_sc_hd__o21ai_4)
    16    0.12    0.32    0.36    3.39 v _09988_/Y (sky130_fd_sc_hd__o21ai_4)
                                         _04378_ (net)
                  0.32    0.00    3.39 v _11217_/A (sky130_fd_sc_hd__nor3_4)
    14    0.11    1.07    0.96    4.35 ^ _11217_/Y (sky130_fd_sc_hd__nor3_4)
                                         _05443_ (net)
                  1.07    0.00    4.35 ^ wire20/A (sky130_fd_sc_hd__buf_8)
    10    0.11    0.19    0.30    4.65 ^ wire20/X (sky130_fd_sc_hd__buf_8)
                                         net20 (net)
                  0.20    0.01    4.66 ^ _11238_/B (sky130_fd_sc_hd__nand2_4)
     5    0.04    0.22    0.13    4.79 v _11238_/Y (sky130_fd_sc_hd__nand2_4)
                                         _05460_ (net)
                  0.22    0.00    4.79 v _11253_/B1 (sky130_fd_sc_hd__o221ai_1)
     1    0.00    0.23    0.23    5.02 ^ _11253_/Y (sky130_fd_sc_hd__o221ai_1)
                                         _00713_ (net)
                  0.23    0.00    5.02 ^ core.CPU_Xreg_value_a4[15][18]$_SDFFE_PP0P_/D (sky130_fd_sc_hd__dfxtp_1)
                                  5.02   data arrival time
-----------------------------------------------------------------------------
(Path is unconstrained)



==========================================================================
detailed place report_check_types -max_slew -max_cap -max_fanout -violators
--------------------------------------------------------------------------

==========================================================================
detailed place max_slew_check_slack
--------------------------------------------------------------------------
0.06809719651937485

==========================================================================
detailed place max_slew_check_limit
--------------------------------------------------------------------------
1.4951549768447876

==========================================================================
detailed place max_slew_check_slack_limit
--------------------------------------------------------------------------
0.0455

==========================================================================
detailed place max_fanout_check_slack
--------------------------------------------------------------------------
1.0000000150474662e+30

==========================================================================
detailed place max_fanout_check_limit
--------------------------------------------------------------------------
1.0000000150474662e+30

==========================================================================
detailed place max_capacitance_check_slack
--------------------------------------------------------------------------
0.007044170051813126

==========================================================================
detailed place max_capacitance_check_limit
--------------------------------------------------------------------------
0.19410200417041779

==========================================================================
detailed place max_capacitance_check_slack_limit
--------------------------------------------------------------------------
0.0363

==========================================================================
detailed place max_slew_violation_count
--------------------------------------------------------------------------
max slew violation count 0

==========================================================================
detailed place max_fanout_violation_count
--------------------------------------------------------------------------
max fanout violation count 0

==========================================================================
detailed place max_cap_violation_count
--------------------------------------------------------------------------
max cap violation count 0

==========================================================================
detailed place setup_violation_count
--------------------------------------------------------------------------
setup violation count 0

==========================================================================
detailed place hold_violation_count
--------------------------------------------------------------------------
hold violation count 0

==========================================================================
detailed place report_checks -path_delay max reg to reg
--------------------------------------------------------------------------
No paths found.

==========================================================================
detailed place report_checks -path_delay min reg to reg
--------------------------------------------------------------------------
No paths found.

==========================================================================
detailed place critical path target clock latency max path
--------------------------------------------------------------------------
0

==========================================================================
detailed place critical path target clock latency min path
--------------------------------------------------------------------------
0

==========================================================================
detailed place critical path source clock latency min path
--------------------------------------------------------------------------
0

==========================================================================
detailed place critical path delay
--------------------------------------------------------------------------
-1

==========================================================================
detailed place critical path slack
--------------------------------------------------------------------------
0

==========================================================================
detailed place slack div critical path delay
--------------------------------------------------------------------------
0.000000

==========================================================================
detailed place report_power
--------------------------------------------------------------------------
Group                  Internal  Switching    Leakage      Total
                          Power      Power      Power      Power (Watts)
----------------------------------------------------------------
Sequential             9.16e-12   1.10e-11   1.45e-08   1.46e-08  49.9%
Combinational          1.89e-11   4.94e-11   1.46e-08   1.46e-08  50.1%
Clock                  0.00e+00   0.00e+00   0.00e+00   0.00e+00   0.0%
Macro                  0.00e+00   0.00e+00   0.00e+00   0.00e+00   0.0%
Pad                    0.00e+00   0.00e+00   0.00e+00   0.00e+00   0.0%
----------------------------------------------------------------
Total                  2.80e-11   6.04e-11   2.91e-08   2.92e-08 100.0%
                           0.1%       0.2%      99.7%

```




## CTS Command

```
make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.mk cts
```
![Screenshot from 2024-11-26 00-08-06](https://github.com/user-attachments/assets/bd9ed1f8-5171-45f1-8441-edeba696502d)

```
make gui_cts
```

![Screenshot from 2024-11-26 04-45-45](https://github.com/user-attachments/assets/c77d53a8-6227-4d3a-917c-31825828af6d)


![Screenshot from 2024-11-26 04-46-15](https://github.com/user-attachments/assets/8ed83d6a-63a8-4051-a677-5763a26ecd17)

CTS REPORT
```

==========================================================================
cts final report_tns
--------------------------------------------------------------------------
tns 0.00

==========================================================================
cts final report_wns
--------------------------------------------------------------------------
wns 0.00

==========================================================================
cts final report_worst_slack
--------------------------------------------------------------------------
worst slack INF

==========================================================================
cts final report_clock_skew
--------------------------------------------------------------------------
Clock clk
No launch/capture paths found.


==========================================================================
cts final report_checks -path_delay min
--------------------------------------------------------------------------
No paths found.

==========================================================================
cts final report_checks -path_delay max
--------------------------------------------------------------------------
No paths found.

==========================================================================
cts final report_checks -unconstrained
--------------------------------------------------------------------------
Startpoint: core.CPU_valid_taken_br_a4$_DFF_P_ (rising edge-triggered flip-flop)
Endpoint: core.CPU_Xreg_value_a4[15][13]$_SDFFE_PP0P_
          (rising edge-triggered flip-flop)
Path Group: unconstrained
Path Type: max

Fanout     Cap    Slew   Delay    Time   Description
-----------------------------------------------------------------------------
                  0.75    0.00    0.00 ^ core.CPU_valid_taken_br_a4$_DFF_P_/CLK (sky130_fd_sc_hd__dfxtp_1)
     2    0.01    0.04    0.46    0.46 v core.CPU_valid_taken_br_a4$_DFF_P_/Q (sky130_fd_sc_hd__dfxtp_1)
                                         core.CPU_valid_taken_br_a4 (net)
                  0.04    0.00    0.46 v _07913_/B (sky130_fd_sc_hd__or4_4)
    41    0.23    0.36    0.84    1.30 v _07913_/X (sky130_fd_sc_hd__or4_4)
                                         _02930_ (net)
                  0.36    0.01    1.31 v load_slew103/A (sky130_fd_sc_hd__buf_16)
    36    0.28    0.15    0.35    1.66 v load_slew103/X (sky130_fd_sc_hd__buf_16)
                                         net103 (net)
                  0.15    0.01    1.67 v max_cap102/A (sky130_fd_sc_hd__buf_16)
    24    0.27    0.15    0.26    1.94 v max_cap102/X (sky130_fd_sc_hd__buf_16)
                                         net102 (net)
                  0.16    0.04    1.97 v _07915_/A (sky130_fd_sc_hd__clkinv_16)
    43    0.48    0.31    0.25    2.22 ^ _07915_/Y (sky130_fd_sc_hd__clkinv_16)
                                         _02932_ (net)
                  0.38    0.11    2.33 ^ _09981_/C (sky130_fd_sc_hd__nor3_2)
     2    0.02    0.10    0.13    2.46 v _09981_/Y (sky130_fd_sc_hd__nor3_2)
                                         _04371_ (net)
                  0.10    0.00    2.46 v _09982_/B1 (sky130_fd_sc_hd__a21oi_4)
     6    0.10    0.70    0.57    3.03 ^ _09982_/Y (sky130_fd_sc_hd__a21oi_4)
                                         _04372_ (net)
                  0.70    0.00    3.03 ^ _09988_/A2 (sky130_fd_sc_hd__o21ai_4)
    16    0.11    0.31    0.36    3.39 v _09988_/Y (sky130_fd_sc_hd__o21ai_4)
                                         _04378_ (net)
                  0.31    0.00    3.39 v _11217_/A (sky130_fd_sc_hd__nor3_4)
    14    0.11    1.07    0.96    4.35 ^ _11217_/Y (sky130_fd_sc_hd__nor3_4)
                                         _05443_ (net)
                  1.07    0.00    4.35 ^ wire20/A (sky130_fd_sc_hd__buf_8)
    10    0.11    0.19    0.30    4.65 ^ wire20/X (sky130_fd_sc_hd__buf_8)
                                         net20 (net)
                  0.20    0.01    4.66 ^ _11238_/B (sky130_fd_sc_hd__nand2_4)
     5    0.04    0.22    0.13    4.79 v _11238_/Y (sky130_fd_sc_hd__nand2_4)
                                         _05460_ (net)
                  0.22    0.00    4.79 v _11240_/B1 (sky130_fd_sc_hd__o221ai_1)
     1    0.00    0.22    0.23    5.02 ^ _11240_/Y (sky130_fd_sc_hd__o221ai_1)
                                         _00708_ (net)
                  0.22    0.00    5.02 ^ core.CPU_Xreg_value_a4[15][13]$_SDFFE_PP0P_/D (sky130_fd_sc_hd__dfxtp_1)
                                  5.02   data arrival time
-----------------------------------------------------------------------------
(Path is unconstrained)



==========================================================================
cts final report_check_types -max_slew -max_cap -max_fanout -violators
--------------------------------------------------------------------------

==========================================================================
cts final max_slew_check_slack
--------------------------------------------------------------------------
0.05385647714138031

==========================================================================
cts final max_slew_check_limit
--------------------------------------------------------------------------
1.4951549768447876

==========================================================================
cts final max_slew_check_slack_limit
--------------------------------------------------------------------------
0.0360

==========================================================================
cts final max_fanout_check_slack
--------------------------------------------------------------------------
1.0000000150474662e+30

==========================================================================
cts final max_fanout_check_limit
--------------------------------------------------------------------------
1.0000000150474662e+30

==========================================================================
cts final max_capacitance_check_slack
--------------------------------------------------------------------------
0.005084257572889328

==========================================================================
cts final max_capacitance_check_limit
--------------------------------------------------------------------------
0.19410200417041779

==========================================================================
cts final max_capacitance_check_slack_limit
--------------------------------------------------------------------------
0.0262

==========================================================================
cts final max_slew_violation_count
--------------------------------------------------------------------------
max slew violation count 0

==========================================================================
cts final max_fanout_violation_count
--------------------------------------------------------------------------
max fanout violation count 0

==========================================================================
cts final max_cap_violation_count
--------------------------------------------------------------------------
max cap violation count 0

==========================================================================
cts final setup_violation_count
--------------------------------------------------------------------------
setup violation count 0

==========================================================================
cts final hold_violation_count
--------------------------------------------------------------------------
hold violation count 0

==========================================================================
cts final report_checks -path_delay max reg to reg
--------------------------------------------------------------------------
No paths found.

==========================================================================
cts final report_checks -path_delay min reg to reg
--------------------------------------------------------------------------
No paths found.

==========================================================================
cts final critical path target clock latency max path
--------------------------------------------------------------------------
0

==========================================================================
cts final critical path target clock latency min path
--------------------------------------------------------------------------
0

==========================================================================
cts final critical path source clock latency min path
--------------------------------------------------------------------------
0

==========================================================================
cts final critical path delay
--------------------------------------------------------------------------
-1

==========================================================================
cts final critical path slack
--------------------------------------------------------------------------
0

==========================================================================
cts final slack div critical path delay
--------------------------------------------------------------------------
0.000000

==========================================================================
cts final report_power
--------------------------------------------------------------------------
Group                  Internal  Switching    Leakage      Total
                          Power      Power      Power      Power (Watts)
----------------------------------------------------------------
Sequential             9.16e-12   1.11e-11   1.45e-08   1.46e-08  49.9%
Combinational          1.89e-11   4.96e-11   1.46e-08   1.46e-08  50.1%
Clock                  0.00e+00   0.00e+00   0.00e+00   0.00e+00   0.0%
Macro                  0.00e+00   0.00e+00   0.00e+00   0.00e+00   0.0%
Pad                    0.00e+00   0.00e+00   0.00e+00   0.00e+00   0.0%
----------------------------------------------------------------
Total                  2.81e-11   6.07e-11   2.91e-08   2.92e-08 100.0%
                           0.1%       0.2%      99.7%
```

```
make gui_route
```

![Screenshot from 2024-11-26 00-15-45](https://github.com/user-attachments/assets/27c79650-8b5d-4134-bb79-985a942b9933)

![Screenshot from 2024-11-26 00-17-17](https://github.com/user-attachments/assets/e2ffadb4-62f8-4a0d-bc3e-4a970ca2dc64)


### For Final Layout
```
make gui_final
```
![Screenshot from 2024-11-26 00-21-05](https://github.com/user-attachments/assets/879b9816-c00e-412c-a5ef-bfb2bfca7d1c)
![Screenshot from 2024-11-26 00-23-44](https://github.com/user-attachments/assets/7a887960-1d0b-4ddb-b4a8-da80ba8f8722)
![Screenshot from 2024-11-26 00-24-37](https://github.com/user-attachments/assets/f8da8b69-7c2c-4598-b6a5-2f56687c1e42)
![Screenshot from 2024-11-26 00-25-27](https://github.com/user-attachments/assets/28cbdd95-7f61-4182-93eb-e7cf76da64b7)


### To give the GDS file in the klayout type the following commands
```

 klayout -e -nn ./platforms/nangate45/FreePDK45.lyt -l ./platforms/nangate45/FreePDK45.lyp ./results/nangate45/gcd/base/6_final.gds
```

![Screenshot from 2024-11-26 00-28-30](https://github.com/user-attachments/assets/6381277c-6fc6-48c9-8d7e-1b60bdbdf7cc)

![Screenshot from 2024-11-26 00-31-39](https://github.com/user-attachments/assets/affb74f1-8e4b-4bee-b71a-7a1376e8227e)


### Route Command

```
make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.mk route
```
![Screenshot from 2024-11-26 03-34-04](https://github.com/user-attachments/assets/9ff3a2f6-558d-4de0-8fc9-3ae207d0d205)

![Screenshot from 2024-11-26 03-34-31](https://github.com/user-attachments/assets/3a4a939a-63c8-4c91-b9f5-90b340acf5fd)

![Screenshot from 2024-11-26 03-34-50](https://github.com/user-attachments/assets/5b16d308-621d-4cc0-afdd-738c1ef65b1d)


## VSDBabySoC Schematic :
![Screenshot from 2024-11-26 06-31-44](https://github.com/user-attachments/assets/0b512d53-bee1-41d4-bc00-b6d6df0d49e1)

![Screenshot from 2024-11-26 05-25-51](https://github.com/user-attachments/assets/6f0bbc50-580d-4f0e-a3ee-453dbe9f652a)

### QoR Report

```
make metadata
```
![Screenshot from 2024-11-26 06-00-28](https://github.com/user-attachments/assets/3b088b51-e0ce-4bc2-83ab-2388f47bc884)

![Screenshot from 2024-11-26 06-02-19](https://github.com/user-attachments/assets/2bd149f2-0d6d-4809-9140-baf344c0e8e6)

## HEATMAPS

### Placement Density
![Screenshot from 2024-11-26 06-12-49](https://github.com/user-attachments/assets/5ca51a2e-0059-49ba-839d-31f2720c6e25)

### Power Density
![Screenshot from 2024-11-26 06-13-28](https://github.com/user-attachments/assets/9de2a8fd-9d72-4e58-bbf1-8cb59fea684a)

### Routing Conjestion
![Screenshot from 2024-11-26 06-16-32](https://github.com/user-attachments/assets/bafb8beb-8da0-46b4-a101-70bafcfb0d2b)

### Estimated Conjestion (RUDY)
![Screenshot from 2024-11-26 06-17-35](https://github.com/user-attachments/assets/98556ec2-75c7-4058-bcaa-e8c3ad839f2c)

### IR Drop
![Screenshot from 2024-11-26 06-18-31](https://github.com/user-attachments/assets/cff35722-2840-46f8-937c-99931154d624)





</details>
