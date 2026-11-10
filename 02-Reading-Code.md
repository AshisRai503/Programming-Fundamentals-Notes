# E2 – Reading Code (Executing Code by Hand)

**Course:** Programming Fundamentals – Duke University (Coursera)
**Journal row:** 2 – Reading Code

## Why it matters
If I can't predict what code does, I can't write it or debug it. Tracing by hand shows *why* a program gives a certain output, so I don't have to guess.

## The tracing method
- **Frame:** a box for each function call (starts with `main`)
- **Variable box:** a box inside the frame for each variable, holding its current value
- **Execution arrow:** points to the line currently running and moves one line at a time
- When a value changes, cross out the old value and write the new one.

## Expressions
- Evaluated by operator precedence: `*`, `/`, `%` come before `+`, `-`
- Parentheses override precedence.

## Assignment statements
`x = expression;`
1. Work out the value on the **right** side.
2. Store it in the box on the **left** side.

`x = x + 1;` is **not** maths. It means "take the old x, add 1, store it back".

## Integer division and modulus
| Expression | Result | Why |
| --- | --- | --- |
| `7 / 2` | `3` | int / int drops the fraction |
| `7.0 / 2` | `3.5` | one operand is floating point |
| `7 % 2` | `1` | remainder |
| `10 % 5` | `0` | divides evenly |

Common uses of `%`: checking even/odd (`n % 2 == 0`) and getting the last digit (`n % 10`).

## Checking my trace
After tracing by hand, I run the actual program and compare the output. If they're different, I made a tracing mistake. Find the line where it went wrong and learn from it.

## Practice example
```c
int main(void) {
  int a = 5;
  int b = a / 2;   // b = 2
  a = a % 2 + b;   // a = 1 + 2 = 3
  printf("%d %d\n", a, b);  // prints: 3 2
  return 0;
}
```
