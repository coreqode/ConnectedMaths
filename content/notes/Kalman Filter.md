---
title: "Kalman Filter"
---

**Kalman filter** is used recursive estimation of system state. It has two steps:
- Prediction 
- Estimation

It makes the following assumption:
- The world is Gaussian.
- All models are linear.


#### Kalman Filter:
It takes a mean of prediction and observation from, say, sensor to estimate it's current state.  It's a weighted  mean between the two. Assume the linear model function:
$$ f(x) = Ax+B $$
Then we have our prediction:
$$ x_t = A_t x_{t-1} + B_t u_t + \epsilon_t $$
And our observation:
$$ z_t = C_tx_t + \delta_t $$

The matrix $A_t$ tells us how the state evolved without any controls or errors. $B_t$ tells how the state changes with control commands $u_t$. $C_t$ tells us how to map the state $x_t$ to an observation. $\epsilon_t$ and $\delta_t$ are Gaussian noise in the system.

We model the probability distribution for the observation and the prediction. This system makes sure that everything stays Gaussian. We have the **Kalman Filter Algorithm** as:

1. $Kalman\_filter(\mu_{t-1},\Sigma_{t-1},u_t,z_t)$:
2. $\tilde\mu_t = A_t \mu_{t-1} + B_t u_t$             
3.  $\tilde\Sigma_t = A_t \Sigma_{t-1} A_t^T+ R_t$
4.  $K_t = \tilde\Sigma_t C^T_t(C_t \tilde\Sigma_t C^T_t  + Q_t)^{-1}$
5.  $\mu_t = \mu_{t-1} + K_t(z_t - C_t \tilde\mu_t)$
6.  $\Sigma_t = (I - K_t C_t) \tilde\Sigma_t$
7. return $\mu_t,\Sigma_t$

#### Extended Kalman Filter
If we are in a Gaussian Linear system, then Kalman filter is Optimal. Otherwise we use Extended Kalman Filter.	It performs local linearization via Taylor series. 

For cases when the systems are not linear, the functions change to:
$$ x_t = g(u_t, x_{t-1}) + \epsilon_t $$ 
$$ z_t = h(x_t) + \delta_t $$


We use  **Extended Kalman Filter** as:
1. $Extended\_Kalman\_filter(\mu_{t-1},\Sigma_{t-1},u_t,z_t)$:
2. $\tilde\mu_t = g(u_t, \mu_{t-1} )$             
3.  $\tilde\Sigma_t = G_t \Sigma_{t-1} G_t^T+ R_t$
4.  $K_t = \tilde\Sigma_t H^T_t(H_t \tilde\Sigma_t H^T_t  + Q_t)^{-1}$
5.  $\mu_t = \mu_{t-1} + K_t(z_t - h(\mu_t))$
6.  $\Sigma_t = (I - K_t H_t) \tilde\Sigma_t$
7. return $\mu_t,\Sigma_t$

##### Working of system:
- If the noise in the sensor is zero, the state space is directly mapped to observation without considering the prediction.
- If the noise is maximum, then the state space is calculated using only the prediction, since the observation is too noisy.