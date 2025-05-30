# Data-Lab

## Author
**Josh Forbes**

## Overview
This project is a solution set for the *Data Lab*, part of the Computer Systems course based on the textbook *Computer Systems: A Programmer's Perspective*. The lab focuses on bit-level manipulation of integers and floating-point numbers in C. Students are challenged to implement a series of functions using only a restricted set of operators and without using control constructs, macros, or function calls.

The goal is to deepen understanding of how data is represented and manipulated at the bit level in C, and to strengthen bitwise logic and debugging skills.

## File Description

- **`bits.c`**:  
  Contains all function implementations for the lab exercises. Each function must adhere to strict coding rules regarding allowed operations and coding style.
  
- **`README.md`** *(this file)*:  
  Provides context and overview of the lab, including rules and testing strategies.

## Coding Rules Summary

### Integer Coding Rules:
You may only use:
- Integer constants from 0 to 255 (0xFF)
- Function arguments and local variables
- Unary operations: `!`, `~`
- Binary operations: `&`, `^`, `|`, `+`, `<<`, `>>`

You **may not**:
- Use any control constructs (`if`, `while`, `for`, `switch`, etc.)
- Define or use macros or helper functions
- Use other operations such as `-`, `&&`, `||`, `?:`
- Use any data types besides `int` (no `float`, `double`, `struct`, etc.)

### Floating-Point Rules:
You **may** use:
- Control constructs (`if`, `while`, etc.)
- Both `int` and `unsigned` data types
- Any operations on integers and unsigneds

You **may not**:
- Use floating-point data types, constants, or operations
- Define or call any functions
- Use casting or macros

## Tools for Verification

- **`dlc` (Data Lab Checker)**:  
  Use to ensure your functions comply with the legal operator rules.

- **`btest` (Bit-level Test Harness)**:  
  Use to run correctness tests against your function implementations.

- **`BDD Checker`**:  
  Optional tool to formally verify logical equivalence between your solution and a reference implementation.

## Examples

```c
/*
 * bitOr - x | y using only ~ and &
 */
int bitOr(int x, int y) {
  return ~(~x & ~y);
}

##How to Run

1. Compile with make or use provided build script.
2. Run tests:
~~~~~~~~~~~~~~~~~~~~~~~~~~
./btest
~~~~~~~~~~~~~~~~~~~~~~~~~~
3. Verify operator legality:
~~~~~~~~~~~~~~~~~~~~~~~~~~
./dlc bits.c
~~~~~~~~~~~~~~~~~~~~~~~~~~

##License
This project follows the GNU Lesser General Public License v2.1 or later, as noted in the source headers.
