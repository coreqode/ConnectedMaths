---
title: "Curvature"
tags: "geometry-processing"
---

If we talk about 1D manifolds, curvature measures how strongly a curve deviates from the straight line and for 2D manifolds, it measures how strongly a surface eviates from plane.

Curvature also have relations with *derivative of tangent vector of a curve* and *curve normal*. Hence, $$x''(s) = k(s).n(s)$$
Here, $k(s)$ is curvature of a curve $s$.
If the sign of normal vector flips, then curvature can be negative as well. We can also see that for a *straight line the curvature value becomes 0*.

There is also a relation of curvature with [osculating circles](https://en.wikipedia.org/wiki/Osculating_circle). 
>Basically if I try to fit a circle in a curve (which is also called osculaing circle), I can find the curvature of that curve. So if my fitted circle is small, it means the curvature is more, and if fitted circle is large, curvature is less. ***Hence curvature is inversely proportional to the radius of osculating circle.*** 

In geometry processing, we discuss three types of curvatures. 
- Principal Curvature
- Mean Curvature
- Gaussian Curvature