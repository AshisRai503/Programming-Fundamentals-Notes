# E1 – The Seven Steps for Programming

**Course:** Programming Fundamentals – Duke University (Coursera)
**Journal row:** 1 – Seven Steps for Programming

## Key idea
Writing code is the *last* part of programming. The hard part is working out the **algorithm**, a clear set of steps that solves the problem. You design it first and translate it into code afterwards.

## The Seven Steps

| Step | Name | What I do |
| --- | --- | --- |
| 1 | Work an example yourself | Solve one small case of the problem by hand, on paper. |
| 2 | Write down exactly what you did | Record every step precisely, even the "obvious" ones. |
| 3 | Generalise your steps | Find the patterns and replace specific numbers with variables, and repeated actions with loops. |
| 4 | Test your algorithm | Run the general steps by hand on a *different* example. |
| 5 | Translate to code | Turn each step into C statements. |
| 6 | Run test cases | Run the program on many inputs, including edge cases. |
| 7 | Debug | Use the scientific method: observe, make a hypothesis, test, fix. |

- **Steps 1–4 = design** (no computer needed)
- **Steps 5–7 = implementation and testing**

## If I get stuck in Step 1
That usually means I don't fully understand the problem, or I'm missing domain knowledge (for example the maths behind it). I need to fix that before going further.

## Tips for Step 3 (my weak point)
- Look for **repetition**, which usually becomes a loop.
- Look for **decisions**, which usually become if/else.
- Ask "where did this number come from?" Usually it comes from the input or a previous step.
- Work **more than one example** in Step 1 so the patterns are easier to see.

## Example: number sequence problem
Sequence: `1, 4, 7, 10, ...` → find the n-th term.
1. By hand: term 0 = 1, term 1 = 4, term 2 = 7
2. Written down: each term adds 3 to the previous one
3. Generalised: `term(n) = 1 + 3 × n`
4. Tested: n = 3 → 1 + 9 = 10 ✓

## Example: graphical pattern problem
Given n, print a pattern of `*`. Draw the grid for n = 3 and n = 4, then look at which (row, column) cells are filled. Write that as a condition such as `if (col <= row)`, wrapped in two nested loops.

## Outcome
I now plan my algorithm on paper before writing any code.
