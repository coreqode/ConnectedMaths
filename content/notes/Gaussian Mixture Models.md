---
title: "Gaussian Mixture Models"
---

- Gaussian Mixture Models or GMM is a part of [[notes/clustering]] algorithms which clusters the data in an unsupervised learning problem.  
- One important characteristic of GMM is that it is a soft clustering method, unlike [[notes/K mean clustering]], which means that it will associate each point to multiple clusters with a certain probability.  
- A Gaussian Mixture is a function comprised of several Gaussians, each identified by $k \in {1, ...K}$ , where $K$ is the number of the clusters of our dataset.  
- Each Gaussian $k$ in the mixture is comprised of the following parameters:  
	- A mean $\mu$ that defines its centre.  
	- A covariance $\Sigma$ that defines its width. This would be equivalent to the dimensions of an ellipsoid in a multivariate scenario.  
	- A mixing probability $\pi$ that defines how big or small the Gaussian function will be.  
-  
- In general, the Gaussian density function is given by:  
$$\mathcal{N}(\mathbf{x} \mid \mu, \Sigma)=\frac{1}{(2 \pi)^{D / 2}|\Sigma|^{1 / 2}} \exp \left(-\frac{1}{2}(\mathbf{x}-\mu)^T \Sigma^{-1}(\mathbf{x}-\mu)\right)$$  
  Here, $x$ represents data points, and $D$ is the number of dimensions of each data point. $\mu$ and $\Sigma$ are the mean and covariance, respectively.  
    
$$\ln \mathcal{N}(\mathbf{x} \mid \mu, \Sigma)=-\frac{D}{2} \ln 2 \pi-\frac{1}{2} \ln \Sigma-\frac{1}{2}(\mathbf{x}-\mu)^T \Sigma^{-1}(\mathbf{x}-\mu)$$ - If we differentiate the above equation with respect to the mean and covariance and then equate to zero, we will be able to find the optimal values for these parameters, and the solutions will correspond to the [[notes/Maximum Likelihood Estimate (MLE)]].  
