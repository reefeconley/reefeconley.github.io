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

![Mersey](/images/mersey.jpeg){: .align-center width="60%"}
<p style="text-align: center;">*The River Mersey flowing over a knickpoint, showing a transition to turbulence as the velocity and depth of the flow increase.*</p>

Let's see where the Reynolds number comes from. The dynamics of fluids such as water and ice are governed by the incompressible Navier-Stokes equations,

$$
\begin{aligned}
\boldsymbol{\nabla}\cdot\mathbf{u} &= 0,\\
\frac{\text{D} \mathbf{u}}{\text{D} t} = \frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u}\cdot\boldsymbol{\nabla})\mathbf{u} &= -\frac{1}{\rho}\boldsymbol{\nabla}p + \nu\nabla^2 \mathbf{u},
\end{aligned}
$$

where we have neglected the effects of body forces (namely gravity). By taking characteristic velocity and length scales $U$ and $L$, we see that the Reynolds number is given by

$$
\frac{(\mathbf{u}\cdot\boldsymbol{\nabla})\mathbf{u}}{\nu\nabla^2 \mathbf{u}} \sim \frac{U^2/L}{\nu U/L^2}\sim \frac{UL}{\nu},
$$

as expected. The chaotic behaviour of turbulent flow arises from the dominance of the nonlinear inertial $(\mathbf{u}\cdot\boldsymbol{\nabla})\mathbf{u}$ term over viscous dissipation. From this, we can see why river flows become turbulent as they flow down a knickpoint: both the flow velocity and depth increase while the kinematic viscosity remains constant (it is a material property of water). Both of these effects cause an increase in the Reynolds number, causing a transition to turbulent flow.

We can further manipulate the momentum equation to gain more insight into the development of swirling vortices in turbulent flow. Taking the curl $\left(\boldsymbol{\nabla} \times \right)$ of both sides of the momentum equation gives

$$
\frac{\text{D} \boldsymbol{\omega}}{\text{D} t} = \left( \boldsymbol{\omega}\cdot\boldsymbol{\nabla}\right)\mathbf{u} + \nu \nabla^2 \boldsymbol{\omega},
$$

This is the *vorticity equation*, where $\boldsymbol{\omega}=\boldsymbol{\nabla} \times \mathbf{u}$. Vorticity represents the local rotation of fluid elements, and is (as expected) non-zero in spinning vortices.

The vorticity equation describes how the vorticity of fluid parcels changes with time. From the terms on the right-hand side of the equation, we can see that this can happen in two ways. The first term on the right-hand side of the vorticty equation describes the process of vortex stretching. This is a uniquely three-dimensional phenomenon that describes the increase in vorticity of a cylinder pulled into its axis of rotation and stretched out along it. This is the mechanism by which hurricanes develop their strong wind speeds. Here, however, we restrict our attention to two-dimensional flows, for which $\left( \boldsymbol{\omega}\cdot\boldsymbol{\nabla}\right)\mathbf{u} = \mathbf{0}$, leaving 

$$
\frac{\text{D} \boldsymbol{\omega}}{\text{D} t} = \nu \nabla^2 \boldsymbol{\omega}.
$$

From this, we can see that the vorticity of inviscid ($\nu=0$) fluids is conserved, yet it diffuses for any real fluid of non-zero viscosity. Scaling the vorticity equation with ${\omega \sim U/L}$ and ${t \sim L/U}$ gives

$$
\frac{\text{D} \boldsymbol{\omega'}}{\text{D} t'} = \frac{1}{\text{Re}} \nabla'^2 \boldsymbol{\omega'},
$$

where primes denote dimensionless quantities. We see that the diffusion of vorticity decreases for large Reynolds number flows.

The video below shows the nearly-free evolution of vorticity in a doubly-periodic two-dimensional domain. The flow has a large Reynolds number $(\text{Re}=5\times10^4)$. The vorticity field is initially perturbed everywhere across many wavenumbers, and the vorticity is then allowed to freely evolve according to the above two-dimensional vorticity equation.

<div style="display: flex; justify-content: center;">
  <video controls style="width: 50%; height: auto;">
    <source src="/images/vorticity/vort_vid.mp4" type="video/mp4">
  </video>
</div>

Though the fluid evolves chaotically and unpredictably, the phenomenology of the flow is clear — the small vortices that form initially soon coalesce into larger ones, until the flow field is dominated by a handful of large vortices at late times. This is characteristic of two-dimensional turbulence and reflects a general cascade of energy from smaller to larger scales. This is fundamentally different to three-dimensional turbulence, in which the energy flows from larger to smaller scales (via vortex stretching). This energy cascade to larger length scales is known as the *inverse energy cascade* and has a significant consequence for the dynamics of the the atmosphere and ocean, which act in some ways as two-dimensional fluids. Kolmogorov's spectral theory of turbulence predicts the energy spectrum $\mathcal{E}$ of such a two-dimensional flow to be

$$
\mathcal{E(k) \sim k^{-5/3}},
$$

in which energy is transferred to smaller wavenumbers (larger wavelengths) approximately along a $k^{-5/3}$ slope when plotted logarithmically.

The magnitude of the voriticty field also decreases with time (see the changing scale bar), reflecting the dissipation of vorticity owing to the $\nu \nabla^2\boldsymbol{\omega}$ term (though $1/\text{Re}$ is small, it is not exactly zero).


