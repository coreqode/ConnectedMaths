---
title: "Laplace-Beltrami Operator"
---  
Laplace Beltrami operator ($\Delta$) takes a function and gives out another function. It is the generalisation of Euclidean [[Laplacian]] Operator on manifolds. Laplacian eigenfunctions depend on each shape and thus 
 coefficients or learned filters from one shape are not trivially transferable to another.

###### Properties of LB operator
- Invariant under [[Isometric deformation]].
- Has countable eigen decomposition
			$\Delta \phi_i = \lambda_i\phi_i$    that forms orthonormal basis for $L^2(\mathcal{M})$
- Characterises geodesic distance.

 ###### Eigen functions
 Eigen functions on the LB of a shape ( or manifold $\mathcal{M}$) has desirable properties. Any function on $\mathcal{M}$ can be expressed as a linear sum of the eigen functions on the LB  of $\mathcal{M}$. The basis function can be given as
 $f = \sum^\inf_0 c_i \phi_i = \sum^\inf_0<f_i, \phi_i>\phi_i =  \sum^k_0<f_i, \phi_i>\phi_i$ 

It is very similar to Fourier transforms.

**NOTE**: Eigenfunctions of Laplace-Beltrami operator on a sphere correspond to basis function of spherical harmonics.

