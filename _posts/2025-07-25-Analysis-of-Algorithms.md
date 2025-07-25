---
title: "Generating Functions"
categories:
  - Blog
tags:
  - Analysis of Algorithms
  - Generating Functions
---

Let $a_k = 2^{k+1}$.

The ordinary generating function is:
$$A(x) = \sum_{k=0}^{\infty} a_k x^k = \sum_{k=0}^{\infty} 2^{k+1} x^k$$

Factor out the constant:
$$2^{k+1} = 2 \cdot 2^k$$

So:
$$A(x) = \sum_{k=0}^{\infty} 2 \cdot 2^k x^k = 2 \sum_{k=0}^{\infty} (2x)^k$$

This is a geometric series with ratio $r = 2x$, which converges for $|x| < \frac{1}{2}$. The sum of a geometric series is:
$$\sum_{k=0}^{\infty} r^k = \frac{1}{1 - r}$$

Therefore:
$$A(x) = 2 \cdot \frac{1}{1 - 2x}$$

Final result:
$$\boxed{\sum_{k=0}^{\infty} 2^{k+1} x^k = \frac{2}{1 - 2x}}$$
