# CI2024_lab1

## Proposed algorithms:
- ### First dumb solutions
- ### Hill Climbing - Single random mutation
- ### Hill Climbing - Multiple random mutations
- ### Hill Climbing - Steepest Step and Restart
- ### Simulated Annealing
- ### Tabu Search

## Notation
#### _First fitness and starting point_ == considering (valid/invalid, -cost) as fitness and starting from all sets taken
#### _Second fitness and starting point_ == considering (# of covered items, -cost) as fitness and starting from the chance of 0.1% for each set to be taken
#### _First tweak_ == single random mutation
#### _Second tweak_ == basic multiple random mutations
#### _Third tweak_ == improved multiple random mutations
#### _num_steps_ == number of steps of valid solutions to reach the best fitness

## Contents description

Using '_first fitness and starting point_' fitness regarding from both valid and invalid solutions have been plotted.
Using '_second fitness and starting point_' both plots considering # of covered items and -cost have been plotted.


All three _Hill Climbing_ algorithms have been implemented:
- using _first fitness and starting point_  
- using _second fitness and starting point_ 

_Simulated Annealing_ and _Tabu Search_ algorithms has been implemented:
- using _third tweak_ combined with _second fitness and starting point_. 


## Observations:
- The second dumb solution could be invalid
- Fitness is a tuple, so it's difficult to understand from the bidimensional plot the iteration which best fitness is reached in. However, _num_steps_ is printed and reported in the results section.
- Using '_second fitness_' is relevant to show the behaviour with both first and second criterion of fitness (i.e. #of covered items and -cost)
- with '_first_fitness_' we have to start from a valid solution (otherwise we are attracted from all-falses state)
- using '_second fitness_' we can also starting from an invalid solution
- choosing a low number of iterations could lead to an invalid solution even though the algorithm is correct and it would work properly with more iterations.
- in the _Simulated Annealing_ and _Tabu Search_ a penalty was added for solution of invalid region in order to jump into the valid one


## Results
In the following, results about the 6 instances gathered from one execution.
#### _Cost_ represents the absolute value of the evaluated cost (the lower the value, the better the outcome), while _# steps_ indicates the number of steps taken to achieve the optimal valid fitness.
#### _# steps_ is limited to 150 for Hill Climbing and 1,000 for Tabu Search. In contrast, the maximum iterations for Simulated Annealing depends on the temperature.

## Instance 1

### Instance 1
| Algorithm                                                                 | Universe Size | Number of Sets | Density | Valid Solution | Cost           | # steps |
|---------------------------------------------------------------------------|---------------|----------------|---------|----------------|----------------|---------|
| First Dumb Solution                                                      | 100           | 10             | 0.2     | True           | 273.43         | 0       |
| Second Dumb Solution                                                     | 100           | 10             | 0.2     | False          | 215.85         | 0       |
| Hill Climbing - Single Random Mutation - First Fitness and Starting Point | 100           | 10             | 0.2     | True           | 287.29         | 0       |
| Hill Climbing - Single Random Mutation - Second Fitness and Starting Point | 100           | 10             | 0.2     | True           | 268.96         | 24      |
| Hill Climbing - Multiple Random Mutations - First Fitness and Starting Point | 100         | 10             | 0.2     | True           | 271.70         | 0       |
| Hill Climbing - Multiple Random Mutations - Second Fitness and Starting Point | 100        | 10             | 0.2     | True           | 295.54         | 23      |
| Hill Climbing - Multiple Random Mutations with an Improved Tweak Function | 100          | 10             | 0.2     | True           | 278.99         | 13      |
| Hill Climbing - Steepest Step and Restart - First Fitness and Starting Point | 100        | 10             | 0.2     | False          | 283.98         | 1       |
| Hill Climbing - Steepest Step and Restart - Second Fitness and Starting Point | 100      | 10             | 0.2     | True           | 286.91         | 9       |
| Tabu Search                                                             | 100           | 10             | 0.2     | True           | 285.13         | 5       |
| Simulated Annealing                                                     | 100           | 10             | 0.2     | True           | 279.13         | 23      |

### Instance 2
| Algorithm                                                                 | Universe Size | Number of Sets | Density | Valid Solution | Cost           | # steps |
|---------------------------------------------------------------------------|---------------|----------------|---------|----------------|----------------|---------|
| First Dumb Solution                                                      | 1000          | 100            | 0.2     | True           | 33954.19       | 0       |
| Second Dumb Solution                                                     | 1000          | 100            | 0.2     | True           | 14938.04       | 0       |
| Hill Climbing - Single Random Mutation - First Fitness and Starting Point | 1000          | 100            | 0.2     | True           | 8429.75        | 139     |
| Hill Climbing - Single Random Mutation - Second Fitness and Starting Point | 1000          | 100            | 0.2     | True           | 7126.42        | 131     |
| Hill Climbing - Multiple Random Mutations - First Fitness and Starting Point | 1000        | 100            | 0.2     | True           | 8589.95        | 143     |
| Hill Climbing - Multiple Random Mutations - Second Fitness and Starting Point | 1000       | 100            | 0.2     | True           | 8070.69        | 108     |
| Hill Climbing - Multiple Random Mutations with an Improved Tweak Function | 1000         | 100            | 0.2     | True           | 7204.84        | 115     |
| Hill Climbing - Steepest Step and Restart - First Fitness and Starting Point | 1000      | 100            | 0.2     | True           | 17754.91       | 60      |
| Hill Climbing - Steepest Step and Restart - Second Fitness and Starting Point | 1000     | 100            | 0.2     | True           | 7762.19        | 20      |
| Tabu Search                                                             | 1000          | 100            | 0.2     | True           | 7378.51        | 460     |
| Simulated Annealing                                                     | 1000           | 100             | 0.2     | True           | 9490.63         | 38      |

### Instance 3
| Algorithm                                                                 | Universe Size | Number of Sets | Density | Valid Solution | Cost           | # steps |
|---------------------------------------------------------------------------|---------------|----------------|---------|----------------|----------------|---------|
| First Dumb Solution                                                      | 10000         | 1000           | 0.2     | True           | 4278629.76     | 0       |
| Second Dumb Solution                                                     | 10000         | 1000           | 0.2     | True           | 2154873.92     | 0       |
| Hill Climbing - Single Random Mutation - First Fitness and Starting Point | 10000         | 1000           | 0.2     | True           | 3670746.19     | 148     |
| Hill Climbing - Single Random Mutation - Second Fitness and Starting Point | 10000         | 1000           | 0.2     | True           | 157637.53      | 57      |
| Hill Climbing - Multiple Random Mutations - First Fitness and Starting Point | 10000       | 1000           | 0.2     | True           | 3382647.09     | 149     |
| Hill Climbing - Multiple Random Mutations - Second Fitness and Starting Point | 10000      | 1000           | 0.2     | True           | 144952.55      | 128     |
| Hill Climbing - Multiple Random Mutations with an Improved Tweak Function | 10000         | 1000           | 0.2     | True           | 132757.47      | 148     |
| Hill Climbing - Steepest Step and Restart - First Fitness and Starting Point | 10000      | 1000           | 0.2     | True           | 4044998.36     | 20      |
| Hill Climbing - Steepest Step and Restart - Second Fitness and Starting Point | 10000     | 1000           | 0.2     | True           | 149385.63      | 34      |
| Tabu Search                                                             | 10000         | 1000           | 0.2     | True           | 140215.98      | 177     |
| Simulated Annealing                                                     | 10000           | 1000             | 0.2     | True           | 213425.38         | 68      |

### Instance 4
| Algorithm                                                                 | Universe Size | Number of Sets | Density | Valid Solution | Cost           | # steps |
|---------------------------------------------------------------------------|---------------|----------------|---------|----------------|----------------|---------|
| First Dumb Solution                                                      | 100000        | 10000          | 0.1     | True           | 251166130.03   | 0       |
| Second Dumb Solution                                                     | 100000        | 10000          | 0.1     | True           | 125762836.17   | 0       |
| Hill Climbing - Single Random Mutation - First Fitness and Starting Point | 100000        | 10000          | 0.1     | True           | 247489000.90   | 149     |
| Hill Climbing - Single Random Mutation - Second Fitness and Starting Point | 100000        | 10000          | 0.1     | True           | 2385827.35     | 120     |
| Hill Climbing - Multiple Random Mutations - First Fitness and Starting Point | 100000      | 10000          | 0.1     | True           | 244690773.56   | 149     |
| Hill Climbing - Multiple Random Mutations - Second Fitness and Starting Point | 100000     | 10000          | 0.1     | False          | 1709166.06     | 60      |
| Hill Climbing - Multiple Random Mutations with an Improved Tweak Function | 100000        | 10000          | 0.1     | True           | 2289452.76     | 147     |
| Hill Climbing - Steepest Step and Restart - First Fitness and Starting Point | 100000      | 10000          | 0.1     | True           | 249625311.48   | 20      |
| Hill Climbing - Steepest Step and Restart - Second Fitness and Starting Point | 100000     | 10000          | 0.1     | True           | 2476388.56     | 55      |
| Tabu Search                                                             | 100000        | 10000          | 0.1     | True           | 2254302.82     | 435     |
| Simulated Annealing                                                     | 100000           | 10000             | 0.1     | True           | 2914794.62         | 122      |

### Instance 5
| Algorithm                                                                 | Universe Size | Number of Sets | Density | Valid Solution | Cost            | # steps |
|---------------------------------------------------------------------------|---------------|----------------|---------|----------------|-----------------|---------|
| First Dumb Solution                                                      | 100000       | 10000          | 0.2     | True           | 538483067.53    | 0       |
| Second Dumb Solution                                                     | 100000       | 10000          | 0.2     | True           | 272444411.16    | 0       |
| Hill Climbing - Single Random Mutation - First Fitness and Starting Point | 100000      | 10000          | 0.2     | True           | 530353019.04    | 149     |
| Hill Climbing - Single Random Mutation - Second Fitness and Starting Point | 100000      | 10000          | 0.2     | True           | 2531749.57      | 41      |
| Hill Climbing - Multiple Random Mutations - First Fitness and Starting Point | 100000    | 10000          | 0.2     | True           | 525090013.89    | 149     |
| Hill Climbing - Multiple Random Mutations - Second Fitness and Starting Point | 100000   | 10000          | 0.2     | True           | 2530235.44      | 22      |
| Hill Climbing - Multiple Random Mutations with an Improved Tweak Function | 100000     | 10000          | 0.2     | True           | 2097044.61      | 133     |
| Hill Climbing - Steepest Step and Restart - First Fitness and Starting Point | 100000   | 10000          | 0.2     | True           | 535291925.95    | 60      |
| Hill Climbing - Steepest Step and Restart - Second Fitness and Starting Point | 100000  | 10000          | 0.2     | True           | 2476388.56      | 55      |
| Tabu Search                                                             | 100000       | 10000          | 0.2     | True           | 2365045.71      | 994     |
| Simulated Annealing                                                     | 100000           | 10000             | 0.2     | True           | 2954034.73         | 31      |

### Instance 6
| Algorithm                                                                 | Universe Size | Number of Sets | Density | Valid Solution | Cost            | # steps |
|---------------------------------------------------------------------------|---------------|----------------|---------|----------------|-----------------|---------|
| First Dumb Solution                                                      | 100000       | 10000          | 0.3     | True           | 840968642.56    | 0       |
| Second Dumb Solution                                                     | 100000       | 10000          | 0.3     | True           | 420620078.56    | 0       |
| Hill Climbing - Single Random Mutation - First Fitness and Starting Point | 100000      | 10000          | 0.3     | True           | 828575686.57    | 148     |
| Hill Climbing - Single Random Mutation - Second Fitness and Starting Point | 100000      | 10000          | 0.3     | True           | 2437888.89      | 11      |
| Hill Climbing - Multiple Random Mutations - First Fitness and Starting Point | 100000    | 10000          | 0.3     | True           | 819868808.81    | 148     |
| Hill Climbing - Multiple Random Mutations - Second Fitness and Starting Point | 100000   | 10000          | 0.3     | True           | 2607641.12      | 5       |
| Hill Climbing - Multiple Random Mutations with an Improved Tweak Function | 100000     | 10000          | 0.3     | True           | 2267580.04      | 76      |
| Hill Climbing - Steepest Step and Restart - First Fitness and Starting Point | 100000   | 10000          | 0.3     | True           | 835681945.13    | 60      |
| Hill Climbing - Steepest Step and Restart - Second Fitness and Starting Point | 100000  | 10000          | 0.3     | True           | 2436145.27      | 29      |
| Tabu Search                                                             | 100000       | 10000          | 0.3     | True           | 2430511.27      | 42      |
| Simulated Annealing                                                     | 100000           | 10000             | 0.3     | True           | 3023534.52         | 11      |




## References and Collaborations
#### Book --> S. Luke; “Essentials of Metaheuristics” (2nd edition)
#### Teaching material
#### Colleagues --> Gabriele Raffaele, Giuseppe Vacante