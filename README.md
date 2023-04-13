## SudukoSolver

The SudukoSolver is a command-line tool that can solve a Suduko puzzle using a simple algorithm that involves filling in the blanks one by one until the entire puzzle is filled.

# Requirements

To use the SudukoSolver, you need to have Ruby installed on your computer. The program has been tested on Ruby 3.1.2#

# Usage

To use the SudukoSolver, you need to create a Suduko puzzle in the form of a 9x9 array of integers, where blank cells are represented by the number 0. For example:

```
board = [
  [0, 0, 0, 0, 0, 0, 0, 3, 0],
  [7, 5, 0, 0, 8, 4, 0, 9, 6],
  [2, 0, 0, 0, 0, 6, 0, 0, 5],
  [0, 0, 4, 0, 0, 8, 0, 6, 0],
  [0, 0, 2, 4, 1, 5, 0, 7, 0],
  [0, 0, 5, 7, 0, 0, 0, 0, 0],
  [5, 3, 1, 6, 7, 0, 0, 0, 4],
  [6, 0, 9, 0, 3, 0, 2, 5, 7],
  [8, 0, 0, 5, 4, 9, 6, 0, 3]
]
```

Once you have created the puzzle, you can create an instance of the SudukoPuzzle class and pass the puzzle to the constructor:

`puzzle = SudukoPuzzle.new(board)`

You can then call the solve! method on the puzzle object to solve the puzzle:

`puzzle.solve!`
After the solve! method has finished running, the board attribute of the puzzle object will contain the solved puzzle:

`pp puzzle.board`

To see the solution in your terminal, run the following command

`ruby main.rb`

# Algorithm

The SudukoSolver algorithm is a simple one that involves filling in the blanks one by one until the entire puzzle is filled. The algorithm works by iterating over each cell in the puzzle, and for each blank cell, filling in a value that is not already present in the same row, column, or 3x3 box.

The algorithm repeats this process for each blank cell in the puzzle until all cells are filled. If at any point the algorithm reaches a cell with no valid values, it backtracks to the previous cell and tries a different value.

# Conclusion

The SudukoSolver is a simple yet effective tool for solving Suduko puzzles. It uses a straightforward algorithm to fill in the blanks one by one, and can solve most puzzles in a matter of seconds.
