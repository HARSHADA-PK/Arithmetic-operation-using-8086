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
|         1200:12         |          1204:24         |
|         1201:34         |          1205:68         |
|         1202:12         |          1206:00         |
|         1203:34         |          1207:C4         |


#### Manual Calculations

(Add your calculation here)

---![IMG-20250825-WA0007](https://github.com/user-attachments/assets/0934d746-14d6-4c13-94ba-80870b3dea1d)


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="623" height="379" alt="Screenshot 2025-08-25 190840" src="https://github.com/user-attachments/assets/696d7125-60df-47bb-b9f9-3bd4b6e3d6c2" />
<img width="619" height="377" alt="Screenshot 2025-08-25 191632" src="https://github.com/user-attachments/assets/b96532b9-c641-4b57-9949-9f7e3746a10f" />



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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200:12         |          1204:00         |
|         1201:34         |          1205:00         |
|         1202:12         |          1206:00         |
|         1203:34         |          1207:C4         |
#### Manual Calculations

(Add your calculation here)

---![IMG-20250825-WA0005](https://github.com/user-attachments/assets/102bb120-f477-4294-8323-d16927cf1cd8)



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="630" height="332" alt="Screenshot 2025-08-25 192336" src="https://github.com/user-attachments/assets/db03e3ad-e6a7-4c81-86ee-a3b17d4f10b7" />
<img width="639" height="390" alt="Screenshot 2025-08-25 192541" src="https://github.com/user-attachments/assets/07ac9578-96de-4fa4-b5dd-74f3ca5c617a" />




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
|         1200:12         |          1204:44         |
|         1201:34         |          1205:51         |
|         1202:12         |          1206:97         |
|         1203:34         |          1207:0A         |

#### Manual Calculations

(Add your calculation here)

---
![IMG-20250825-WA0003](https://github.com/user-attachments/assets/6923ae06-b998-4198-88a7-141c352a49bf)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="637" height="380" alt="Screenshot 2025-08-25 203602" src="https://github.com/user-attachments/assets/1b4639ed-6bd6-43ea-8cdd-4abf4e19ecd9" />
<img width="641" height="390" alt="Screenshot 2025-08-25 203808" src="https://github.com/user-attachments/assets/a28afcb3-2672-4179-87d3-edbf383daa2b" />



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
|         1200:12         |          1204:01         |
|         1201:34         |          1205:00         |
|         1202:12         |          1206:00         |
|         1203:34         |          1207:00         |



#### Manual Calculations

(Add your calculation here)

---![IMG-20250825-WA0006](https://github.com/user-attachments/assets/8306e4c9-f0ba-4d6b-940c-ee8ecbfd5078)

## OUTPUT FROM MASM SOFTWARE
<img width="631" height="379" alt="Screenshot 2025-08-25 204206" src="https://github.com/user-attachments/assets/5de73254-268e-4af7-aae1-793add015878" />
<img width="635" height="385" alt="Screenshot 2025-08-25 204339" src="https://github.com/user-attachments/assets/b98d12ec-7fcd-4d41-90d2-b48655a31f35" />





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
