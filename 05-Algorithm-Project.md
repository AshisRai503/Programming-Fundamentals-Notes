# E5 – Designing, Implementing and Testing an Algorithm (Course Project)

**Course:** Programming Fundamentals – Duke University (Coursera)
**Journal row:** 5 – Designing, implementing and testing an algorithm

## Project task
Design my own **sorting algorithm** using Steps 1–4 of the Seven Steps (design only, no code required).

> ✏️ Edit the steps below so they match the algorithm I actually came up with.

## Step 1 – Work an example by hand
Unsorted list: `[5, 2, 8, 1]`
By hand, I looked for the smallest number, put it first, then repeated the process with what was left:
`[1, 2, 8, 5]` → `[1, 2, 8, 5]` → `[1, 2, 5, 8]`

## Step 2 – Write down exactly what I did
1. Looked at all 4 numbers and found that 1 was the smallest.
2. Swapped 1 with the number in position 0 (the 5).
3. Looked at positions 1–3 and found that 2 was the smallest. It was already in place.
4. Looked at positions 2–3 and found that 5 was the smallest. Swapped it with the 8.
5. Only one number was left, so the list was sorted.

## Step 3 – Generalise
For each position `i` from 0 to n−2:
- Find the smallest value from position `i` to n−1.
- Swap it with the value at position `i`.

## Step 4 – Test by hand on new examples
| Test case | Input | Expected | Result |
| --- | --- | --- | --- |
| Normal | `[3, 1, 2]` | `[1, 2, 3]` | ✓ |
| Already sorted | `[1, 2, 3]` | `[1, 2, 3]` | ✓ |
| Reversed | `[4, 3, 2, 1]` | `[1, 2, 3, 4]` | ✓ |
| Duplicates | `[2, 1, 2]` | `[1, 2, 2]` | ✓ |
| One element | `[7]` | `[7]` | ✓ |
| Empty | `[]` | `[]` | ✓ |

## What I learned
- Working several examples made Step 3 much easier.
- Edge cases (empty list, duplicates) only came to mind because Step 4 made me test on purpose.

## Next steps (Weeks 9–12 plan)
- Translate this algorithm into C (Step 5).
- Write a test plan and debug it with GDB (Steps 6–7).
