# 1D Time-Dependent Schrödinger Equation Simulation

This project implements a numerical solver for the **1D Time-Dependent Schrödinger Equation (TDSE)**. Using the **Crank-Nicolson method** (an implicit scheme), the simulation models the evolution of a Gaussian wave packet and its interaction with a potential barrier, allowing for the study of quantum tunneling and transmission coefficients.

## Project Overview

Solving the Schrödinger equation numerically is a fundamental task in quantum mechanics. The challenge lies in maintaining the stability and unitarity of the wave function over time. This project utilizes:
* **Cayley's Form / Crank-Nicolson Scheme**: To ensure the evolution operator remains unitary.
* **Thomas Algorithm**: An efficient tridiagonal matrix solver used to compute the wave function at each time step.

## Repository Structure

* **`01_Schrodinger_Solver.py`**: The core simulation script. It initializes a Gaussian wave packet and computes its evolution through a potential barrier by solving the implicit system at each step.
* **`02_Wave_Packet_Animation.py`**: A visualization tool that uses `matplotlib.animation` to render the probability density $|\Psi(x,t)|^2$ and the potential $V(x)$.
* **`03_Numerical_Analysis.ipynb`**: A comprehensive Jupyter Notebook exploring different physical scenarios, such as the dependence of transmission coefficients on barrier height and the convergence of the method with different grid sizes ($N$).

## Technologies Used

* **Python 3**
* **NumPy**: For complex number handling and matrix operations.
* **Matplotlib**: For static plotting and dynamic animations.
