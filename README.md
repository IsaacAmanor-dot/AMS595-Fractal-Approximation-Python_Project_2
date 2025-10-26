# **AMS595-Fractal-Approximation**

This repository contains the complete implementation and analysis for **Python Project 2: Fractal Approximation**, completed as part of **AMS 595 / DCS 525 (Scientific Programming)** at **Stony Brook University**.  
The project demonstrates three numerical modeling techniques — **iterative complex dynamics**, **stochastic simulation**, and **analytic function approximation** — implemented in Python with supporting visualizations and data analysis.

---

## **Project Overview**

### **1. Mandelbrot Set Generation**
The Mandelbrot Set is constructed using the recurrence  
\[
z_{n+1} = z_n^2 + c, \quad z_0 = 0,
\]
for complex values \(c\) on the grid \([-2,1]\times[-1.5,1.5]\).  
Each point is iterated 200 times with a divergence threshold of 50 to determine whether it remains bounded.  
The result is a grayscale fractal visualization highlighting the boundary between stable and divergent regions.

### **2. Markov Chain Simulation**
A \(5\times5\) stochastic transition matrix \(\mathbf{P}\) and an initial probability vector \(\mathbf{p}\) are generated randomly and normalized.  
The chain evolves through the rule  
\[
\hat{\mathbf{p}} = \mathbf{P}^T \mathbf{p},
\]
iterated 50 times to obtain \(\mathbf{p}_{50}\).  
The stationary distribution \(\mathbf{v}\) is found as the eigenvector of \(\mathbf{P}^T\) associated with eigenvalue 1, and convergence is verified when  
\[
|\mathbf{p}_{50} - \mathbf{v}| < 10^{-5}.
\]

### **3. Taylor Series Approximation**
The function  
\[
f(x) = x\sin^2(x) + \cos(x)
\]
is approximated on \([-10,10]\) using its Taylor series about \(c=0\) up to degree \(m=99\).  
A factorial study compares accuracy and runtime for varying degrees, showing decreasing error and stable computational cost.

---

## **Repository Structure**

# AMS595-Fractal-Approximation-Python_Project_2
Python implementation of the Mandelbrot Set, Markov Chain simulation, and Taylor Series approximation with factorial analysis for AMS 595 / DCS 525 Project 2.
