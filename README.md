# CI2024_lab1

## Proposed algorithms:
- ### First dumb solutions --> the second one could be invalid
- ### Hill Climbing - Single random mutation
- ### Hill Climbing - Multiple random mutations
- ### Hill Climbing - Steepest Step and Restart
- ### Simulated Annealing
- ### Tabu Search

## All three Hill Climbing algorithms:
- Using fitness1 and startingpoint1 --> with fitness1, we have to start from a valid solution
- Using fitness2 and startingpoint2 --> we can also starting from an invalid solution (we are not attracted from all falses state)

## Furthermore:
- _tweak3_ is an improved tweak function related to multiple random mutations w.r.t. _tweak2_

## Observations:
- USING fitness2 is relevant to show the behaviour with both first and second criterion of fitness (i.e. #of covered items and -cost)
- with fitness1, we have to start necessarily from a valid solution
- using fitness2, we can also starting from an invalid solution (we are not attracted from all-falses state)
- choosing a low number of iterations could lead to an invalid solution even though the algorithm is correct and it would work properly with more iterations. (example fitness2, startingpoint2 and 100 iteration doesn't work in the steepest step and restart)
- in the Simulated Annealing a penalty was added for solution of invalid region in order to jump into the valid one

## TO DO:
- review the False (invalid) solution
- try if possible to create an initial index in the notebook, so that everything is more clear
- complete this README.md 


## Instances and results 
In the following, results about the 6 instances.

## Instance 1

| Algorithm                                                                        | Universe Size | Number of Sets | Density | Valid Solution | Cost                |
|----------------------------------------------------------------------------------|---------------|----------------|---------|----------------|---------------------|
| First Dumb Solution                                                              | 100           | 10             | 0.2     | True           | 274.78  |
| Second Dumb Solution                                                             | 100           | 10             | 0.2     | False          | 42.27   |
| Hill Climbing - Single Random Mutation - First Fitness and Starting Point        | 100           | 10             | 0.2     | True           | 246.41  |
| Hill Climbing - Single Random Mutation - Second Fitness and Starting Point       | 100           | 10             | 0.2     | True           | 282.26   |
| Hill Climbing - Multiple Random Mutations - First Fitness and Starting Point     | 100           | 10             | 0.2     | True           | 272.01   |
| Hill Climbing - Multiple Random Mutations - Second Fitness and Starting Point    | 100           | 10             | 0.2     | True           | 277.54   |
| Hill Climbing - Multiple Random Mutations with an Improved Tweak Function        | 100           | 10             | 0.2     | True           | 286.69  |
| Hill Climbing - Steepest Step and Restart - First Fitness and Starting Point     | 100           | 10             | 0.2     | True           | 290.88  |
| Hill Climbing - Steepest Step and Restart - Second Fitness and Starting Point    | 100           | 10             | 0.2     | True           | 280.63   |
| Simulated Annealing                                                              | 100           | 10             | 0.2     | True           | 304.63  |
| Tabu Search                                                                      | 100           | 10             | 0.2     | True           | 298.916  |

## Instance 2

| Algorithm                                                                        | Universe Size | Number of Sets | Density | Valid Solution | Cost                |
|----------------------------------------------------------------------------------|---------------|----------------|---------|----------------|---------------------|
| First Dumb Solution                                                              | 1000          | 100            | 0.2     | True           | 34058.58   |
| Second Dumb Solution                                                             | 1000          | 100            | 0.2     | False          | 16507.06  |
| Hill Climbing - Single Random Mutation - First Fitness and Starting Point        | 1000          | 100            | 0.2     | True           | 8440.79   |
| Hill Climbing - Single Random Mutation - Second Fitness and Starting Point       | 1000          | 100            | 0.2     | True           | 7079.99   |
| Hill Climbing - Multiple Random Mutations - First Fitness and Starting Point     | 1000          | 100            | 0.2     | True           | 9328.06   |
| Hill Climbing - Multiple Random Mutations - Second Fitness and Starting Point    | 1000          | 100            | 0.2     | True           | 7225.87   |
| Hill Climbing - Multiple Random Mutations with an Improved Tweak Function        | 1000          | 100            | 0.2     | True           | 7204.84   |
| Hill Climbing - Steepest Step and Restart - First Fitness and Starting Point     | 1000          | 100            | 0.2     | True           | 24548.61  |
| Hill Climbing - Steepest Step and Restart - Second Fitness and Starting Point    | 1000          | 100            | 0.2     | True           | 8300.12  |
| Simulated Annealing                                                              | 1000          | 100            | 0.2     | True           | 8939.52   |
| Tabu Search                                                                      | 1000          | 100            | 0.2     | True           | 7409.74   |

## Instance 3

| Algorithm                                                                        | Universe Size | Number of Sets | Density | Valid Solution | Cost                |
|----------------------------------------------------------------------------------|---------------|----------------|---------|----------------|---------------------|
| First Dumb Solution                                                              | 10000         | 1000           | 0.2     | True           | 4276759.90   |
| Second Dumb Solution                                                             | 10000         | 1000           | 0.2     | True           | 2125601.67  |
| Hill Climbing - Single Random Mutation - First Fitness and Starting Point        | 10000         | 1000           | 0.2     | True           | 3675620.54 |
| Hill Climbing - Single Random Mutation - Second Fitness and Starting Point       | 10000         | 1000           | 0.2     | True           | 153908.03    |
| Hill Climbing - Multiple Random Mutations - First Fitness and Starting Point     | 10000         | 1000           | 0.2     | True           | 3382625.12  |
| Hill Climbing - Multiple Random Mutations - Second Fitness and Starting Point    | 10000         | 1000           | 0.2     | True           | 150473.54  |
| Hill Climbing - Multiple Random Mutations with an Improved Tweak Function        | 10000         | 1000           | 0.2     | True           | 144863.93  |
| Hill Climbing - Steepest Step and Restart - First Fitness and Starting Point     | 10000         | 1000           | 0.2     | True           | 4133214.99  |
| Hill Climbing - Steepest Step and Restart - Second Fitness and Starting Point    | 10000         | 1000           | 0.2     | False          | 149179.79   |
| Simulated Annealing                                                              | 10000         | 1000           | 0.2     | True           | 188292.79  |
| Tabu Search                                                                      | 10000         | 1000           | 0.2     | True           | 140375.03  |

## Instance 4

| Algorithm                                                                        | Universe Size | Number of Sets | Density | Valid Solution | Cost                |
|----------------------------------------------------------------------------------|---------------|----------------|---------|----------------|---------------------|
| First Dumb Solution                                                              | 100000        | 10000          | 0.1     | True           | 251202344.48        |
| Second Dumb Solution                                                             | 100000        | 10000          | 0.1     | True           | 125318561.50        |
| Hill Climbing - Single Random Mutation - First Fitness and Starting Point        | 100000        | 10000          | 0.1     | True           | 247426765.10        |
| Hill Climbing - Single Random Mutation - Second Fitness and Starting Point       | 100000        | 10000          | 0.1     | True           | 2513309.97          |
| Hill Climbing - Multiple Random Mutations - First Fitness and Starting Point     | 100000        | 10000          | 0.1     | True           | 244692971.71        |
| Hill Climbing - Multiple Random Mutations - Second Fitness and Starting Point    | 100000        | 10000          | 0.1     | True           | 2610265.54          |
| Hill Climbing - Multiple Random Mutations with an Improved Tweak Function        | 100000        | 10000          | 0.1     | True           | 2136383.55          |
| Hill Climbing - Steepest Step and Restart - First Fitness and Starting Point     | 100000        | 10000          | 0.1     | True           | 250402732.67        |
| Hill Climbing - Steepest Step and Restart - Second Fitness and Starting Point    | 100000        | 10000          | 0.1     | False          | 1056157.18          |
| Simulated Annealing                                                              | 100000        | 10000          | 0.1     | True           | 2560923.80          |
| Tabu Search                                                                      | 100000        | 10000          | 0.1     | True           | 2206767.96          |

## Instance 5

| Algorithm                                                                        | Universe Size | Number of Sets | Density | Valid Solution | Cost                |
|----------------------------------------------------------------------------------|---------------|----------------|---------|----------------|---------------------|
| First Dumb Solution                                                              | 100000        | 10000          | 0.2     | True           | 538427563.95        |
| Second Dumb Solution                                                             | 100000        | 10000          | 0.2     | True           | 271893574.39        |
| Hill Climbing - Single Random Mutation - First Fitness and Starting Point        | 100000        | 10000          | 0.2     | True           | 530259286.02        |
| Hill Climbing - Single Random Mutation - Second Fitness and Starting Point       | 100000        | 10000          | 0.2     | True           | 2636473.07          |
| Hill Climbing - Multiple Random Mutations - First Fitness and Starting Point     | 100000        | 10000          | 0.2     | True           | 525089092.09        |
| Hill Climbing - Multiple Random Mutations - Second Fitness and Starting Point    | 100000        | 10000          | 0.2     | True           | 2693209.22          |
| Hill Climbing - Multiple Random Mutations with an Improved Tweak Function        | 100000        | 10000          | 0.2     | True           | 2102501.43          |
| Hill Climbing - Steepest Step and Restart - First Fitness and Starting Point     | 100000        | 10000          | 0.2     | True           | 536561979.63        |
| Hill Climbing - Steepest Step and Restart - Second Fitness and Starting Point    | 100000        | 10000          | 0.2     | True           | 2474777.08          |
| Simulated Annealing                                                              | 100000        | 10000          | 0.2     | True           | 2959940.07          |
| Tabu Search                                                                      | 100000        | 10000          | 0.2     | True           | 2310619.51          |

## Instance 6

| Algorithm                                                                        | Universe Size | Number of Sets | Density | Valid Solution | Cost                |
|----------------------------------------------------------------------------------|---------------|----------------|---------|----------------|---------------------|
| First Dumb Solution                                                              | 100000        | 10000          | 0.3     | True           | 841067324.91        |
| Second Dumb Solution                                                             | 100000        | 10000          | 0.3     | True           | 413962179.16        |
| Hill Climbing - Single Random Mutation - First Fitness and Starting Point        | 100000        | 10000          | 0.3     | True           | 828574227.45        |
| Hill Climbing - Single Random Mutation - Second Fitness and Starting Point       | 100000        | 10000          | 0.3     | True           | 2691074.05          |
| Hill Climbing - Multiple Random Mutations - First Fitness and Starting Point     | 100000        | 10000          | 0.3     | True           | 819965376.99        |
| Hill Climbing - Multiple Random Mutations - Second Fitness and Starting Point    | 100000        | 10000          | 0.3     | True           | 2858083.90          |
| Hill Climbing - Multiple Random Mutations with an Improved Tweak Function        | 100000        | 10000          | 0.3     | True           | 2270485.66          |
| Hill Climbing - Steepest Step and Restart - First Fitness and Starting Point     | 100000        | 10000          | 0.3     | True           | 838182200.77        |
| Hill Climbing - Steepest Step and Restart - Second Fitness and Starting Point    | 100000        | 10000          | 0.3     | True           | 2438181.67          |
| Simulated Annealing                                                              | 100000        | 10000          | 0.3     | True           | 3115280.81          |
| Tabu Search                                                                      | 100000        | 10000          | 0.3     | True           | 2350578.69          |


## References and Collaborations
#### Book -->
#### Teaching material -->
#### Colleague --> @accountGitHub