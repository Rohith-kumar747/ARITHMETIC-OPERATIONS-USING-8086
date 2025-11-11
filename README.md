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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     2000-33             |      2004-66             |
|     2001-33             |      2005-66             |
|     2002-33             |                          |
|     2003-33             |                          |
      
#### Manual Calculations
<img width="1077" height="754" alt="Screenshot 2025-11-11 200731" src="https://github.com/user-attachments/assets/fbdf17e7-fd56-445a-8b20-51bf7cb86d1d" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="642" height="433" alt="Screenshot 2025-11-11 153351" src="https://github.com/user-attachments/assets/fc75326b-04b0-4e47-8cd1-2168220523c4" />


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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     2000-88             |      2004-44             |
|     2001-88             |      2005-44             |
|     2002-44             |                          |
|     2003-44             |                          |
      
#### Manual Calculations

<img width="1191" height="758" alt="image" src="https://github.com/user-attachments/assets/750f48c8-95b8-439f-a746-00253f3df846" />

---
## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="642" height="433" alt="Screenshot 2025-11-11 154754" src="https://github.com/user-attachments/assets/72958127-9f4d-4612-8d0c-064cbb616173" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     2000-03             |      2004-33             |
|     2001-00             |      2005-00             |
|     2002-11             |                          |
|     2003-00             |                          |
      

#### Manual Calculations

<img width="726" height="759" alt="Screenshot 2025-11-11 201232" src="https://github.com/user-attachments/assets/0708dd14-1a7b-4980-91fe-67afb9194195" />

---
## OUTPUT SCREEN FROM MASM SOFTWARE

![inmul](https://github.com/user-attachments/assets/f799b022-8264-457b-8008-91974e74fb34)


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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     2000-99             |      2004-03             |
|     2001-99             |      2005-00             |
|     2002-33             |                          |
|     2003-33             |                          |
      
#### Manual Calculations
![WhatsApp Image 2025-11-11 at 8 02 24 PM](https://github.com/user-attachments/assets/797fc03f-aad6-47f7-b376-2ab7e758d98d)

---
## OUTPUT FROM MASM SOFTWARE

![WhatsApp Image 2025-10-30 at 11 50 18 PM](https://github.com/user-attachments/assets/e6a3dd2d-7edb-4186-8e81-1eeec30f50f1)


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

