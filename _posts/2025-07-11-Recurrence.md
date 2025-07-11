---
title: "Post: Recurrence"
categories:
  - Blog
tags:
  - Recurrence
---

The quadratic formula is given by:
$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

### 🔹 Step 1: Start with the recurrence relation

We are given:

$$
A_n = 1 + \frac{2}{N} \sum_{j=1}^{N} A_{j-1}
$$

This expresses $A_n$ in terms of the sum of previous values $A_{j-1}$.

---

### 🔹 Step 2: Multiply both sides by $N$

To eliminate the denominator:

$$
N A_n = N + 2 \sum_{j=1}^{N} A_{j-1}
$$

This is a cleaner form that will help us compare with the previous term.

---

### 🔹 Step 3: Write the same equation for $n-1$

Now write the recurrence for $A_{n-1}$:

$$
A_{n-1} = 1 + \frac{2}{N-1} \sum_{j=1}^{N-1} A_{j-1}
$$

Multiply both sides by $N-1$:

$$
(N-1) A_{n-1} = (N-1) + 2 \sum_{j=1}^{N-1} A_{j-1}
$$

---

### 🔹 Step 4: Subtract the two equations

Subtract the equation for $A_{n-1}$ from the one for $A_n$:

$$
N A_n - (N-1) A_{n-1} = N - (N-1) + 2 \left( \sum_{j=1}^{N} A_{j-1} - \sum_{j=1}^{N-1} A_{j-1} \right)
$$

Simplify:

- Left side: $N A_n - (N-1) A_{n-1}$
- Right side: $1 + 2 A_{N-1}$

So:

$$
N A_n = (N-1) A_{n-1} + 1 + 2 A_{N-1}
$$

---

### 🔹 Step 5: Rearranged form

Bring all terms involving $A_n$ and $A_{n-1}$ together:

$$
N A_n = (N+1) A_{n-1} + 1
$$

This is a **clean recurrence** involving only $A_n$ and $A_{n-1}$.

---

### 🔹 Step 6: Normalize by dividing both sides by $N+1$

Let’s define:

$$
B_n = \frac{A_n}{N+1}
$$

Then:

$$
B_n = \frac{(N+1) A_{n-1} + 1}{N(N+1)} = \frac{A_{n-1}}{N} + \frac{1}{N(N+1)}
$$

---

### 🔹 Step 7: Recursive form of $B_n$

This gives:

$$
B_n = B_{n-1} + \left( \frac{1}{N} - \frac{1}{N+1} \right)
$$

This is a **telescoping sum**.

---

### 🔹 Step 8: Telescoping sum

Starting from $B_0 = 0$, we get:

$$
B_N = \sum_{k=1}^{N} \left( \frac{1}{k} - \frac{1}{k+1} \right) = 1 - \frac{1}{N+1}
$$

---

### 🔹 Step 9: Final result

Since $B_N = \frac{A_N}{N+1}$, we have:

$$
A_N = (N+1) \cdot \left(1 - \frac{1}{N+1} \right) = N
$$

---


