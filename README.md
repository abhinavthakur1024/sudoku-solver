# sudoku-solver
Sudoku solver
project DAA 

total boexes are 9
each grid has 9 box 

rules no number will be repet in any row , column , grid (3 * 3)

use recursion approach
(0,0) --> 1 to 9 

in this we use 4 method 
1> isSafe --> Once an empty cell is found, it tries to place numbers (1 to 9) in that cell, using the isSafe method to check for safety.
2> row check --> The number must not be present in the same row (r).
3> COlumn check --> The number must not be present in the same column (c).
4> Sub-grid Check --> The number must not be present in the 3x3 sub-grid


>If a number can be safely placed, it recursively calls solveSudoku for the next empty cell.
>If a solution is found, the method returns true.
>If no number can be safely placed, it backtracks by resetting the cell to 0 and tries the next number.
>the variable d is used as an index for iterating(repeat) over either the rows or columns of the Sudoku board.

for (int d = 0; d < board.length; d++) {  this check for row
    if (board[row][d] == num) {
        return false;
    }
}

for (int r = 0; r < board.length; r++) {  this check for column
            if (board[r][col] == num) {
                return false;
            }
        }

if num is present in row or col it return false

 int sqrt = (int) Math.sqrt(board.length);
        int boxRowStart = row - row % sqrt;
        int boxColStart = col - col % sqrt;
this sqrt will return the square root of number let number is 4 the square root of 4 is 2


