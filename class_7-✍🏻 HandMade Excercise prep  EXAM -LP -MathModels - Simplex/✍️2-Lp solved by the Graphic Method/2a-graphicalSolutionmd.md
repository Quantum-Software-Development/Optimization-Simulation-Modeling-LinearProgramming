# 📈 Graphical Solution to the Linear Programming (LP) Problem

**Objective:**

Maximize  
$$
Z = 4x_1 + 3x_2
$$

**Subject to:**

$$
\begin{cases}
x_1 + 3x_2 \leq 7 \\
2x_1 + 2x_2 \leq 8 \\
x_1 + x_2 \leq 3 \\
x_2 \leq 2 \\
x_1 \geq 0, \quad x_2 \geq 0
\end{cases}
$$

---

## Step 1: Plot the Constraints

Convert inequalities into equalities to draw the lines:

1. $x_1 + 3x_2 = 7$
   - If $x_1 = 0 \Rightarrow x_2 = \frac{7}{3} \approx 2.33$
   - If $x_2 = 0 \Rightarrow x_1 = 7$

2. $2x_1 + 2x_2 = 8$
   - If $x_1 = 0 \Rightarrow x_2 = 4$
   - If $x_2 = 0 \Rightarrow x_1 = 4$

3. $x_1 + x_2 = 3$
   - If $x_1 = 0 \Rightarrow x_2 = 3$
   - If $x_2 = 0 \Rightarrow x_1 = 3$

4. $x_2 = 2$ → horizontal line

---

## Step 2: Identify the Feasible Region

- The feasible region is the intersection of all shaded regions that satisfy the constraints.
- Must include $x_1 \geq 0$ and $x_2 \geq 0$.

---

## Step 3: Find Intersection Points (Vertices)

1. Intersection of $x_1 + 3x_2 = 7$ and $2x_1 + 2x_2 = 8$:
   - Multiply first by 2: $2x_1 + 6x_2 = 14$
   - Subtract: $4x_2 = 6 \Rightarrow x_2 = 1.5$, $x_1 = 2.5$
   - Point: **(2.5, 1.5)**

2. Intersection of $x_1 + 3x_2 = 7$ and $x_1 + x_2 = 3$:
   - Subtract: $2x_2 = 4 \Rightarrow x_2 = 2$, $x_1 = 1$
   - Point: **(1, 2)**

3. Intersection of $x_1 + x_2 = 3$ and $x_2 = 2$:
   - $x_1 = 1$
   - Point: **(1, 2)**

4. Intersection of $2x_1 + 2x_2 = 8$ and $x_2 = 2$:
   - $x_1 = 2$
   - Point: **(2, 2)**

5. $x_1 + x_2 = 3$ and $x_1 = 0 \Rightarrow x_2 = 3$ ❌ (Invalid since $x_2 \leq 2$)

6. $x_1 + 3x_2 = 7$ and $x_1 = 0 \Rightarrow x_2 = 7/3 \approx 2.33$ ❌ (Invalid since $x_2 \leq 2$)

---

## Step 4: Evaluate Objective Function at Each Vertex

Feasible Vertices:

- A: (0, 0)
- B: (0, 2)
- C: (1, 2)
- D: (2, 2)
- E: (2, 0)
- F: (3, 0)

| Point | $x_1$ | $x_2$ | $Z = 4x_1 + 3x_2$ |
|:-----:|:-----:|:-----:|:-----------------:|
| A     | 0     | 0     | 0                 |
| B     | 0     | 2     | 6                 |
| C     | 1     | 2     | 10                |
| D     | 2     | 2     | 14 ❌             |
| E     | 2     | 0     | 8                 |
| F     | 3     | 0     | 12                |

---

## Step 5: Check Feasibility

- **(2,2)** violates: $x_1 + 3x_2 = 2 + 6 = 8 > 7$ ❌
- All others: ✅

---

## ✅ Final Step: Choose the Best Feasible Point

| Point | $Z$ | Feasible |
|:-----:|:---:|:--------:|
| A     | 0   | Yes      |
| B     | 6   | Yes      |
| C     | 10  | Yes      |
| E     | 8   | Yes      |
| F     | 12  | ✅ Best   |
| D     | 14  | No       |

---

## 🏁 Conclusion

- **Optimal solution:** $x_1 = 3$, $x_2 = 0$
- **Maximum value:** $Z = 12$