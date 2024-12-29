# Lua Nested Table Iteration Bug

This repository demonstrates a subtle bug related to the unpredictable iteration order of Lua's `pairs` iterator when dealing with nested tables.  The bug arises because `pairs` does not guarantee a consistent order of key-value pairs, which can lead to unexpected behavior when processing nested structures.

The `bug.lua` file contains code that showcases this issue.  The `bugSolution.lua` file demonstrates how to mitigate this issue using a technique that provides predictable order.

## How to reproduce:

1. Clone the repository
2. Run `lua bug.lua`
3. Observe the output; it might vary due to the inconsistent iteration order.

## Solution:

The provided solution focuses on using a more deterministic method for iterating the nested table, thereby avoiding the unpredictability of `pairs`.  See `bugSolution.lua` for the solution and explanation.