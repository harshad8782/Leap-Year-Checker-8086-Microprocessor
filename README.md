# Leap Year Checker – 8086 Assembly Language Project

This project demonstrates a simple **8086 microprocessor** program written in **Assembly Language** using **TASM** to determine whether a given year is a **leap year** or not.

---

## 📌 Project Overview

A leap year has 366 days instead of 365, with an extra day added to February (Feb 29). This Assembly program takes a year as input and checks whether it's a leap year based on the standard rules:
- Divisible by 4  
- Not divisible by 100 unless divisible by 400

---

## 🎯 Objective

To build a microprocessor-based solution that:
- Accepts a year as input.
- Uses basic arithmetic and conditional logic to check leap year status.
- Displays the appropriate result.

---

## ⚙️ Technologies Used

- **8086 Assembly Language**
- **TASM 1.7 (Turbo Assembler)**
- **DOS Interrupts (INT 21H)**
- **Windows 10 for execution**

---

## 🧑‍💻 Team Members

- Harshad Raurale  
- Kaushik Shigavan  
- Shrey Raut  

---

## 📥 Input Format

The user is prompted to enter a year. Input must be a 2-digit or 4-digit number using keyboard input.

---

## 💻 Sample Code Snippet

```asm
LEA DX,MSG  
MOV AH,09H  
INT 21H     ; Display message

LEA DX,NUMBER  
MOV AH,0AH  
INT 21H     ; Accept user input

AAD         ; Convert ASCII to binary
MOV BL,04H  
DIV BL      ; Check divisibility by 4
JZ YES      ; If zero remainder, it's a leap year
```

---

✅ Output
Displays either:

YES, IT IS A LEAP YEAR

NO, IT IS NOT A LEAP YEAR
