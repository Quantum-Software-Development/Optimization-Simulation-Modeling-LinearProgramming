  #  🐍Linear Programming Problem – Simplex Method using Python

This example presents a complete, step-by-step solution to a **Linear Programming (LP)** problem using the **Simplex Method**, along with a basic **Python implementation**.

## 🧮 Problem Statement

**Maximise:**

Z = 4x₁ + 3x₂

**Subject to:**

x₁ + 3x₂ ≤ 7  
2x₁ + 2x₂ ≤ 8  
x₁ + x₂ ≤ 3  
x₂ ≤ 2  
x₁ ≥ 0, x₂ ≥ 0

## ✅ Standard Form Conversion

Introduce slack variables: s₁, s₂, s₃, s₄

The system becomes:


$x_1 + 3x_2 + s_1 = 7$  
$2x_1 + 2x_2 + s_2 = 8$  
$x_1 + x_2 + s_3 = 3$  
$x_2 + s_4 = 2$  
$x_1,\ x_2,\ s_1,\ s_2,\ s_3,\ s_4 \geq 0$

\
\begin{aligned}
\text{Max.} \quad & Z = 4x_1 + 3x_2 \\
\text{S.a.} \quad & 
\begin{cases}
x_1 + 3x_2 + s_1 = 7 \\
2x_1 + 2x_2 + s_2 = 8 \\
x_1 + x_2 + s_3 = 3 \\
x_2 + s_4 = 2 \\
x_1,\, x_2,\, s_1,\, s_2,\, s_3,\, s_4 \geq 0
\end{cases}
\end{aligned}
\

x₁ + 3x₂ + s₁ = 7  
2x₁ + 2x₂ + s₂ = 8  
x₁ + x₂ + s₃ = 3  
x₂ + s₄ = 2  
x₁, x₂, s₁, s₂, s₃, s₄ ≥ 0

## 📊 Initial Simplex Tableau

| Base | x₁ | x₂ | s₁ | s₂ | s₃ | s₄ | RHS |
|------|----|----|----|----|----|----|-----|
| s₁   | 1  | 3  | 1  | 0  | 0  | 0  | 7   |
| s₂   | 2  | 2  | 0  | 1  | 0  | 0  | 8   |
| s₃   | 1  | 1  | 0  | 0  | 1  | 0  | 3   |
| s₄   | 0  | 1  | 0  | 0  | 0  | 1  | 2   |
| **Z**| -4 | -3 | 0  | 0  | 0  | 0  | 0   |

## 🔄 Iterations Overview

###  Iteration 1

- **Entering variable**: x₁ (most negative in Z row)  
- **Leaving variable**: s₃ (minimum ratio = 3)  
- Pivot to bring x₁ into the basis.  

Updated tableau shows next candidate as:  
- **Entering variable**: x₂  
- **Leaving variable**: s₁ or s₄ (tie – choose s₁)

### Iteration 2

After pivoting x₂ into the basis, tableau is updated again.  
Now the most negative coefficient in the Z row is for s₃, but:  
- No valid pivot is possible (no positive coefficients in that column).  
- Hence, no further improvement is feasible.

## 🏁 Final Optimal Solution

The optimal solution was reached at the end of Iteration 1:

x₁ = 3  
x₂ = 0  
Z(max) = 12

**All constraints are satisfied.**

---

## 🐍 Python Code – Simplex Solver (Basic Version)

```python
from scipy.optimize import linprog

# Coefficients of the objective function (to maximise Z = 4x₁ + 3x₂)
# Convert to minimisation: -Z
c = [-4, -3]

# Coefficients of the inequality constraints (Ax ≤ b)
A = [
    [1, 3],
    [2, 2],
    [1, 1],
    [0, 1]
]

b = [7, 8, 3, 2]

# Bounds for x₁ and x₂: both ≥ 0
x_bounds = (0, None)
bounds = [x_bounds, x_bounds]

# Solve the problem
res = linprog(c, A_ub=A, b_ub=b, bounds=bounds, method="simplex")

# Output results
if res.success:
    print("Optimal solution found:")
    print(f"x₁ = {res.x[0]:.2f}")
    print(f"x₂ = {res.x[1]:.2f}")
    print(f"Maximum Z = {(-res.fun):.2f}")
else:
    print("No solution found:", res.message)
```
