# E3 – Functions, Conditional Statements and Loops

**Course:** Programming Fundamentals – Duke University (Coursera)
**Journal row:** 3 – Functions, conditional statements and loops

## Functions
```c
int square(int x) {   // return type, name, parameter
  return x * x;
}
```
- **Calling a function creates a new frame** with a box for each parameter.
- **Pass by value:** the argument's *value* is copied into the parameter. Changing the parameter inside the function does **not** change the caller's variable.
- **return:** works out the value, destroys the frame, and sends the value back to **the place where the function was called**.
- When tracing, mark the call site so you know where to return to.

## Conditional statements
### if / else
```c
if (x > 0) {
  printf("positive\n");
} else if (x < 0) {
  printf("negative\n");
} else {
  printf("zero\n");
}
```
### switch / case
```c
switch (day) {
  case 1:  printf("Mon\n"); break;
  case 2:  printf("Tue\n"); break;
  default: printf("Other\n");
}
```
- Without `break`, execution **falls through** to the next case.

## Loops
| Loop | Checks the condition | Use when |
| --- | --- | --- |
| `while` | before each pass (may run 0 times) | the number of passes is unknown |
| `do { } while ( );` | after each pass (runs at least once) | it must run once, e.g. input checking |
| `for (init; cond; update)` | before each pass | counting a known number of times |

```c
for (int i = 0; i < 5; i++) {
  printf("%d ", i);   // 0 1 2 3 4
}
```

## break and continue
- `break` exits the nearest loop (or switch) immediately.
- `continue` skips the rest of this pass and moves on to the next one.

## Scope
- A variable exists only inside the `{ }` block where it was declared.
- A variable declared in a `for` header exists only inside that loop.
- Variables in different functions are separate, even if they share a name.

## Nested loops: tracing tip
The inner loop finishes **all** of its passes for **each** pass of the outer loop. Keep a separate box for each loop variable and update them carefully.

## Outcome
I traced course exercises that use nested loops and several function calls.
