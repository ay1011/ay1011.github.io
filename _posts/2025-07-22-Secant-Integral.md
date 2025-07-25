---
title: "Post: General Formula for Secant Integral"
categories:
  - Blog
tags:
  - Secant
  - Integral
---

Integral of even powers of secant is given by:

$$
\int \sec^{2n}(x) \, dx = 
\left( \sum_{k=0}^{n-1} 
\left( \prod_{j=0}^{k} \frac{2n - 2j - 2}{2n - 2j - 1} \right) 
\sec^{2(n - k - 1)}(x) \right) \tan(x) + C
$$

---

Integral of odd powers of secant is given by:

$$
\int \sec^{2n+1}(x) \, dx = 
\sum_{k=0}^{n} 
\left( \prod_{j=0}^{k} \frac{2n - 2j - 1}{2n + 1 - 2j} \right) 
\tan(x) \sec^{2n + 1 - 2(k+1)}(x) + 
\left( \prod_{j=0}^{n-1} \frac{2n - 2j - 1}{2n + 1 - 2j} \right) 
\ln|\sec(x) + \tan(x)| + C
$$

---

## Recursive Derivation of $\int \sec^{11}(x) \, dx$

Let $s = \sec(x)$, $t = \tan(x)$. We use the recursive formula:

$$
\int \sec^{2n+1}(x) \, dx = \frac{1}{2n} \tan^{2n-1}(x) \sec(x) + \frac{2n - 1}{2n} \int \sec^{2n-1}(x) \, dx
$$

---

### Step-by-step Expansion

$$
\begin{aligned}
\int \sec^{11}(x) \, dx &= \frac{1}{10} \tan^9(x) \sec(x) + \frac{9}{10} \int \sec^9(x) \, dx \\
&= \frac{1}{10} \tan^9(x) \sec(x) + \frac{9}{10} \left( \frac{1}{8} \tan^7(x) \sec^3(x) + \frac{7}{8} \int \sec^7(x) \, dx \right) \\
&= \frac{1}{10} \tan^9(x) \sec(x) + \frac{9}{10 \cdot 8} \tan^7(x) \sec^3(x) + \frac{9 \cdot 7}{10 \cdot 8} \int \sec^7(x) \, dx \\
&= \frac{1}{10} \tan^9(x) \sec(x) + \frac{9}{10 \cdot 8} \tan^7(x) \sec^3(x) + \frac{9 \cdot 7}{10 \cdot 8} \left( \frac{1}{6} \tan^5(x) \sec^5(x) + \frac{5}{6} \int \sec^5(x) \, dx \right) \\
&= \frac{1}{10} \tan^9(x) \sec(x) + \frac{9}{10 \cdot 8} \tan^7(x) \sec^3(x) + \frac{9 \cdot 7}{10 \cdot 8 \cdot 6} \tan^5(x) \sec^5(x) + \frac{9 \cdot 7 \cdot 5}{10 \cdot 8 \cdot 6} \int \sec^5(x) \, dx \\
&= \frac{1}{10} \tan^9(x) \sec(x) + \frac{9}{10 \cdot 8} \tan^7(x) \sec^3(x) + \frac{9 \cdot 7}{10 \cdot 8 \cdot 6} \tan^5(x) \sec^5(x) + \frac{9 \cdot 7 \cdot 5}{10 \cdot 8 \cdot 6} \left( \frac{1}{4} \tan^3(x) \sec^7(x) + \frac{3}{4} \int \sec^3(x) \, dx \right) \\
&= \frac{1}{10} \tan^9(x) \sec(x) + \frac{9}{10 \cdot 8} \tan^7(x) \sec^3(x) + \frac{9 \cdot 7}{10 \cdot 8 \cdot 6} \tan^5(x) \sec^5(x) + \frac{9 \cdot 7 \cdot 5}{10 \cdot 8 \cdot 6 \cdot 4} \tan^3(x) \sec^7(x) + \frac{9 \cdot 7 \cdot 5 \cdot 3}{10 \cdot 8 \cdot 6 \cdot 4} \int \sec^3(x) \, dx \\
&= \frac{1}{10} \tan^9(x) \sec(x) + \frac{9}{10 \cdot 8} \tan^7(x) \sec^3(x) + \frac{9 \cdot 7}{10 \cdot 8 \cdot 6} \tan^5(x) \sec^5(x) + \frac{9 \cdot 7 \cdot 5}{10 \cdot 8 \cdot 6 \cdot 4} \tan^3(x) \sec^7(x) + \frac{9 \cdot 7 \cdot 5 \cdot 3}{10 \cdot 8 \cdot 6 \cdot 4 \cdot 2} \tan(x) \sec^9(x) \\
&\quad + \frac{9 \cdot 7 \cdot 5 \cdot 3 \cdot 1}{10 \cdot 8 \cdot 6 \cdot 4 \cdot 2} \ln|\sec(x) + \tan(x)| + C
\end{aligned}
$$

---

### Final Expression

Substituting each layer into the previous one:

$$
\begin{aligned}
\int \sec^{11}(x) \, dx &= 
\frac{1}{10} \tan^9(x) \sec(x) +
\frac{9}{10 \cdot 8} \tan^7(x) \sec^3(x) +
\frac{9 \cdot 7}{10 \cdot 8 \cdot 6} \tan^5(x) \sec^5(x) \\
&\quad +
\frac{9 \cdot 7 \cdot 5}{10 \cdot 8 \cdot 6 \cdot 4} \tan^3(x) \sec^7(x) +
\frac{9 \cdot 7 \cdot 5 \cdot 3}{10 \cdot 8 \cdot 6 \cdot 4 \cdot 2} \tan(x) \sec^9(x) \\
&\quad +
\frac{9 \cdot 7 \cdot 5 \cdot 3 \cdot 1}{10 \cdot 8 \cdot 6 \cdot 4 \cdot 2} \ln|\sec(x) + \tan(x)| + C
\end{aligned}
$$

[Source](http://galileo.math.siu.edu/Courses/250/F03/sec.pdf)
