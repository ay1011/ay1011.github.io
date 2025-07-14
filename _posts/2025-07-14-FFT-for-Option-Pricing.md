---
title: "Post: FFT for Option Pricing"
categories:
  - Blog
tags:
  - FFT
  - Option Pricing
---

Given a sequence of values $x_0, x_1, \ldots, x_{n-1}$, the Discrete Fourier Transform (DFT) is defined as a sequence $X_0, X_1, \ldots, X_{n-1}$, where:

$$
X_k = \frac{1}{\sqrt{n}} \sum_{j=0}^{n-1} x_j e^{i \frac{2\pi}{n} jk}
$$

The Fourier transform of a sequence is often written as:

$$
X = \mathcal{F}(x)
$$

