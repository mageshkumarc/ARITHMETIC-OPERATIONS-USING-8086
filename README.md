# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) |      DATA (INPUT)        |
| ----------------------- | ------------------------ |
|         2000            |           86             |
|         2001            |           49             |
|         2002            |           13             |
|         2003            |           35             |


| MEMORY LOCATION (OUTPUT)|      DATA (OUTPUT)       |
| ----------------------- | ------------------------ |
|         2004            |           99             |
|         2005            |           7E             |
|         2006            |           00             |


#### Manual Calculations

![WhatsApp Image 2025-09-21 at 22 13 15_8fb7f91b](https://github.com/user-attachments/assets/1879e6df-bec8-4eed-a11e-85ee0cd1dec5)


---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="637" height="398" alt="INDIRECT ADDITION OUTPUT" src="https://github.com/user-attachments/assets/da003391-ce67-4696-8dc9-ac04e5efefe3" />



## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) |      DATA (INPUT)        |
| ----------------------- | ------------------------ |
|         2000            |           86             |
|         2001            |           49             |
|         2002            |           13             |
|         2003            |           35             |


| MEMORY LOCATION (OUTPUT)|      DATA (OUTPUT)       |
| ----------------------- | ------------------------ |
|         2004            |           73             |
|         2005            |           14             |
|         2006            |           00             |

#### Manual Calculations

![WhatsApp Image 2025-09-21 at 22 13 15_fe1989e3](https://github.com/user-attachments/assets/b9b8fbf6-298e-4474-8766-21145f0cba38)


---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="639" height="399" alt="INDIRECT SUBTRACTION OUTPUT" src="https://github.com/user-attachments/assets/ba6e81d1-40e4-4aaa-a223-0d1b989de89f" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

### FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) |      DATA (INPUT)        |
| ----------------------- | ------------------------ |
|         2000            |           86             |
|         2001            |           49             |
|         2002            |           13             |
|         2003            |           35             |


| MEMORY LOCATION (OUTPUT)|      DATA (OUTPUT)       |
| ----------------------- | ------------------------ |
|         2004            |           1D             |
|         2005            |           38             |
|         2006            |           13             |

#### Manual Calculations

![WhatsApp Image 2025-09-21 at 22 13 15_87454127](https://github.com/user-attachments/assets/3b8bdaad-7c42-4fed-818a-946e332f1c2a)


---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="637" height="399" alt="INDIRECT MULTIPLICATION OUTPUT" src="https://github.com/user-attachments/assets/2da13846-b0ab-4294-9a8f-0088be80b56e" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) |      DATA (INPUT)        |
| ----------------------- | ------------------------ |
|         2000            |           68             |
|         2001            |           24             |
|         2002            |           68             |
|         2003            |           22             |


| MEMORY LOCATION (OUTPUT)|      DATA (OUTPUT)       |
| ----------------------- | ------------------------ |
|         2004            |           00             |
|         2005            |           01             |
|         2006            |           02             |

#### Manual Calculations

![WhatsApp Image 2025-09-21 at 22 13 15_6d02462d](https://github.com/user-attachments/assets/3624e44b-b0ac-48bc-8c7d-231c86f18df6)


---
## OUTPUT FROM MASM SOFTWARE

<img width="635" height="394" alt="INDIRECT DIVSION OUTPUT" src="https://github.com/user-attachments/assets/9d3cd038-b3f6-43b0-b9f9-41e89f43a02c" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

