# Simultaneous Adaptive Chirplet Transform

Simultaneous optimization for the adaptive chirplet transform parameters using modern deep learing optimizers in TensorFlow.

## Introduction

The adaptive chirplet transform algorith seeks to sparsely approximate a target signal as the sum of [chirplets](http://wearcam.org/chirplet.htm). This problem is NP-hard and traditionally makes use of matching pursuit and expectation-maximization algorithms.

The main problem with applying more convenient differential optimization methods is that there are usually many local optima for sparse approximations. However, as the number of chirplets (i.e., optimization parameters) increases, the probability of a zero gradient grows smaller.

## Goal

In this repository I seek to understand the applicability of modern gradient-based optimizers to this problem. In particular, I attempt to answer the following questions:

 1. Constrained vs. unconstrained optimization: What happens when projection is used to calculate chirplet coefficients vs. directly optimizing them with gradient descent? How does this vary with the number of chirplets used?
 2. Adaptive pruning/l1 regularization: This approach is likely to work well for a large number of chirplets. How can adaptive pruning methods and regularization techniques be applied to approach optimal performance on sparse approximations? How does this compare to the [original](https://github.com/amanb2000/Adaptive_Chirplet_Transform) adaptive chirplet transform algorithm performance?
 3. Monte Carlo methods for optimal approximation: To what extent does randomization of (2) help with the efficient generation of optimal sparse signal approximations?
 4. Fitting chirplets to a large dataset: How does the number of signals to fit in the dataset affect the applicability of the proposed methods for generating sparse representations? 




