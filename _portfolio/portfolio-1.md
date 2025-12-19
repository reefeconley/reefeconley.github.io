---
title: "Vorticity and turbulence"
excerpt: "Nearly-free evolution of vorticity in two dimensions<br/><img src='/images/vorticity/vorticity.png' style='width: 40%;'>"
collection: portfolio
---

Some fluids flow in a smooth, predictable fashion while others move in chaotic, swirling patterns of vortices. These different flow regimes are ubiquitious across nature: glacier flow is a good example of the former case of *laminar flow* while the flow of air in a room is a case of the latter *turbulent flow*. Watching a calm river, we see that the same fluid can transition from laminar to turbulent flow as it flows down a knickpoint before returning to laminar flow once more.

The key governing parameter of the flow pattern is the *Reynolds number*,

$$
\text{Re} = \frac{UL}{\nu},
$$

where $U$ and $L$ are characteristic velocity and length scales of the flow, and $\nu$ is the kinematic viscosity (diffusivity of momentum) of the fluid. The Reynolds number represents the ratio of inertial to viscous forces. When the Reynolds number is large, the inertial forces dominate over viscous forces and the below becomes turbulent.

Let's see where the Reynolds number comes from. The dynamics of incompressible fluids are governed by the Navier-Stokes equations,

$$
\begin{aligned}
\boldsymbol{\nabla}\cdot\mathbf{u} &= 0,\\
\frac{\text{D} \mathbf{u}}{\text{D} t} = \frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u}\cdot\boldsymbol{\nabla})\mathbf{u} &= -\frac{1}{\rho}\boldsymbol{\nabla}p + \nu\nabla^2 \mathbf{u},
\end{aligned}
$$

where we assume no body forces (such as gravity) are present. By taking characteristic velocity and length scales $U$ and $L$, we see that the Reynolds number is given by

$$
\frac{(\mathbf{u}\cdot\boldsymbol{\nabla})\mathbf{u}}{\nu\nabla^2 \mathbf{u}} \sim \frac{U^2/L}{\nu U/L^2}\sim \frac{UL}{\nu},
$$

as expected. The chaotic behaviour of turbulent flow arises from the dominance of the nonlinear inertial $(\mathbf{u}\cdot\boldsymbol{\nabla})\mathbf{u}$ term over viscous dissipation.

We can further manipulate the momentum equation to gain more insight into the development of swirling vortices in turbulent flow. Taking the curl $\left(\boldsymbol{\nabla} \times \right)$ of both sides of the momentum equation gives

$$
\frac{\text{D} \mathbf{\omega}}{\text{D} t} = \left( \mathbf{\omega}\cdot\boldsymbol{\nabla}\right)\mathbf{u} + \nu \nabla^2 \mathbf{\omega},
$$

This is the *vorticity equation*, where $\mathbf{\omega}=\boldsymbol{\nabla} \times \mathbf{u}$. Vorticity represents the local rotation of fluid elements, and is (as expected) non-zero in spinning vortices.

The vorticity equation describes how the vorticity of fluid parcels changes with time. From the terms on the right-hand side of the equation, we can see that this can happen in two ways. The first term on the right-hand side of the vorticty equation describes the process of vortex stretching. This is a uniquely three-dimensional phenomenon that describes the increase in vorticity of a cylinder pulled into its axis of rotation and stretched out along it. This is the mechanism by which hurricanes develop their strong wind speeds. Here, however, we restrict our attention to two-dimensional flows, for which $\left( \mathbf{\omega}\cdot\boldsymbol{\nabla}\right)\mathbf{u} = \mathbf{0}$, leaving 

$$
\frac{\text{D} \mathbf{\omega}}{\text{D} t} = \nu \nabla^2 \mathbf{\omega}.
$$