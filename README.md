# 1D Heat Equation Simulation (Implicit FDM)

A numerical solver for the 1-dimensional Heat Equation using the **Implicit (Backward Euler) Finite Difference Method** coupled with a custom Gaussian elimination solver.

Developed as part of the **Numerical Mathematics** coursework within the Mathematical Engineering curriculum at CTU (Czech Technical University in Prague).

$$\frac{\partial T}{\partial t} = \alpha \frac{\partial^2 T}{\partial x^2}$$

## Features
- **Spatial Discretization:** Central difference scheme on a uniform grid.
- **Time Stepping:** Implicit Backward Euler scheme (unconditionally stable).
- **Linear Solver:** Manual forward Gaussian elimination and back-substitution on the tridiagonal coefficient matrix.
- **Visualization:** Matplotlib temperature distribution across the rod over time.

## Methodology
The parabolic partial differential equation models heat diffusion across a 1D medium of length $L$. By applying an implicit formulation, the system avoids numerical instability limits on the time step ($\Delta t$), solving the resulting linear system $A \cdot T^{n+1} = T^n + \text{bc}$ at each time step.
