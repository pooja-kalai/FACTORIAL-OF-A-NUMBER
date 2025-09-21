# FACTORIAL-OF-A-NUMBER
# FACTORIAL OF A NUMBER USING 8051 (Keil)

## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.

---

## APPARATUS REQUIRED
- Personal computer with Keil software

---

## ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
3. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
4. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
5. **Output**: Store or print the value of factorial.
6. **End**

---

## FLOWCHART
<img width="506" height="525" alt="image" src="https://github.com/user-attachments/assets/f3b47187-6f0f-490c-8704-f2973cb2b276" />


---

## PROGRAM
```asm
ORG 0000H
MOV DPTR,#4500H
MOVX A,@DPTR
MOV R0,A
INC DPTR
ACALL FACTORIAL
MOVX @DPTR,A
SJMP THIN
FACTORIAL:DEC R0
CJNE R0,#01H,PRODUCT
SJMP THICK
PRODUCT:MOV B,R0
MUL AB
ACALL FACTORIAL
THICK: RET
THIN:RET
END

```
OUTPUT
<img width="940" height="667" alt="image" src="https://github.com/user-attachments/assets/01da5fea-9f7b-4cd0-b171-3c98ecf86e55" />
<img width="943" height="497" alt="image" src="https://github.com/user-attachments/assets/2ea6dc7a-98e1-4a94-934a-8be042231294" />
---
MANUAL CALCULATIONS
<img width="624" height="939" alt="image" src="https://github.com/user-attachments/assets/2384604c-7c3d-4d4d-a97a-3ff2af9f5510" />

RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---


