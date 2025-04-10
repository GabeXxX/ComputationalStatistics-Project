# ComputationalStatistics-Project
----
# DeepONet

This project explores the implementation and application of DeepONet, a neural network architecture designed to learn nonlinear operators between function spaces.

## Overview

The primary goal of DeepONet is to approximate nonlinear operators  $G: V_1 \rightarrow V_2$ that map between spaces of function. This is achieved using the Universal Approximation Theorem for Operators, enabling the model to handle input data from sensors in a mesh-free manner.  In many applications, DeepONet can learn the mapping between parameters of a PDE and its solution.

## Key Concepts

* **Universal Approximation Theorem for Operators:** The theoretical foundation that allows DeepONet to approximate complex operators using a finite number of function values.
* **DeepONet Architecture:** Comprises two main components:
    * A **branch network** that processes input functions sampled at specific locations.
    * A **trunk network** that processes the output locations[cite: 9].
* The final output is computed as the sum of the products of the outputs of the branch and trunk networks[cite: 9].

## Tests

The project includes tests on the following problems:

1.  **Poisson Equation:** Learning the mapping from parameters to the solution of a Poisson equation.
2.  **Function-to-Function Mapping:** Approximating a nonlinear operator that maps 1D functions to other 1D functions.
3.  **Darcy Flow:** Modeling a simplified Darcy flow model with a spatially distributed permeability field.
4.  **Comparison with POD-NN** in the approximation of of the Darcy flow model.
5.  Analysis of the impact of **latent dimension**, **training data size**, and **noise** on the accuracy of DeepONet.

## Bonus

* Exploration of Mesh-Informed Neural Networks (MINN).

## References
1. Lu, L., Jin, P., Pang, G., Zhang, Z., & Karniadakis, G. E. (2021). Learning nonlinear operators via DeepONet based on the universal approximation theorem of operators. Nature Machine Intelligence, 3(3), 218–229. https://doi.org/10.1038/s42256-021-00302-5
2. Franco, N. R., Manzoni, A., & Zunino, P. (2022). Mesh-Informed neural networks for operator learning in finite element spaces. arXiv (Cornell University). https://doi.org/10.48550/arxiv.2203.11648
