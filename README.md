# KNAPSACK OPTIMIZATION USING A GENETIC ALGORITHM

## Project Overview

The **Knapsack Optimization Using a Genetic Algorithm** project implements a Genetic Algorithm (GA) to solve the 0/1 Knapsack Problem.

The objective is to select a combination of items that maximizes the total value without exceeding the given knapsack weight capacity.

The project uses evolutionary computing techniques such as selection, crossover, mutation, and elitism to find an optimal solution.

## Team Members

| Name | Register Number |
|---|---|
| Harshavarthan S | RA2411047050063 |
| Ragul S | RA2411047050064 |

**Programme:** B.Tech Artificial Intelligence  
**Course:** 21CSE320T – Evolutionary Computing

## Problem Statement

Given a collection of items, each having a specific weight and value, the objective is to maximize the total value of selected items while ensuring that the total weight does not exceed the knapsack capacity.

Each item can either be selected (1) or not selected (0).

## Objectives

- Implement a Genetic Algorithm to solve the 0/1 Knapsack Problem.
- Represent solutions using binary chromosomes.
- Design a fitness function with a penalty for exceeding the capacity.
- Apply tournament selection, single-point crossover, and mutation.
- Use elitism to preserve the best solutions.
- Track fitness improvement across generations.
- Validate the result using exhaustive search.

## Technologies Used

- Python
- Google Colab
- Pandas
- Matplotlib
- Genetic Algorithm
- Evolutionary Computing

## Dataset Description

The project uses 15 sample items with their corresponding weights and values.

| Item | Weight | Value |
|---|---:|---:|
| Laptop | 8 | 16 |
| Camera | 5 | 10 |
| Tablet | 4 | 7 |
| Phone | 3 | 6 |
| Headphones | 2 | 4 |
| Monitor | 7 | 12 |
| Keyboard | 2 | 3 |
| Mouse | 1 | 2 |
| Printer | 6 | 9 |
| External Drive | 2 | 5 |
| Speaker | 4 | 6 |
| Router | 2 | 4 |
| Desk Lamp | 3 | 4 |
| Office Chair | 9 | 14 |
| USB Hub | 1 | 2 |

**Knapsack Capacity:** 25 weight units.

## Genetic Algorithm Parameters

| Parameter | Value |
|---|---|
| Population Size | 50 |
| Number of Generations | 100 |
| Crossover Probability | 0.85 |
| Mutation Probability | 1/15 |
| Selection Method | Tournament Selection |
| Tournament Size | 3 |
| Crossover Method | Single-Point Crossover |
| Elitism | 2 Chromosomes |
| Chromosome Representation | Binary Encoding |
| Random Seed | 15 |

## Methodology

1. **Population Initialization:** Generate 50 random binary chromosomes.
2. **Fitness Evaluation:** Calculate the total weight and value of each chromosome.
3. **Selection:** Select parents using tournament selection.
4. **Crossover:** Combine parent chromosomes using single-point crossover.
5. **Mutation:** Randomly flip binary genes to maintain population diversity.
6. **Elitism:** Preserve the two best chromosomes in each generation.
7. **Termination:** Repeat the process for 100 generations.
8. **Validation:** Compare the Genetic Algorithm result with exhaustive search.

## Fitness Function

The fitness function evaluates the quality of each chromosome.

For feasible solutions:

Fitness = Total Value

For overweight solutions:

Fitness = Total Value - 1000 × (Total Weight - Capacity)

This penalty discourages solutions that exceed the knapsack capacity.

## How to Run the Project

1. Open [Google Colab](https://colab.research.google.com/).
2. Create a new Python notebook.
3. Copy the complete project code into a single code cell.
4. Click the **Run** button.
5. View the selected items, total weight, total value, validation result, and convergence graph.

No additional installation is required when running in Google Colab.

## Experimental Results

The Genetic Algorithm successfully identifies a feasible solution for the given dataset.

**Selected Items:**

| Item | Weight | Value |
|---|---:|---:|
| Laptop | 8 | 16 |
| Camera | 5 | 10 |
| Tablet | 4 | 7 |
| Headphones | 2 | 4 |
| Mouse | 1 | 2 |
| External Drive | 2 | 5 |
| Router | 2 | 4 |
| USB Hub | 1 | 2 |
| **Total** | **25** | **50** |

### Performance Summary

- Best Fitness: 50
- Maximum Total Value: 50
- Total Weight Used: 25
- Knapsack Capacity: 25
- Population Size: 50
- Generations: 100

## Validation

The obtained result is validated using exhaustive search by evaluating all 2^15 (32,768) possible item combinations.

The exhaustive-search reference confirms that the maximum feasible value is **50**.

Therefore, the Genetic Algorithm successfully reaches the optimal solution for the given dataset.

## Visualization

The project generates a convergence graph showing the best fitness value across 100 generations.

The graph also displays the exhaustive-search optimum as a reference line.

## Conclusion

This project demonstrates the application of Genetic Algorithms to combinatorial optimization problems.

By implementing binary encoding, tournament selection, crossover, mutation, and elitism, the algorithm successfully identifies an optimal item combination with a total value of 50 and a total weight of 25.

The exhaustive-search validation confirms the optimality of the obtained result.

## References

1. Goldberg, D. E., *Genetic Algorithms in Search, Optimization, and Machine Learning*, Addison-Wesley, 1989.
2. Mitchell, M., *An Introduction to Genetic Algorithms*, MIT Press, 1998.

---

**Developed by:**  
Harshavarthan S – RA2411047050063  
Ragul S – RA2411047050064
