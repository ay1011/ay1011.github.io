---
title: "Post: Recurrence"
categories:
  - Blog
tags:
  - Recurrence
---

### 🔹 Step 1: Start with the recurrence relation

$$
A_n = 1 + \frac{2}{N} \sum_{j=1}^{N} A_{j-1}
$$

---

### 🔹 Step 2: Multiply both sides by $N$

$$
N A_n = N + 2 \sum_{j=1}^{N} A_{j-1}
$$

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

$$
N A_n = (N-1) A_{n-1} + 1 + 2 A_{N-1}
$$

---

### 🔹 Step 5: Rearranged form

Bring all terms involving $A_n$ and $A_{n-1}$ together:

$$
N A_n = (N+1) A_{n-1} + 1
$$

---

### 🔹 Step 6: Normalize by dividing both sides by $N+1$

Define:

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


