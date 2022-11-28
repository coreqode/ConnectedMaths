---
title: "Expectation Maximization"
alias: "EM"
---
This algorithm is usually used to fit multiple Gaussian distributions over a given dataset. This can be considered as an extension of *k means model*, where the centres are described by Gaussian parameters instead of a mean in Euclidean space.

##### Multivariate Gaussian Distribution:
$\mathcal{N}(x; \mu,\Sigma) = \frac{1}{(2\pi)^{d/2}}\ |\Sigma|^{-1/2}\ e^{( -\frac{1}{2} (x-\mu)^T|\Sigma|^{-1/2}(x-\mu))}$	

Given the data, we can calculate the **mean** as:

$\mu = \frac{1}{m}\sum_ix^{(i)}$

and **variance**:

$\Sigma = \frac{1}{m}\sum_i  (x^{(i)}-\mu)^T(x^{(i)}-\mu)$

Expectation algorithm is iteratively done in 2 steps:
1. **Expectation step**:
	We calculate the probability of each point belonging to a gaussian using above formula. The distribution with maximum probability value is chosen as parent distribution.
2. **Maximization step**:
	For each gaussian, $\mu$ and $\Sigma$ values are recalculated using the newly assigned datapoints.

Another interesting application of EM [[notes/Kalman Filter]]