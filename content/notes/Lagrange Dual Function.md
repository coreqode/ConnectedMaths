---
title: "Lagrange Dual Function"
tags: calculus
---
-   Lagrangian: Define Lagrangian $(L: \mathbb{R}^n \times \mathbb{R}^m \times \mathbb{R}^p \rightarrow \mathbb{R})$ as
    
    $$ L(x, \lambda, \nu)=f_0(x)+\sum_{i=1}^m \lambda_i f_i(x)+\sum_{i=1}^p \nu_i h_i(x), $$
    
    with dom $(L=\mathcal{D} \times \mathbb{R}^m \times \mathbb{R}^p$). Here $(\lambda_i, \nu_i)$ are called Lagrange multipliers. Here $(\lambda)$ and $(\nu)$ are called dual variables or Lagrange multiplier vectors.  
    
-   Lagrange Dual Function: Define the Lagrange dual function $(g: \mathbb{R}^m \times \mathbb{R}^\rho \rightarrow \mathbb{R})$
    
    $$ g(\lambda, \nu)=\inf _{x \in \mathcal{D}} L(x, \lambda, \nu)=\inf _{x \in \mathcal{D}}\left(f_0(x)+\sum_{i=1}^m \lambda_i f_i(x)+\sum_{i=1}^p \nu_i h_i(x)\right) $$