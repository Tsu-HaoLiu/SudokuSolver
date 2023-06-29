# SudokuSolver
### _The Simplest Sudoku Solver_

SudokuSolver can both solve and generate sudoku boards and is powered by Python.

- This program can easily solve difficult sudoku puzzles!
- It can also create some evil difficult puzzles for your friends to solve!


# How do I use this baby?!

```python
test_board = [
    [0, 3, 0, 0, 8, 0, 0, 0, 6],
    [2, 0, 0, 0, 0, 0, 7, 0, 3],
    [0, 7, 0, 0, 0, 0, 0, 0, 0],

    [0, 0, 1, 2, 0, 0, 0, 0, 0],
    [0, 5, 2, 8, 0, 0, 0, 0, 0],
    [0, 0, 0, 3, 6, 7, 0, 0, 0],

    [9, 0, 4, 0, 0, 0, 0, 5, 0],
    [0, 0, 0, 0, 9, 0, 2, 0, 0],
    [0, 0, 0, 0, 0, 6, 0, 8, 0]
]

sudoku = SudokuBoard()

# Add a sudoku board -> list[list]
sudoku.set_board(test_board)
sudoku.solve()

# You can also directly add the board and method to the class
sudoku = SudokuBoard(test_board)
sudoku_solved = sudoku.solve()
```
Printing the board: `print("board:", *sudoku_solved, sep="\n")`
```python
board:
[4, 3, 5, 7, 8, 2, 1, 9, 6]
[2, 9, 8, 6, 1, 5, 7, 4, 3]
[1, 7, 6, 9, 3, 4, 8, 2, 5]
[3, 6, 1, 2, 5, 9, 4, 7, 8]
[7, 5, 2, 8, 4, 1, 3, 6, 9]
[8, 4, 9, 3, 6, 7, 5, 1, 2]
[9, 8, 4, 1, 2, 3, 6, 5, 7]
[6, 1, 7, 5, 9, 8, 2, 3, 4]
[5, 2, 3, 4, 7, 6, 9, 8, 1]
```
### How do I generate a sudoku board?!?!?
```python
# It's quick and easy
sudoku = SudokuBoard()

# Difficulty `beginner` (default), `easy`, `medium`, `hard`, `extreme`
solved_board = sudoku.generate()
scrambled_board = sudoku.scrambled_board('medium')
```

## Development

Want to contribute or reivew my code? Great! I'm always looking for way to improve my code!

**Have Fun!**

