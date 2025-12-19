---
title: "Vorticity and turbulence"
excerpt: "Nearly-free evolution of vorticity in two dimensions<br/><img src='/images/vorticity/vorticity.png' style='width: 40%;'>"
collection: portfolio
---

# Vorticity and turbulence

Some fluids flow in a smooth, predictable fashion while others move in chaotic, swirling patterns of vortices. These different flow regimes are ubiquitious across nature, with ice a good example of the former case of *laminar flow* and air of the latter *turbulent flow*. Watching a calm river, it is possible to see that the same fluid can at one time flow in a laminar fashion and transition to turbulent flow as it flows down a knickpoint, before returning to laminar flow again.

The key governing parameter of the flow pattern is the *Reynolds number*,

$$
\text{Re} = \frac{UL}{\nu},
$$

where $U$ and $L$ are characteristic velocity and length scales of the flow, and $\nu$ is the kinematic viscosity (diffusivity of momentum) of the fluid. By scaling the Navier-Stokes equations for a fluid of constant density $\rho$ using $U$, $L$ and a characteristic timescale $T=L/U$ and pressure scale $\mu U/L$, where $\mu$ is the dynamic viscosity of the fluid (satisfying $\mu = \rho \nu$), we obtain

$$
\begin{aligned}
\mathbf{\nabla}'\cdot\mathbf{u}' &= 0,\\
\text{Re}\left[\frac{\partial \mathbf{u}'}{\partial t'} + (\mathbf{u}'\cdot\mathbf{\nabla}')\mathbf{u}'\right] &= -\mathbf{\nabla}'p' + \nabla'^2 \mathbf{u}',
\end{aligned}
$$

where primes denote dimensionless quantities.
