# EXPERIMENT 3: 8086 MICROPROCESSOR – BASIC ARITHMETIC OPERATIONS

**Date:** 17-11-2026  
**Name:** Sheikh Hamza J  
**Roll Number:** RA2511030010360  
**Department:** NWC  

---

## AIM

To write and execute 8086 Assembly Language programs to perform basic arithmetic operations such as addition, subtraction, multiplication, and division using an Online 8086 Emulator.

## SOFTWARE REQUIRED

1. Computer or laptop
2. Web browser (Google Chrome / Microsoft Edge)
3. Online 8086 Emulator
4. Internet connection

## THEORY

### 8086 Microprocessor

The Intel 8086 is a 16-bit microprocessor developed by Intel. It has a 16-bit data bus and a 20-bit address bus, allowing it to access up to 1 MB of memory. It consists of two main units:

- **Bus Interface Unit (BIU):** Fetches instructions from memory and handles communication between the processor and memory or input/output devices.
- **Execution Unit (EU):** Decodes and executes instructions using the arithmetic and logic unit (ALU), registers, and control circuitry.

The 8086 supports arithmetic, logical, data-transfer, and control-transfer instructions. In this experiment, arithmetic instructions are used to perform addition, subtraction, multiplication, and division.

### Technical Specifications of 8086

| Specification | Description |
|---|---|
| Microprocessor | Intel 8086 |
| Architecture | 16-bit |
| Data bus | 16-bit |
| Address bus | 20-bit |
| Maximum memory | 1 MB |
| Operating modes | Minimum and maximum |
| General-purpose registers | AX, BX, CX, DX |
| Pointer and index registers | SP, BP, SI, DI |
| Instruction categories | Arithmetic, logical, data transfer, and control transfer |
| Clock frequency | 5 MHz, 8 MHz, or 10 MHz, depending on the version |

## 8086 REGISTER ORGANIZATION

The 8086 contains registers that temporarily store data, addresses, and intermediate results while a program is executing.

- **AX (Accumulator):** Commonly used in arithmetic and logical operations. It can be divided into AH (higher 8 bits) and AL (lower 8 bits).
- **BX (Base Register):** Used for data storage and memory addressing. It can be divided into BH and BL.
- **CX (Count Register):** Commonly used as a counter in loop and shift operations. It can be divided into CH and CL.
- **DX (Data Register):** Used in some multiplication and division operations and input/output operations. It can be divided into DH and DL.
- **SI (Source Index):** Used as a source index in memory and string operations.
- **DI (Destination Index):** Used as a destination index in memory and string operations.
- **BP (Base Pointer):** Used to access data in the stack segment.
- **SP (Stack Pointer):** Points to the top of the stack.

## ARITHMETIC AND RELATED INSTRUCTIONS

| Instruction | Description |
|---|---|
| MOV | Transfers data from a source to a destination. |
| ADD | Adds the source operand to the destination operand. |
| SUB | Subtracts the source operand from the destination operand. |
| MUL | Performs unsigned multiplication. |
| DIV | Performs unsigned division. |
| HLT | Halts processor execution. |

### Important register behaviour

- For 8-bit addition and subtraction, the result is stored in the destination operand used in the instruction.
- For 8-bit unsigned multiplication, the processor multiplies AL by the specified 8-bit operand and stores the 16-bit result in AX (AH:AL).
- For 8-bit unsigned division, the processor divides AX by the specified 8-bit operand. The quotient is stored in AL and the remainder is stored in AH.
- The suffix `H` indicates that a number is written in hexadecimal notation.

## PROCEDURE

1. Open the Online 8086 Emulator in a web browser.
2. Select or open the 8086 microprocessor environment.
3. Enter the required 8086 Assembly Language program in the editor.
4. Assemble or compile the program.
5. Check whether the program contains any syntax errors.
6. If there are no errors, execute the program using the Run or Step option.
7. Observe the values stored in the relevant registers.
8. Compare the register values with the expected results of the arithmetic operation.
9. Repeat the same procedure for addition, subtraction, multiplication, and division.

## ONLINE 8086 EMULATOR

**Website:** https://yjdoc2.github.io/8086-emulator-web/

---

## EXPERIMENT 1: ADDITION

### AIM:
To perform the addition of two 8-bit numbers using the 8086 microprocessor.

### PROGRAM:

```asm
MOV AL, 05H
MOV BL, 03H
ADD AL, BL
HLT
```

### EXPLANATION:

1. Load the first number 05H into AL.
2. Load the second number 03H into BL.
3. Perform addition using the ADD instruction.
4. The result is stored in AL.

### EXPECTED OUTPUT:

| Register | Value |
|---|---|
| AL | 08H |
| BL | 03H |

**Result:** 05H + 03H = 08H.

## EXPERIMENT 2: SUBTRACTION

### AIM:
To perform the subtraction of two 8-bit numbers using the 8086 microprocessor.

### PROGRAM:

```asm
MOV AL, 09H
MOV BL, 04H
SUB AL, BL
HLT
```

### EXPLANATION:

1. Load the first number 09H into AL.
2. Load the second number 04H into BL.
3. Perform subtraction using the SUB instruction.
4. The result is stored in AL.

### EXPECTED OUTPUT:

| Register | Value |
|---|---|
| AL | 05H |
| BL | 04H |

**Result:** 09H - 04H = 05H.

## EXPERIMENT 3: MULTIPLICATION

### AIM:
To perform the multiplication of two 8-bit unsigned numbers using the 8086 microprocessor.

### PROGRAM:

```asm
MOV AL, 05H
MOV BL, 04H
MUL BL
HLT
```

### EXPLANATION:

1. Load the first number 05H into AL.
2. Load the second number 04H into BL.
3. Perform multiplication using the MUL instruction.
4. The 16-bit result is stored in AX (AH:AL).

### EXPECTED OUTPUT:

| Register | Value |
|---|---|
| AL | 14H |
| AH | 00H |
| AX | 0014H |

**Result:** 05H × 04H = 14H.

## EXPERIMENT 4: DIVISION

### AIM:
To perform the division of two 8-bit unsigned numbers using the 8086 microprocessor.

### PROGRAM:

```asm
MOV AX, 0014H
MOV BL, 04H
DIV BL
HLT
```

### EXPLANATION:

1. Load the dividend 0014H into AX.
2. Load the divisor 04H into BL.
3. Perform division using the DIV instruction.
4. The quotient is stored in AL.
5. The remainder is stored in AH.

### EXPECTED OUTPUT:

| Register | Value |
|---|---|
| AL | 05H |
| AH | 00H |

**Result:** 14H ÷ 04H = 05H, Remainder = 00H.

## OUTPUT OF SIMULATION:

### FIGURE-01: ADDITION OUTPUT

<img width="402" height="392" alt="image" src="https://github.com/user-attachments/assets/24723076-ce8c-482b-90c0-72ecb7966aed" />

### FIGURE-02: SUBTRACTION OUTPUT

<img width="407" height="398" alt="image" src="https://github.com/user-attachments/assets/6af6bb72-0313-45a5-a0d3-586ee7808c32" />


### FIGURE-03: MULTIPLICATION OUTPUT

<img width="402" height="402" alt="image" src="https://github.com/user-attachments/assets/56c1c093-4368-4ab7-aa64-2006d3d471ce" />


### FIGURE-04: DIVISION OUTPUT

<img width="385" height="390" alt="image" src="https://github.com/user-attachments/assets/0eef9fdf-913d-4212-99e8-6f7e8d0f5594" />

## OVERALL RESULT

The 8086 Assembly Language programs for addition, subtraction, multiplication, and division were written and executed using the Online 8086 Emulator. The results were verified by observing the corresponding register values.

## LEARNING OUTCOMES

After completing this experiment, the following concepts were understood:

1. The basic architecture and register organization of the 8086 microprocessor.
2. The use of general-purpose registers for storing data and intermediate results.
3. The working of the MOV, ADD, SUB, MUL, DIV, and HLT instructions.
4. The difference between 8-bit addition/subtraction, 8-bit multiplication, and 8-bit division in terms of result storage.
5. The use of an online emulator to assemble and execute 8086 Assembly Language programs.
6. The process of observing register contents and verifying arithmetic results.

## VIVA QUESTIONS AND ANSWERS

**1. What is a microprocessor?**  
A microprocessor is a programmable electronic chip that performs arithmetic, logical, and control operations.

**2. What is the 8086 microprocessor?**  
The 8086 is a 16-bit microprocessor developed by Intel.

**3. Why is the 8086 called a 16-bit microprocessor?**  
It is called a 16-bit microprocessor because its ALU and main internal data operations work with 16-bit data.

**4. What are the two main units of the 8086?**  
The Bus Interface Unit (BIU) and the Execution Unit (EU).

**5. What is a register?**  
A register is a small, fast storage location inside the processor used to hold data or addresses temporarily.

**6. What is the function of the AX register?**  
AX is the accumulator register and is commonly used in arithmetic operations.

**7. What are AH and AL?**  
AH is the higher 8 bits of AX, and AL is the lower 8 bits of AX.

**8. What is the function of the MOV instruction?**  
MOV copies data from a source to a destination.

**9. Which instruction is used for addition?**  
The ADD instruction.

**10. Which instruction is used for subtraction?**  
The SUB instruction.

**11. Which instruction is used for multiplication?**  
The MUL instruction is used for unsigned multiplication.

**12. Which instruction is used for division?**  
The DIV instruction is used for unsigned division.

**13. What is the function of HLT?**  
HLT halts the processor's execution.

**14. Where is the result of 8-bit addition stored in this experiment?**  
The result is stored in AL.

**15. Where is the result of 8-bit subtraction stored in this experiment?**  
The result is stored in AL.

**16. Where is the result of 8-bit multiplication stored?**  
The 16-bit result is stored in AX, with AH holding the higher byte and AL holding the lower byte.

**17. Where are the quotient and remainder stored in 8-bit division?**  
The quotient is stored in AL and the remainder is stored in AH.

**18. What is the difference between MUL and IMUL?**  
MUL performs unsigned multiplication, whereas IMUL performs signed multiplication.

**19. What is the difference between DIV and IDIV?**  
DIV performs unsigned division, whereas IDIV performs signed division.

**20. What does the letter H mean in a value such as 05H?**  
H indicates that the value is represented in hexadecimal notation.

**21. What happens if the divisor is zero?**  
The processor generates a divide-error exception.

**22. What is the difference between a quotient and a remainder?**  
The quotient is the whole-number result of division, while the remainder is the value left over.

**23. What is an emulator?**  
An emulator is software that imitates the operation of a hardware system so that programs can be tested without the physical hardware.

**24. What is the purpose of the ALU?**  
The Arithmetic Logic Unit performs arithmetic and logical operations.

**25. What is the difference between 8-bit and 16-bit data?**  
8-bit data contains 8 binary bits, while 16-bit data contains 16 binary bits.

---

**Platform:** Online 8086 Emulator  
**Programming Language:** 8086 Assembly Language  
**Experiment:** Basic Arithmetic Operations
