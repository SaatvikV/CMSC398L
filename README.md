# CMSC398L

The Sudoku Solver problem gives a sudoku board as input and requires the user to output the completed board. Sudoku is a number-placement puzzle where the objective is to fill a 9×9 grid with digits from 1 to 9, such that each column, each row, and each of the nine 3×3 subgrids that compose the grid contain all of the digits from 1 to 9. The problem is shown below.

![image](https://github.com/SaatvikV/CMSC398L/assets/33701797/d6493052-3d98-42c8-9f34-074e99c54569)


I chose this problem as I really enjoy solving sudoku and wanted to discuss the solution for this. My solution for this problem is shown below.

![image](https://github.com/SaatvikV/CMSC398L/assets/33701797/64863f61-8076-497c-a646-68c8038f796e)


Let us walk through the solution. We employ a backtracking solution. The check function checks our current row and column for a duplicate value. We do this to ensure we are allowed to place the number in that spot and there is no duplicate number in our row and column and our current box. The solveSudoku function utilizes recursive backtracking to fill out the grid. We iterate through each cell in the grid and if the cell is empty, it tries placing each digit from '1' to '9' and recursively calls itself for the next cell. If a placement is valid and leads to a solution, it returns true. If no valid placement is found, it backtracks by setting the cell back to '.', indicating that the current placement is not correct. This is done recursively until we fill out the board. The original call is at the start of the grid.

The time complexity of this solution is O(9(n*n)) where n represents the number of empty squares.

The space complexity is O(n^2) represented by the sudoku board.
