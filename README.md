# AMS595-Fractal-Approximation

This repository contains the implementation and analysis for **Python Project 2: Fractal Approximation**, completed as part of **AMS 595 / DCS 525 Project.  
The project demonstrates three numerical techniques **iterative complex dynamics**, **stochastic simulation**, and **analytic function approximation** implemented in Python with visualizations and data analysis.

---

## Project Overview

### 1) Mandelbrot Set Generation
The Mandelbrot set is constructed using the recurrence
$$
z_{n+1} = z_n^2 + c,\quad z_0 = 0,
$$
for complex values $c$ on the grid $[-2,1]\times[-1.5,1.5]$.  
Each point is iterated 200 times with a divergence threshold of 50 to determine whether it remains bounded.  
The result is a grayscale fractal visualization highlighting the boundary between stable and divergent regions.

### 2) Markov Chain Simulation
A $5\times5$ stochastic transition matrix $\mathbf{P}$ and an initial probability vector $\mathbf{p}$ are generated randomly and normalized.  
The chain evolves through
$$
\hat{\mathbf{p}} = \mathbf{P}^T \mathbf{p},
$$
iterated 50 times to obtain $\mathbf{p}_{50}$.  

The stationary distribution $\mathbf{v}$ is the eigenvector of $\mathbf{P}^T$ for eigenvalue 1, and convergence is verified when
$$
\bigl\lvert \mathbf{p}_{50} - \mathbf{v} \bigr\rvert < 10^{-5}.
$$

### 3) Taylor Series Approximation
The function
$$
f(x) = x\sin^2(x) + \cos(x)
$$
is approximated on $[-10,10]$ using its Taylor series about $c=0$ up to degree $m=99$:  
$$
f(x) \approx \sum_{n=0}^{m} \frac{f^{(n)}(c)}{n!}(x-c)^n.
$$
A factorial study compares accuracy and runtime for varying $m$, showing decreasing error and stable computational cost.
Python scripts used for these simulations are attached here and they are well commented for readability.

