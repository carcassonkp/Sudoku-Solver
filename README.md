## Brute-Force Backtracking Approach

In this approach the first step is to find an empty Sudoku cell and fill it with a digit from one to nine. The algorithm verifies which digits are safe to use whenever it finds an empty
cell; if a digit is already present in that cell’s row, column, or square, it will not be inserted. Once a digit has been placed, the algorithm will use recursion to run the solving function
again, this time finding the next empty cell and repeating the process until there are no empty cells, the problem has been solved. If a cell cannot be filled with a number, the algorithm will return to the previous cell and change the digit to another
valid option, a process known as backtracking.

![Alt Text](https://upload.wikimedia.org/wikipedia/commons/8/8c/Sudoku_solved_by_bactracking.gif)
