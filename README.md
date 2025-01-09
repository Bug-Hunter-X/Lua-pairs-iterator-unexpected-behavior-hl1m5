# Lua pairs iterator unexpected behavior
This repository demonstrates a potential issue with Lua's `pairs` iterator when used with tables that are modified during iteration.  The `bug.lua` file contains code that showcases this issue, while `bugSolution.lua` offers a solution.

## Problem
Lua's `pairs` iterator does not guarantee a specific order of iteration.  When a table is modified during iteration (e.g., elements are added or removed), the behavior can be unpredictable and might result in elements being skipped or an infinite loop.

## Solution
The solution involves iterating over a copy of the table's keys, ensuring that modifications to the original table during iteration do not affect the iteration process.