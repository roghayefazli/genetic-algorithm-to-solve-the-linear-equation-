# genetic-algorithm-to-solve-the-linear-equation-

### genetic_moadele.ipynb

This Jupyter Notebook file contains a Python script that uses a genetic algorithm to solve the linear equation:

$$a + 2b + 3c + 4d = 30$$

The script aims to find the values for variables `a`, `b`, `c`, and `d` that minimize the absolute difference between the left-hand side of the equation and the target value of 30.

#### How it works

The code implements the following steps of a genetic algorithm:

1.  **Fitness Function:** The `fitness_function` measures how close a solution is to the target. It calculates the absolute difference: $|a + 2b + 3c + 4d - 30|$. The goal is to find a solution with a fitness score as close to zero as possible.
2.  **Initial Population:** The `create_population` function generates a random initial set of individuals (solutions), where each individual is a list of four numbers representing `a`, `b`, `c`, and `d`.
3.  **Parent Selection:** The `select_parents` function randomly selects two individuals from the current population to serve as parents for the next generation.
4.  **Crossover:** The `crossover` function combines the genetic material of two parents to create a new offspring. It uses a single crossover point to mix and match the values from the parents.
5.  **Mutation:** The `mutate` function introduces random changes to the offspring's values to maintain genetic diversity and prevent the algorithm from getting stuck in a local optimum. The mutation rate is set to 10%.
6.  **Evolution Loop:** The script runs for a set number of `generations`. In each generation, it creates a new population by selecting parents, performing crossover, and mutating the resulting children. The new population then replaces the old one.
7.  **Best Solution:** After all generations have run, the script identifies the individual in the final population with the lowest fitness score (i.e., the one closest to solving the equation) and prints the values of `a`, `b`, `c`, and `d`.

#### Requirements

This script only requires the standard Python `random` library, so no special installation is needed.

#### How to run

1.  Open the `genetic_moadele.ipynb` file in a Jupyter Notebook environment (e.g., JupyterLab, Google Colab, or Visual Studio Code with the Jupyter extension).
2.  Run the cells sequentially. The final cell will execute the genetic algorithm and print the best solution it found.
