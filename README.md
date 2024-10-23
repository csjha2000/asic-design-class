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
- **TASK 11:** [Synthesize RISC-V and compare output with functional simulations.](#task-10)
      
  

# TASK 1      
( 16/07/2024 )

<details>
       <summary>Create a simple C program and compile it using GCC followed by verification of the program output.</summary>

## AIM : To Create a simple C program and compile it using GCC followed by verification of the program output. </summary>

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


# Functional Simulations

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










</details>








