# PRODIGGY_SD_04
Create a program that solves Sudokupuzzles automatically. The programshould take an input grid representingan unsolved Sudoku puzzle and use analgorithm to fill in the missing numbers.It should use backtracking or othersuitable techniques to explore possiblesolutions and find the correctarrangement of numbers for the puzzle.Once solved, the program shoulddisplay the completed Sudoku grid.
Creating a program to solve Sudoku puzzles involves several key steps and concepts:

### Input Grid
The program starts by taking an input grid representing an unsolved Sudoku puzzle. This grid is typically a 9x9 matrix where each cell contains a number from 1 to 9 or a placeholder (such as 0 or an empty space) for an empty cell.

### Solving Algorithm
The core of the program is the solving algorithm, which usually employs a technique called **backtracking**. Here's how backtracking works:

1. **Find an Empty Cell**: The algorithm searches the grid for the first empty cell (a cell with a placeholder).
2. **Try Possible Numbers**: For the empty cell, the algorithm tries each number from 1 to 9.
3. **Check Validity**: For each number, the algorithm checks if placing that number in the cell is valid. A number is valid if it:
   - Doesn't already exist in the same row.
   - Doesn't already exist in the same column.
   - Doesn't already exist in the same 3x3 subgrid.
4. **Place the Number**: If a number is valid, the algorithm places it in the cell and moves on to the next empty cell, repeating the process.
5. **Backtrack if Necessary**: If placing a number leads to a dead end (i.e., no valid numbers can be placed in subsequent empty cells), the algorithm removes the number (backtracks) and tries the next possible number for the previous empty cell.
6. **Continue Until Solved**: This process continues until the grid is completely filled with valid numbers, resulting in a solved puzzle.

### Displaying the Solution
Once the algorithm has filled in all the cells correctly, the program displays the completed Sudoku grid.

### Summary of Steps:
1. **Input Grid**: Read the unsolved Sudoku grid.
2. **Backtracking Algorithm**:
   - Find the first empty cell.
   - Try each number from 1 to 9.
   - Check if the number is valid in the current cell.
   - Place the valid number and move to the next empty cell.
   - If no valid number can be placed, backtrack to the previous cell.
   - Repeat until the grid is solved.
3. **Output Grid**: Display the completed Sudoku grid.

### Example
Imagine an unsolved Sudoku grid where some cells are filled with numbers and others are empty. The algorithm would:
- Start with the first empty cell.
- Try placing 1 in the cell, check if it's valid. If not, try 2, then 3, and so on.
- Once a valid number is placed, move to the next empty cell and repeat.
- If stuck, backtrack to the previous cell and try the next number.
- Continue this process until all cells are correctly filled.

By following these steps, the program systematically explores all possible configurations of numbers, ensuring that it finds a valid solution for the Sudoku puzzle.
