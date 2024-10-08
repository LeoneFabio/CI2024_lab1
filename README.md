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
- run entire code with the 6 istances of requested (UNIVERSE_SIZE, NUM_SETS and density)
- delete plots of second fitness and starting point w.r.t. the -cost --> are useless, they don't give us any further info
- add 'write into a file' lines of code, in order to save results
- search for better parameters in simulated annealing in order to do not spend so much time with 100_000 universal size configurations
- try if possible to create an initial index in the notebook, so that everything is more clear


## Statistics and results 
In the following, results about the 6 instances.

## References and Collaborations
#### Book -->
#### Teaching material -->
#### Colleague --> @accountGitHub
