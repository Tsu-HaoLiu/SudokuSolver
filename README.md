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

sudoku = SudokuCore()

# Add a sudoku board -> list[list]
sudoku.addboard(test_board)

# Set the method (currently only 2)
sudoku.setmethod("sorted_recursion") # recursion, sorted_recursion
sudoku_solved = sudoku.solve()


# You can also directly add the board and method to the class
sudoku = SudokuCore(test_board, "recursion")
sudoku_solved = sudoku.solved_board
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
sudoku = SudokuCore()

# Difficulty `beginner` (default), `easy`, `medium`, `hard`, `extreme`
unsolved_board = sudoku.generate("medium")

# You can also get the solved board :O
solved_board = sudoku.solved_board
```
### I am speeeeed
If you are looking for speed I recommend using the `sorted_recursion` method to solve your sudoku boards faster. This is because it is first pre-scanning all positions and possible numbers on the board, instead of going through all possible combinations like in `recursion`. (Times are dependent on difficulty and how fast your computer can process)
**Here are some stats after ~50 solves:**
> recursion avg: 20.5283s
> 
> sorted_recursion avg: 7.2337s

## Development

Want to contribute or reivew my code? Great! I'm always looking for way to improve my code!


## License

[MIT License](https://github.com/Tsu-HaoLiu/SudokuSolver/blob/main/LICENSE)

**Have Fun!**

