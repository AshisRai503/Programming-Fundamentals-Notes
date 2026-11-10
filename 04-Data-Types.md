# E4 – Data Types and Number Representation

**Course:** Programming Fundamentals – Duke University (Coursera)
**Journal row:** 4 – Data types and number representation

## Everything is bits
Computers store everything as **binary** (0s and 1s). The **type** tells the computer how to read those bits.

## Number systems
| Decimal | Binary | Hex |
| --- | --- | --- |
| 0 | 0000 | 0x0 |
| 5 | 0101 | 0x5 |
| 9 | 1001 | 0x9 |
| 10 | 1010 | 0xA |
| 15 | 1111 | 0xF |
| 255 | 1111 1111 | 0xFF |

- **Binary → decimal:** add up the place values: `1011` = 8 + 0 + 2 + 1 = **11**
- **Decimal → binary:** divide by 2 again and again, then read the remainders from bottom to top
- **Binary ↔ hex:** each hex digit = 4 bits. `1010 1111` → `A F` → **0xAF**

## Common C types (typical sizes)
| Type | Typical size | Holds |
| --- | --- | --- |
| `char` | 1 byte | one character / small integer |
| `int` | 4 bytes | about −2.1 billion to +2.1 billion |
| `float` | 4 bytes | decimal number, about 7 digits of precision |
| `double` | 8 bytes | decimal number, about 15–16 digits of precision |

Use `sizeof(type)` to check the size on your own machine.

## Characters and ASCII
A `char` is stored as a number:
- `'A'` = 65, `'a'` = 97, `'0'` = 48
- `'a' - 'A'` = 32 (the gap between lower case and upper case)
- `'7' - '0'` = 7 (turns a digit character into its number)

## Floating-point precision
Many decimals (such as 0.1) cannot be stored exactly in binary, so `0.1 + 0.2` is not exactly `0.3`. **Don't compare floats with `==`.** Check whether they are close enough instead.

## Overflow
A type can only hold so many values. Going past the limit causes **overflow**:
- **Unsigned** integers wrap around (max + 1 → 0).
- **Signed** integer overflow is undefined behaviour in C. Avoid it.

## Type conversion
- Mixing `int` and `double` in an expression turns the int into a double.
- Casting: `(double) 7 / 2` → `3.5`
- Assigning a double to an int **drops the fraction**: `int x = 3.9;` → `3`

## Custom types
```c
struct point {        // groups related data
  int x;
  int y;
};
typedef struct point point_t;   // gives the type a shorter name

enum colour { RED, GREEN, BLUE };  // named constants: 0, 1, 2

point_t p;
p.x = 3;
p.y = 4;
```
