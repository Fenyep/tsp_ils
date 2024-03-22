# Iterated Local Search

## Generic algorithm

**Data**: An initial solution s0 and a maximum number of iteration maxIt

**Result**: A solution s*

1. s0 = GenerateInitialSolution()
2. s* = LocalSearch(s0)
3. **repeat**
4. .    s' = Pertubations(s*, history)
5. .    s*' = LocalSearch(s')
6. .    s* = AcceptanceCriterion(s*, s*', history)
7. **until** termination condition or maxIt met


## Algorithm applied to the Travelling Salesman Problem

Python implementation of the Iterative Local Search Algorithm to the Travelling Salesman Problem
