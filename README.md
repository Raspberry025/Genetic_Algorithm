# Genetic_Algorithm
MLPC_Group_Assignment

Smart Grid Energy Optimization using Genetic Algorithms

This project focuses on optimizing energy distribution in a smart grid using Genetic Algorithms (GA). It allocates energy from multiple sources (e.g., Solar, Wind, Hydro) to consumer nodes (e.g., Residential, Industrial) across a 24-hour cycle to minimize cost, transmission losses, and constraint violations.

Objectives

- Minimize total energy cost for fulfilling demand.
- Reduce energy transmission losses based on distance.
- Ensure all nodes receive sufficient power within source capacity limits.
- Compare performance of Serial GA, Parallel GA, Greedy, and Rule-based methods.

Project Structure

- 'DAML Group Project Code.ipynb': Main notebook containing preprocessing, EDA, GA execution, baseline comparison, and visualizations.
- 'nodes_df.csv': Contains hourly energy demand of each node.
- 'sources_df.csv': Contains hourly energy supply of each source with cost and capacity details.
- 'distance_df.csv': Matrix of distances (in km) between nodes and sources.

Methods Used

Genetic Algorithm (GA)
- Chromosomes represent hourly power allocations from each source to each node.
- Fitness function penalizes unmet demand, supply overflow, cost, and line loss.
- Includes tournament selection, crossover, and mutation operators.

Parallel GA
- Uses 'multiprocessing' to parallelize fitness evaluation for faster computation.

Baselines
- Greedy Algorithm: Assigns demand to first capable source.
- Rule-Based Method (Optional): Manually defined source preference rules.

Outputs & Analysis

- Convergence curves showing improvement in fitness over generations.
- Fitness comparison across GA variants and baselines.
- Mutation rate vs. fitness trade-off analysis.
- Performance table showing fitness, cost, loss, and execution time.
- Penalty stress test with extreme demand spikes.

Dependencies & Setup

Before running the notebook, make sure the following Python libraries are installed:

pip install pandas numpy matplotlib seaborn psutil

You will also need:

Python 3.7+
Jupyter Notebook to run .ipynb interactively

This project was developed as part of the ITS66604 - Machine Learning for Predictive Computing (MLPC) course for the May 2025 semester. It fulfills all deliverables such as:

- Mathematical problem formulation
- Fitness function and chromosome encoding
- Parallelization and serial comparison
- Convergence visualization and performance trade-off
- Penalty-based evaluation and stress testing
