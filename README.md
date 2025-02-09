# Modeling Virus Mutation and T-Cell Dynamics in HIV/AIDS

This repository contains the code and resources for the research paper titled "Modeling Virus Mutation and T-Cell Dynamics in HIV/AIDS: A Comparative Study using Finite Difference and Physics-Informed Neural Network".

## Overview

This research paper explores the dynamics of HIV infection by modeling the interactions between T-cells and the virus. It focuses on normal T-cells, latently infected T-cells, actively infected T-cells, and the virus itself [1]. The model incorporates key biological factors such as reclassification, death rates, and population dynamics, while ensuring the total T-cell population is bounded and the steady-state solution remains stable [1]. The study employs and compares two numerical methods: the Finite Difference Method (FDM) and Physics-Informed Neural Networks (PINNs).

## Key Concepts

*   **T-cells:**  Essential for cell-mediated immune response, including helper T-cells and cytotoxic T-cells.
*   **HIV:** A highly adaptable virus that integrates its genetic material into host cells, turning them into virus-producing factories.
*   **Finite Difference Method (FDM):** A numerical method that discretizes continuous space into a grid to solve partial differential equations. This method is known for its stability, fast convergence, high accuracy and simplicity.
*   **Physics-Informed Neural Networks (PINNs):**  Neural networks that incorporate the governing laws of a physical phenomenon, allowing them to learn from data and equations. PINNs can learn with little or no labelled datasets.

## Methodology

The research uses a system of four equations to model the interactions between T-cells and HIV.
```math
\begin{align*}
\frac{dT}{dt} &= s + rT\left(1 - \frac{T + T_L + T_A}{T_{\text{max}}}\right) - \mu T - k_1VT, \\
\frac{dT_L}{dt} &= k_1VT - \mu T_L - k_2T_L, \\
\frac{dT_A}{dt} &= k_2T_L - \beta T_A, \\
\frac{dV}{dt} &= N\beta T_A - k_1VT - \alpha V.
\end{align*}
```

*   The equations describe the behavior of normal T-cells, latently infected T-cells, actively infected T-cells, and the virus.
*   The study uses both Finite Difference Method (FDM) and Physics-Informed Neural Networks (PINNs) to solve the system of equations.
*   The model parameters are based on biological data.

## Results

The paper compares the results obtained from FDM and PINNs, using graphs to show the concentration of different cell types and the virus over time.

*   The results are presented in the form of concentration vs time graphs.
*   Figures 1, 2, 3, 4 and 5 shows the results obtained from Physics-Informed Neural Networks.
*   Figures 6, 7, 8, 9 and 10 shows the results obtained from Finite Difference Method.

## Repository Contents

*   `code/`: Contains the source code for the FDM and PINN implementations.
*   `figures/`: Contains all the figures used.
*   `paper/`: Contains the original research paper.
*   `README.md`: This file.
*   `reference/`: Contains a book which is our main reference.
*   `requirements.txt`: Lists the required Python libraries.

## How to Run the Code

1.  Clone the repository:
    ```bash
    git clone <repository URL>
    ```
2.  Navigate to the project directory:
    ```bash
    cd <repository name>
    ```
3.  Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```
4.  Run the simulation scripts located in the code directory
