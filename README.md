## Brute-Force Backtracking Approach

In this approach the first step is to find an empty Sudoku cell and fill it with a digit from one to nine. The algorithm verifies which digits are safe to use whenever it finds an empty
cell; if a digit is already present in that cell’s row, column, or square, it will not be inserted. Once a digit has been placed, the algorithm will use recursion to run the solving function
again, this time finding the next empty cell and repeating the process until there are no empty cells, the problem has been solved. If a cell cannot be filled with a number, the algorithm will return to the previous cell and change the digit to another
valid option, a process known as backtracking.

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/8/8c/Sudoku_solved_by_bactracking.gif" alt="animated" />
</p>

## CSP Approach with backtracking

When approaching Sudoku solving as a CSP it’s required to
define and identify the problem’s components. The components
include the variables, the domain and the problem’s constraints.

* Variables = {Cell1 . . . Cell81}. 
* Domain = {1, 2, 3, 4, 5, 6, 7, 8, 9
* Constraint 1 = {Rows must have unique values}
* Constraint 2 = {Columns must have unique values}
* Constraint 3 = {Squares must have unique values}

The main objective of this approach is to reduce the search
space of the problem before we implement recursion and
backtracking. The first step is to attribute to each cell in
the Sudoku a list of its peers, a cell’s peers are the cells
present in the corresponding row, column and square. This will
greatly improve the search time when the algorithm needs to
check if a digit is already present on that cell’s peers. The
second step consists in filling every single empty cell with all
the digits in the domain, which are digits from one to nine,
shown in the next figure.

<p align="center" width="100%">
    <img width="50%" src="https://user-images.githubusercontent.com/70576587/150957524-1e97744a-2a5c-4bb4-8ba2-4496407006a7.png"> 
</p>
