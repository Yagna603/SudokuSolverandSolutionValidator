# SudokuSolverandSolutionValidator

**Flowchart**

   **Basic Ideology**
The hint was to use the concept of multi-threading. We decided to use 27 threads for creating the validator. 9 threads were used to check the 9 rows, the other 9 threads to check 9 columns and the remaining 9 were used to check the subgrids (grids of 3 x 3).
                                                ↓
**Benefit of Multi-threading**
The benefit of using Multi-threading technique is that we can simultaneously check the validation of rows, columns and subgrids.
                                                ↓
**Integrating the threads**
We maintained a global array, accessible to all the threads. Every thread would return a value (0 or 1) to the global array, depicting whether that particular row, column or subgrid is valid or not. The task becomes easy now, since a thread checks only for a single occurrence of all the numbers from 1 to 9.
The Sudoku validator part completes here. But that was not all.
                                                ↓
**The new idea of “Solver”**
We thought about adding more features to our program and hence decided to include a ‘Solver'. The Sudoku Solver takes input in form of an unsolved Sudoku 
(we denoted blank spaces with ‘0’), it then solves the Sudoku. The program then validates the Sudoku solution and then gives output as solved Sudoku.
                                                ↓
**Yet another Idea!!**
Then an idea came through about developing such a mechanism, through which the user can solve a sudoku in step by step manner.
                                                ↓
**Implementing the new Idea!!**
What we did to implement this was that we took an unsolved sudoku as input. Then asked the user, that how many values would he/she like to fill 
(which are empty/blank until now). The values along with the positions where they are to be put were taken as input.
                                                ↓
**Checking and providing the user a choice**
Then we checked whether the inputs given by the user lead to a valid solution or not. If it did, we gave the user a choice to continue filling the sudoku 
(the updated sudoku after taking input values). If the input values did not lead to a valid solution, we prompted the user that there is a mistake somewhere. We did not update the sudoku this time but did gave the user a choice to keep trying.
