---
title: "Heat Equation"
---
Heat equation aims to model the distribution of heat over a surface with time. For 3 dimension, it is given as:
		   $\frac{\partial T}{\partial t} = \alpha(\frac{\partial^2 T}{\partial x^2}+\frac{\partial^2 T}{\partial y^2}+\frac{\partial^2 T}{\partial z^2})$ = $\alpha \nabla^2T$ 
The right hand side is the [[Laplacian]] operator. It states that the change in temperature at a give point $u$ is linearly dependent on the second derivative of the the temperature at that point, with respect to the space ( shape ). Here $\alpha$ is the thermal *diffusivity* of the medium. 


- It is closely related to spectral geometry.

Solving heat equation would mean finding the temperature at any given point of the domain at time any time *t*.
A function in the domain that satisfies the equation:
$u_t = \alpha \nabla^2 u= \alpha \Delta u$
(i.e second derivative of the function in the domain is equal to the function itself) is the solution to the heat equation.

Intuitively, heat diffusion at a point of surface depends on the curvature of the heat  diffusion function itself. If the function is convex, the temperature would decrease at that point, in time and visa versa. Meaning, the change in temperature at any point depends on the gradient of the temperature.


In equilibrium, $u_t=0$ to solve the heat equation, we solve the Laplace equation: $\nabla ^ 2 u=0$. 
