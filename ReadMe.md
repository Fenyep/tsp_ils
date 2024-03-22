# Iterated Local Search

## Generic algorithm

**Data**: An initial solution s0 and a maximum number of iteration maxIt

**Result**: A solution s*

1. s0 = GenerateInitialSolution()
2. s* = LocalSearch(s0)
3. **repeat**
4. .... s' = Pertubations(s*, history)
5. .... s*' = LocalSearch(s')
6. .... s* = AcceptanceCriterion(s*, s*', history)
7. **until** termination condition or maxIt met
8. **return** s*


## Algorithm applied to the Travelling Salesman Problem

**Data**: cities, maxIt

**Result**: A solution s*

1. *// Initialize the solution with a random permutation of the cities*
2. s* = random_permutation(cities)
3. *// Perform localsearch on the subproblem of finding the shortest path between two adjacent cities*
4. **repeat**
5. .... *// Perturb the solution by swapping two cities*
6. .... s' = Pertubation(s*)
7. .... *// Evaluate the fitness of the pertubed solution with the current solution*
8. .... fitness = evaluate_fitness(s')
9. .... *// Compare the fitness of the perturbed solution with the current solution*
10. .... if fitness < evaluate_fitness(s*):
11. ........ // Accept the pertubed solution as the new best solution
12. ........ s* = s'
13. **until** termination condition or maxIt
14. **return** s*


## implementation of the Iterative Local Search Algorithm to the Travelling Salesman Problem
