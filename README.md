# TASK 1 : Create a simple C program and compile it using GCC followed by verification of the program output. 

### Step 1 : Open the text editor followed by assigning the name of the C program.

This can be done by giving the following command: leafpad sum1ton.c

Here leafpad is the text editor, sum1ton is the name of the file and at last .c represents that it is a C program.


![1](https://github.com/user-attachments/assets/188f3dea-68d2-489a-8db9-e4c6e11c8d39)


### Step 2 : Press enter and the text editor (leafpad) opensup as shown in the snapshot given below.


![2](https://github.com/user-attachments/assets/0283e5ea-978e-4200-b594-a206a8ad6a52)


### Step 3 : Write the required C program which calculates the sum from 1 to 5, as shown in the snapshot given below.


![3](https://github.com/user-attachments/assets/7f1386ba-74eb-4ef8-9a9f-0efb83338a0f)


### Step 4 : Press Ctrl + S in order to save the program that has been written.

### Step 5 : Now compile the program using GCC by giving the following command : gcc sum1on.c and press enter.


![4](https://github.com/user-attachments/assets/c78c877c-a870-4ea8-bbca-517f5443fe0f)


### Step 6 : Now check the output of the program by giving the following command : ./a.out


![5](https://github.com/user-attachments/assets/ffc1a40f-2449-4c0a-bce0-1c7add7d0427)


 ### Conclusion : In the above snapshot it is verified the program is compiled successfully and the result is also correct, that is 15 (1+2+3+4+5 = 15).


 # TASK 2 : Compiling and executing a C program using RISC - V compiler and optimize the compilation using O1 and Ofast.

 ### Step 1 : Write a simple C program in the text editor (leafpad) and save it. You can see contents of the C program below.

 ![1](https://github.com/user-attachments/assets/a454ed04-8a3a-4d5d-9851-9b65a8e079d2)

 ### Step 2 : Now compile the C program using RISC - V compiler using O1 optimization as shown in the snapshot shown below.

 ![3](https://github.com/user-attachments/assets/8e2a2657-fb13-4f58-9373-45a07489fbb1)

 ### Step 3 : Now create the object file (.o) that is the output of the compiler as shown in the procedure shown below.

 ![4](https://github.com/user-attachments/assets/0831e910-36b1-4f02-a61c-2d25b38d0cd2)

 ### Step 4 : As soon as you enter the above command, a huge list of opcode is shown in the terminal.

 ### But we are interested in main section of the program so type : /main as shown below.

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

 ![9](https://github.com/user-attachments/assets/c1b48f69-5459-4f66-9489-a43f03a236e4)

  ### In the snapshot shown below we can see the opcode of the main section.

  ![10](https://github.com/user-attachments/assets/b85f864a-57d8-46f3-bc92-5a1a19579da2)

  ## Observation 2 : There are 12 lines of opcode in the main section.

  ## Conclusion : The compilation in the later procedure is optimised.


 














