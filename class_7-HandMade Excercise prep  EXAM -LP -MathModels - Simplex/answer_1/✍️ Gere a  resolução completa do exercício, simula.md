
# 📊 Linear Programming Model — Production Optimization

## ✅ Problem Statement

A company, after going through a production streamlining process, ended up with the availability of 3 productive resources: **R1**, **R2**, and **R3**.

A study on resource usage showed the possibility of producing two products: **P1** and **P2**. After evaluating costs and consulting the sales department, it was found that:

- **P1 yields a profit of 120 monetary units per unit**
- **P2 yields a profit of 150 monetary units per unit**

The production department provided the following **resource usage** table:

| Product | R1/unit | R2/unit | R3/unit |
|---------|---------|---------|---------|
| **P1**  |    2    |    3    |    5    |
| **P2**  |    4    |    0    |    3    |

And the **monthly resource availability**:

| Resource | Monthly Availability |
|----------|----------------------|
| **R1**   | 100                  |
| **R2**   | 90                   |
| **R3**   | 120                  |

---

## 🎯 Objective

Mathematically model the **Linear Programming (LP)** problem to **maximize profit** under resource constraints.

---

## 🧠 Step-by-Step Modeling

### 1. 🧮 Decision Variables

Let:

x₁ = quantity produced of product P1
x₂ = quantity produced of product P2

Or in LaTeX (for use in documents):

```latex
x_1 = \text{quantity produced of product P1} \\
x_2 = \text{quantity produced of product P2}



⸻

2. 📈 Objective Function

Maximize total profit:

\text{Maximize } Z = 120x_1 + 150x_2



⸻

3. 📏 Resource Constraints

Each resource has limited availability:
	•	R1 constraint:

2x_1 + 4x_2 \leq 100

	•	R2 constraint:

3x_1 \leq 90

	•	R3 constraint:

5x_1 + 3x_2 \leq 120



⸻

4. 🚫 Non-Negativity Constraints

We cannot produce a negative quantity of products:

x_1 \geq 0, \quad x_2 \geq 0



⸻

🧾 Complete Mathematical Model

\boxed{
\begin{cases}
\text{Maximize } Z = 120x_1 + 150x_2 \\
2x_1 + 4x_2 \leq 100 \\
3x_1 \leq 90 \\
5x_1 + 3x_2 \leq 120 \\
x_1 \geq 0, \quad x_2 \geq 0
\end{cases}
}



⸻

## 📌 Summary Tables

### 🔢 Profit per Product

| Product | Profit per Unit (u.m.) |
|:--------|:----------------------:|
| **P1**  | 120                    |
| **P2**  | 150                    |

---

### 🧰 Resource Usage per Unit

| Product | R1/unit | R2/unit | R3/unit |
|:--------|:-------:|:-------:|:-------:|
| **P1**  |   2     |   3     |   5     |
| **P2**  |   4     |   0     |   3     |

---

### 📦 Monthly Resource Availability

| Resource | Available Units |
|:---------|:----------------:|
| **R1**   |      100         |
| **R2**   |       90         |
| **R3**   |      120         |


⸻

🧠 Notes
	•	This LP model can be solved using methods such as the Simplex Algorithm.
	•	Can also be implemented in software such as Python (PuLP), MATLAB, or Excel Solver.

