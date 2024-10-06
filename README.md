# CI2024_lab1

- ### First dumb solutions --> the second one could be invalid
- ### Hill Climbing - Single random mutation
- ### Hill Climbing - Multiple random mutations
- ### Hill Climbing - Steepest Step and Restart

## All three methods:
- Using fitness1 and startingpoint1 --> with fitness1, we have to start from a valid solution
- Using fitness2 and startingpoint2 --> we can also starting from an invalid solution (we are not attracted from all falses state)


## Observations:
- with fitness1, we have to start necessarily from a valid solution
- using fitness2, we can also starting from an invalid solution (we are not attracted from all-falses state)
-choosing a low number of iterations could lead to an invalid solution even though the algorithm is correct and it would work properly with more iterations. (example fitness2, startingpoint2 and 100 iteration doesn't work in the steepest step and restart)


# TO DO:
- ogni volta che c'è:   
_fitness_values = [second_fitness_criterion for first_fitness_criterion, second_fitness_criterion in history]
fitness_plot(fitness_values)_
commentare cosa sono primo e secondo criterio
- ogni volta che si usa fitness 2 vorrei stampare entrambi i grafici (con il primo e secondo criterio di fitness)
- mettere labels nei grafici per spiegare cosa significano le curve ed i punti e mettere la griglia grid
