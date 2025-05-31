# Simple Calculator in C

This project is a simple command-line calculator implemented in C.

## Files

- `main.c`: Entry point. Just calls `Calculator()` function.
- `calculator.c`: Handles calculator logic and user input.
- `calculator.h`: Declares the prototype for the `Calculator()` function.
---

## How to Compile

Use the following command to compile:

```bash
gcc main.c calculator.c -o simple-c-calculator
```
---

## Important Notes (Environment)

This program uses  `scanf_s` , which is specific to
**Windows environments such as Visual Studio 2022**.
Compiling with GCC or Clang will result in errors,
as  `scanf_s`  is not supported in those environments.

---

## Building on Other Environments

If you are using GCC, Clang, or another non-Visual Studio environment,
you will need to replace  `scanf_s`  with the standard  `scanf` .

Examples:

```c

// For numeric input (e.g., double)
scanf_s("%lf", num);    // Visual Studio
↓
scanf("%lf", num);      // Standard C

// For character input with buffer handling
sscanf_s(buffer, "%c", symbol, 1);
↓
sscanf(buffer, "%c", symbol);

```

---

## How to Run

```
./simple-c-calculator
```

---

## Features

- Supports basic arithmetic operations (+, -, *, /)
- Handles invalid input with error messages
- Includes loop with y/n confirmation to continue
 
---

## Notes

- This project was created for learning purposes.
- There are no planned updates.

---

[Click here for the Japanese README](README.ja.md)