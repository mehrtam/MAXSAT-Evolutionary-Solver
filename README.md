**MAXSAT Optimization Using Evolutionary Algorithms**

This repository contains a complete implementation of evolutionary algorithms to solve the MAXSAT problem using the Weighted CNF (WDIMACS) format. It includes:

A baseline and optimized evolutionary solver

An experimental framework to analyze the effect of hyperparameters such as population size, mutation rate, and time budget

Statistical analysis and visualizations to compare solver performance

Repository Structure:

notebooks/

MAXSAT_Solver.ipynb – Exercises 1–3, optimized and baseline solvers

MAXSAT_Parameter_Study.ipynb – Parameter experiments and boxplots

data/

3col80_5_2.shuffled.cnf.wcnf

results/

maxsat_experiment_results.csv

maxsat_boxplot.png

README.md

requirements.txt

Notebook Descriptions:

MAXSAT_Solver.ipynb:
Implements the evolutionary algorithm with two versions:

Optimized using NumPy and Numba for fast clause satisfaction

Baseline version for comparison
Includes clause parsing, population initialization, fitness evaluation, crossover, mutation, and elitism.

MAXSAT_Parameter_Study.ipynb:
Runs experiments to test the effect of:

Population size: 10, 30, 50, 100

Mutation rate: 0.001, 0.01, 0.05, 0.1

Time budget: 1, 5, 10, 30 seconds
Each setting is tested across 100 repetitions. Results are saved to CSV and plotted with Seaborn boxplots.

Output Format:

Each run returns:
t nsat xbest
Where:

t = number of evaluations

nsat = number of satisfied clauses

xbest = best assignment found

Requirements:

numpy

pandas

matplotlib

seaborn

numba

Install with:

pip install -r requirements.txt

References:

MAXSAT Benchmark: http://maxsat.ia.udl.cat/benchmarks/

WDIMACS Format Specification

Author:

This project was developed as part of AI coursework at the University of Birmingham
License:

MIT License © 2025 Mehrta Eslami
