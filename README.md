
<br>

#  <p align="center">  Integrated Mathematics Projects 
####  <p align="center">  LOGISTICS, FINANCE, CREDIT, ENGINEERING, HEALTH AND OTHERS
#####  <p align="center">  [Optimization / Modeling and Simulation / Linear Programming / Graphic Method - Maximization and Minimization/ Simplex Algorithm / Matrix / Mathematical Modeling]()


<br><br>

### This Repo is focused on mathematical concepts, taught during the third semester of the Data Science and Artificial Intelligence bachelor's program at PUC-SP in 2025, under the instruction of [***Professor Doctor in Mathematics Daniel Rodrigues da Silva***](https://www.linkedin.com/in/daniel-rodrigues-048654a5/)


<br><br>


<!--### <p align="center">  <img src="https://github.githubassets.com/images/icons/emoji/octocat.png" width="46">  -->
### <p align="center"> [![Sponsor Quantum Software Development](https://img.shields.io/badge/Sponsor-Quantum%20Software%20Development-brightgreen?logo=GitHub)](https://github.com/sponsors/Quantum-Software-Development)


<br><br>


#### ➣ [Access Geogebra](https://www.geogebra.org/download?lang=pt)

#### ➣ [Access Tutoril]() about solving LP problems using [Geogebra](https://youtu.be/nHYNeWIDd3g?si=n_UaKVjFmTM1Nhst)

#### ➢ [Access PHPSimplex](https://www.phpsimplex.com/pt/)



#### ➢ [Analytics4All](https://analytics4all.org/2016/06/08/phpsimplex-simplex-linear-programming/)


<br><br>

## [Introduction to optimization problems and their basic properties]():

Constrained and unconstrained optimization. Linear Programming: formulation, geometric solution, simplex method, and duality. Network flow models: Transportation, Assignment, Shortest Path, and Maximum Flow problems. Integer programming. Multiobjective programming. Monte Carlo and discrete event simulation.


Optimization and simulation are two key areas in Operations Research, used for problem-solving and decision-making, but they approach these tasks differently[4][5]. Simulation creates a virtual model to analyze a system's behavior under various conditions, allowing for experimentation by varying parameters[1]. Optimization, on the other hand, employs mathematical algorithms to identify the best configuration of these parameters, aiming to maximize or minimize a specific objective, such as reducing costs or increasing efficiency[1][2].

**[Sim-Opt]() (Simulation-Optimization)**
Sim-opt combines simulation and optimization techniques to provide a comprehensive and dynamic understanding of a system[1]. This approach integrates real-world uncertainties with the search for ideal solutions[1]. By simulating the impact of each parameter and comparing it to an ideal scenario, sim-opt helps identify the factors that most influence a system's performance, leading to more strategic decisions[1].

<br>

**[Benefits]() of Sim-Opt**
*   **[Analyzing uncertain scenarios]():** Sim-opt evaluates the impact of unpredictable events and helps plan strategies to manage risks[1].
*   **[Optimizing processes]():** It identifies bottlenecks and opportunities for improvement and defines the best practices for various situations[1].
*   **[Making informed decisions]():** Sim-opt bases decisions on data and simulations, reducing uncertainty and the risk of errors[1].

<br>

**[How to Implement Optimization]() in Simulation Models**

1.  **[Define decision variables]():** Identify the variables that affect the simulation model's outputs and will be tested by the optimization algorithm[3].
2.  **[Define variable types and limits]():** Determine whether each decision variable is real or integer and set lower and upper limits. The optimization algorithm will search for solutions within these limits[3].
3.  **[Define the objective function]():** Establish a function to evaluate the solutions tested by the algorithm. This function can be designed to minimize, maximize, or use both types of variables, depending on the study's objectives[3].
4.  **[Select population size]():** Choose the number of solutions for the evolutionary algorithm. The population size affects the reliability and time required for the search. Also, define other parameters such as the required precision, significance level, and number of replications[3].
5.  **[Analyze solutions]():** After the search, analyze the solutions found. Compare all solutions based on the objective function to identify the best and other competitive solutions[3].

<br>

The [key difference]() between sim-opt and other analytical tools is its [ability to model the complexity and dynamics of real-world systems](), including data uncertainty and variability[1]. This allows for the creation of more robust and adaptable plans[1].

<br><br>

# I- Example of a [Optimization Problem]()

#### ➢ [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/blob/8e3cf8ba6bdc2ce92a011ff5169a3ec704a9d6f0/class_1-Optimization-Simulation-Modelin/1-Optimization%20and%20Simulation.pdf) to access Theoretical and Pratical Material. 

<br>

### An optimization problem can be represented using the `optidef` package. For example:

$$
\begin{aligned}
    &\min_{x} f(x) \\
    &\text{subject to } x \geq 0
\end{aligned}
$$


```latex
\begin{aligned}
    &\min_{x} f(x) \\
    &\text{subject to } x \geq 0
\end{aligned}
```

<br>


## [Simplex Algorithm]()

The simplex algorithm is used to solve linear problems. Although there isn't a specific command for it, we can describe it in text or use tables to show the steps of the algorithm.

<br>

### [Matrix]():

A matrix can be created using the `amsmath` package:

$$
A =
\begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{bmatrix}
$$

```latex
A =
\begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{bmatrix}
```

<br>

### [Simulation]():

Simulation generally involves complex mathematical models that can be described using differential or integral equations.

$$
y(t) = A e^{kt}
$$

```latex
\y(t) = A e^{kt}
```
<br>

##### ➢ [***Note***](): ***This equation represents a simple solution to an ordinary differential equation.***

<br><br>

# II- [Modeling - Writing Mathematical Models]()

#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/blob/6a19c6fa9a8b255e1d21bb7d2c5d1ede61f5faf1/class_2-Modeling-Writing%20Mathematical%20Model%20s/2-Optimization%20and%20Simulation%20Modeling.pdf) to access Theoretical and Pratical Material. 

#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/tree/8e6e2abf64164103aba57d65a58ce19490ea3361/class_2-Modeling-Writing%20Mathematical%20Model%20s/Manually%20solved%20exercises) and access exercises manually solved.

#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/tree/d9ba27da44bc9e19a5c9239a8aeb8ea4eb0da24d/class_2-Modeling-Writing%20Mathematical%20Model%20s/Extra%20Excercises) and access extras exercises 

<br>

### [Example](): Maximizing Profit for a Chocolate Manufacturer

A chocolate manufacturer has a stock of chocolates, consisting of 130 kg with cherry filling and 170 kg with mint filling. He decides to sell the stock in the form of two different assorted packages. One package contains a mix with half the weight in cherry chocolates and half in mint chocolates and sells for R$ 20.00 per kg. The other package contains a mix of one-third cherry chocolates and two-thirds mint chocolates and sells for R$ 12.50 per kg. How many kilograms of each mix should the seller prepare to maximize his sales profit?

### [Solution]():

###  ***Objective Function***

### ➢ [Maximize]():

$$
Z = 20x_1 + 12.5x_2
$$

```latex
Z = 20x_1 + 12.5x_2
```

<br>

### ➣ [Subject to Constraints]():

$$
\begin{cases}
    \frac{x_1}{2} + \frac{x_2}{3} \leq 130 \\
    \frac{x_1}{2} + \frac{2x_2}{3} \leq 170 \\
    x_1 \geq 0, \quad x_2 \geq 0
\end{cases}
$$

```latex
\begin{cases}
    \frac{x_1}{2} + \frac{x_2}{3} \leq 130 \\
    \frac{x_1}{2} + \frac{2x_2}{3} \leq 170 \\
    x_1 \geq 0, \quad x_2 \geq 0
\end{cases}
```

<br>

### ➢ [Solution Steps]():


1. Express the cherry chocolate constraint:

$$\frac{x_1}{2} + \frac{x_2}{3} \leq 130$$

```latex
\frac{x_1}{2} + \frac{x_2}{3} \leq 130
```

 <br>  
   
2. Express the mint chocolate constraint:
   
$$\frac{x_1}{2} + \frac{2x_2}{3} \leq 170$$

```latex
\frac{x_1}{2} + \frac{2x_2}{3} \leq 170
```

<br><br>
   
## [Solve the system using the **Simplex Method** or an optimization tool]()

<br>

### [Optimal Solution]():

#### Solving the system yields:

$$
(x_1, x_2) = (180, 120)
$$


```latex
\(x_1, x_2) = (180, 120)
```

<br>

### [Maximum Profit Calculation]()

$$
Z = 20(180) + 12.5(120)
$$


```latex
\Z = 20(180) + 12.5(120)
```

<br> 

$$
Z = 3600 + 1500 = 5100
$$

<br>

Thus, the maximum profit achievable is [**R$ 5,100**]().


<br><br>


# III- [Graphical Method for Linear Programming]() (LP)

#### ➢ [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/blob/910094081c2f3be40f14dacf4ec2c56de3d7aa83/class_3-Graphic%20Method/3-Graphic%20Method.pdf) to access Theoretical and Pratical Material.

#### ➣ [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/tree/bcf9b6ae4da82dba29644bd2599e54e86f5c8188/class_3-Graphic%20Method/Manually%20solved%20exercises) and access solved exercises manually

<br>

The **graphical method** for solving simple linear programming (LP) problems involving **two decision variables**. The graphical method provides a visual way to understand the constraints, the feasible region, and how to find the optimal solution that either maximizes or minimizes the objective function.

#

### [Key]() Concepts:

- **[Decision Variables]():** These are the variables that we want to determine the values of to optimize the ***[OBJECTIVE FUNCTION]()*** (e.g.):

  $$\(x_1\)$$ and $$\(x_2\)$$

<br>
 
- **[Objective Function]():** This is the linear function that we aim to maximize or minimize. For example:

  $$\max/\min \quad Z$$ = $$c_1x_1 + c_2x_2$$

  ```latex
    Max/Min \quad Z = c_1x_1 + c_2x_2
    ```

<br>

- **[Constraints]():** These are linear inequalities or equalities that restrict the values the decision variables can take.
  - [Equality constraint]():

  $$a_{i1}x_1 + a_{i2}x_2$$ = $$b_i$$

  ```latex
   a_{i1}x_1 + a_{i2}x_2 = b_i
   ```

  <br>


  - [Less than or equal to constraint]():

   $$a_{i1}x_1$$ + $$a_{i2}x_2 \leq b_i$$

   ```latex
   a_{i1}x_1 + a_{i2}x_2 \leq b_i
   ```
    <br>

  - [Greater than or equal to constraint]():

    $$a_{i1}x_1$$ + $$a_{i2}x_2 \geq b_i$$

  ```latex
  a_{i1}x_1 + a_{i2}x_2 \geq b_i
  ```


    <br>


- **[Feasible Solution]():** A solution $\(x_1, x_2)\$ that satisfies all the constraints of the problem.
- **[Feasible Region]():** The set of all feasible solutions. Graphically, this is a subregion of the plane formed by the intersection of the regions defined by the constraints. The feasible region is often a **convex polygon**.
- **[Boundary Line]():** Each equality constraint or the equality part of an inequality constraint represents a straight line in the graph.
- **[Semiplane]():** Each inequality constraint defines a half-plane on one side of its boundary line, including the line itself. The feasible region is the intersection of these semiplanes.
- **[Vertices]() (Extreme Points):** The corner points of the feasible region, formed by the intersection of two or more boundary lines.
- **[Optimal Solution]():** A feasible solution that yields the best (maximum for maximization problems, minimum for minimization problems) value of the objective function.


<br>


## [Steps to Solve Graphically]()

<br>

1. **[Plot the Constraints]():** FFor each constraint, treat it as an equality and plot the corresponding straight line on the Cartesian plane ($x_1$ on the horizontal axis, $x_2$ on the vertical axis) [3].

 <br>

2. **[Identify the Feasible Region]():** For each inequality constraint, determine which side of the line satisfies the inequality. This can be done by testing a point (e.g., the origin $\(0,0)\)$; if it's not on the line) in the inequality. The feasible region is the area where all the shaded regions of the inequalities overlap. If there are non-negativity constraints $\(x_1 \geq 0\)$ and $\(x_2 \geq 0\)$, the feasible region will be in the **[first quadrant]()** [3].

 <br>

3.  **[Identify the Vertices]():** Determine the coordinates of all the vertices (corner points) of the feasible region [4, 6]. These are the points where the boundary lines intersect.

 <br>
 
4.  **[Evaluate the Objective Function at Each Vertex]():** Substitute the coordinates of each vertex into the objective function to find the value of the objective function at that point [6].


 <br>

5.  **[Determine the Optimal Solution]():**
    *   For a **maximization** problem, the vertex that yields the **largest** value of the objective function is the optimal solution [1, 6].
    *   For a **minimization** problem, the vertex that yields the **smallest** value of the objective function is the optimal solution [2, 7].


<br><br>

## [Possible Scenarios]()

*   **Unique Optimal Solution:** The objective function achieves its maximum or minimum value at a single vertex of the feasible region [3, 5, 6].

*   **Multiple Optimal Solutions:** The objective function achieves its optimal value at more than one point, typically along an edge connecting two adjacent vertices. In this case, all points on that edge are optimal solutions [5].

*   **Unbounded Feasible Region:** If the feasible region extends infinitely in some direction, the objective function might also be unbounded (it can increase or decrease indefinitely without reaching a maximum or minimum value) [5]. However, if an optimal solution exists even with an unbounded region, it will still occur at a vertex [5].

*   **Empty Feasible Region:** If the constraints are inconsistent and there are no points that satisfy all of them simultaneously, the feasible region is empty, and the linear programming problem has no solution [4].

  <br>

## [Theorem on Optimal Solutions]()

If the feasible region of a linear programming problem is **non-empty and bounded**, then the objective function attains both a **maximum and a minimum value**, and these occur at **extreme points (vertices)** of the feasible region [5].

If the feasible region is **unbounded**, and if the objective function attains a maximum or minimum value, it will also occur at an **extreme point (vertex)** [5].

  <br>

## [Examples]()

The source provides several examples [6-8] that illustrate the graphical method for both maximization and minimization problems with different sets of constraints. These examples demonstrate how to plot the constraints, identify the feasible region, find the vertices, and evaluate the objective function to determine the optimal solution and its value. For instance, Example 1 [6] finds the maximum of $x_1 + 2x_2$ subject to several constraints.

  <br>

## [Conclusion about the Graphical Method]()

The graphical method is a useful tool for solving linear programming problems with two decision variables, providing a clear visual representation of the solution process. It helps in understanding the concepts of feasible solutions, feasible regions, and the role of vertices in finding the optimal solution. However, this method is limited to problems with only two decision variables. For problems with more variables, more advanced techniques like the simplex algorithm are required.

<br><br>

# IV- [The Simplex Method]()

#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/blob/5d0f89d3a4d9f67f900463505cb7d4b4e72d186a/class_4-Simplex%20Method/class_4-Simplex%20Method.pdf) to access Theoretical and Pratical Material. 


#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/tree/f9cef4452ad8486d03c8273aa83885de625c2da8/class_4-Simplex%20Method/SIMPLEX%20IMPLEMENT%20and%20CALCULUS%20EXERCISES) and access Simplex Implementation and Calculus Exercises Manually Solved

<br>

# V- [Two-Stage Simplex]()

#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/blob/e09ce2c81b12f47975bdb0ed6b3acd77b2195532/class_6-Two-Stage%20Simplex./two-stage%20simplex..pdf) to access Theoretical and Pratical Material.

#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/tree/83b16e5330d7e467cb5df57827e7d02076ac0f84/class_6-Two-Stage%20Simplex/Exercise_1-Two-StageSimplex-Solved%20with%20Multiple%20Iteraties) and access Two-StageS Simplex with Multiple Iteraties - Implementation and Calculus Exercise Manually Solved

#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/tree/caf816701eac73bdf1289997519ea3560f72956e/class_6-Two-Stage%20Simplex/Exercise_2-Two-StageSimplex-Solved%20with%20Only%20%20One%20Iteration) and access Two-Stage Simplex with Only  One Iteration - Implementation and Calculus Exercise Manually Solved


<br>

# VI - [Excel Solver for Linear Programming - Simplex]()


The Excel Solver is an optimization tool available in Microsoft Excel that allows users to find the optimal solution to decision problems involving constraints and objectives. It can solve linear and nonlinear programming problems by adjusting the values of decision variables to maximize or minimize a target (objective) function, subject to a set of constraints.

<br>

In the context of Linear Programming (LP) and the Simplex Method, Excel Solver can be used to:
	•	Define decision variables (cells that Solver will change);
	•	Set a linear objective function to maximize or minimize;
	•	Specify constraints on variables (e.g., inequalities or equalities);
	•	Use the Simplex LP solving method to compute the optimal solution


  <br>

[***Solver is especially useful in educational settings for visualizing and solving linear optimization problems without requiring programming, making it a powerful tool for teaching and learning operations research.***]()

  <br>


# VII - [Simplex Method using Excel Solver]()

This example shows how to solve a Linear Programming (LP) problem using the **Simplex Method** via **Excel Solver**.

<br>

## [Problem](): 

### [Maximize the objective function]():

Z = 3x + 5y

### [Subject to the constraints]():

x + 2y ≤ 100
2x + y ≤ 80
x, y ≥ 0


<br>


### - [Excel Spreadsheet Setup]():

### **Fill the spreadsheet with the following structure:**

<br>

#### [*Variables and Objective*]()

<br>

| Cell | Description            | Formula / Value      |
|------|------------------------|----------------------|
| B1   | x (Decision Variable)  | *(leave blank)*      |
| B2   | y (Decision Variable)  | *(leave blank)*      |
| B3   | Objective Function Z   | `=3*B1 + 5*B2`        |

<br>

#### [*Constraints Left-Hand Side (LHS)*]()

<br>

| Cell | Description                | Formula             |
|------|----------------------------|---------------------|
| B5   | Constraint 1 LHS           | `=1*B1 + 2*B2`       |
| B6   | Constraint 2 LHS           | `=2*B1 + 1*B2`       |

<br>

#### [*Constraints Right-Hand Side (RHS)*]()

<br>

| Cell | Description                | Value               |
|------|----------------------------|---------------------|
| C5   | Constraint 1 RHS           | `100`               |
| C6   | Constraint 2 RHS           | `80`                |


<br><br>

### - [Solver Configuration (Simplex LP)]():

1. Go to `Data` > `Solver`.
2. Set Objective Cell: `B3`
3. Select: **Max**
4. By Changing Variable Cells: `B1:B2`
5. Add Constraints:
    - `B5 <= C5`
    - `B6 <= C6`
    - `B1 >= 0`
    - `B2 >= 0`
6. Choose **Simplex LP** as the solving method.
7. Click **Solve**.

<br>

### - [Solution]():

After running Solver

x = 20
y = 40
Z = 320 + 540 = 260


Z = 260

<br>

## [Excel Solver Example – Linear Programming with Simplex]()

This example demonstrates how to use Excel Solver to solve a Linear Programming problem using the **Simplex Method**.

<br>

### Problem Statement

### [Maximize]():

Z = 40x + 30y

Subject to:

2x + y ≤ 40
x + 2y ≤ 50
x, y ≥ 0

<br>

### [*Excel Setup*]():

<br>


| Cell | Description              | Formula / Value     |
|------|--------------------------|---------------------|
| B1   | x (Decision Variable)    | (leave blank)       |
| B2   | y (Decision Variable)    | (leave blank)       |
| B3   | Objective Function (Z)   | `=40*B1 + 30*B2`     |
| B5   | Constraint 1 (LHS)       | `=2*B1 + 1*B2`       |
| B6   | Constraint 2 (LHS)       | `=1*B1 + 2*B2`       |

<br>

| Cell | Constraint RHS           | Value               |
|------|--------------------------|---------------------|
| C5   | Constraint 1 (RHS)       | 40                  |
| C6   | Constraint 2 (RHS)       | 50                  |


<br>

### [*Solver Configuration*]():

1. Set Objective: **B3**  
2. To: **Maximize**  
3. By Changing Variable Cells: **B1:B2**  
4. Subject to the Constraints:
   - **B5 <= C5**
   - **B6 <= C6**
   - **B1 >= 0**
   - **B2 >= 0**
5. Choose **Simplex LP** as the solving method.
6. Click **Solve** to find the optimal solution.

<br>

### [*Solution Output*]():

After running Solver:

- **x = 10**
- **y = 20**
- **Z = 40×10 + 30×20 = 1000**

<br>

# VIII - 🐍[Linear Programming Problem – Simplex Method using Python]():

This example presents a complete, step-by-step solution to a **Linear Programming (LP)** problem using the **Simplex Method**, along with a basic **Python implementation**.

## 🧮 [Problem Statement]():

### [**Maximize:**]():

$Z = 4x_1 + 3x_2$

### [**Subject to:**]():

$x_1 + 3x_2 \leq 7$  
$2x_1 + 2x_2 \leq 8$  
$x_1 + x_2 \leq 3$  
$x_2 \leq 2$  
$x_1 \geq 0,\ x_2 \geq 0$


<br>

```latex
\
\begin{aligned}
\text{Max.} \quad & Z = 4x_1 + 3x_2 \\
\text{S.a.} \quad & 
\begin{cases}
x_1 + 3x_2 \leq 7 \\
2x_1 + 2x_2 \leq 8 \\
x_1 + x_2 \leq 3 \\
x_2 \leq 2 \\
x_1 \geq 0 \text{ e } x_2 \geq 0
\end{cases}
\end{aligned}
\
```

<br>

### ✅ Standard Form Conversion:

### [pIntroduce slack variables](): s₁, s₂, s₃, s₄

### [The system becomes]():

<br>

$x_1 + 3x_2 + s_1 = 7$  
$2x_1 + 2x_2 + s_2 = 8$  
$x_1 + x_2 + s_3 = 3$  
$x_2 + s_4 = 2$  
$x_1,\ x_2,\ s_1,\ s_2,\ s_3,\ s_4 \geq 0$

<br>

```latex
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
```
<br>

### 📊 [Initial Simplex Tableau]():

| Base | x₁ | x₂ | s₁ | s₂ | s₃ | s₄ | RHS |
|------|----|----|----|----|----|----|-----|
| s₁   | 1  | 3  | 1  | 0  | 0  | 0  | 7   |
| s₂   | 2  | 2  | 0  | 1  | 0  | 0  | 8   |
| s₃   | 1  | 1  | 0  | 0  | 1  | 0  | 3   |
| s₄   | 0  | 1  | 0  | 0  | 0  | 1  | 2   |
| **Z**| -4 | -3 | 0  | 0  | 0  | 0  | 0   |


<br>

### 🔄 [Iterations Overview]():

####  [Iteration 1]():

- **Entering variable**: x₁ (most negative in Z row)  
- **Leaving variable**: s₃ (minimum ratio = 3)  
- Pivot to bring x₁ into the basis.  

### {Updated tableau shows next candidate as]():  

- **Entering variable**: x₂  
- **Leaving variable**: s₁ or s₄ (tie – choose s₁)

#### [Iteration 2]():

After pivoting x₂ into the basis, tableau is updated again.  
Now the most negative coefficient in the Z row is for s₃, but:  
- No valid pivot is possible (no positive coefficients in that column).  
- Hence, no further improvement is feasible.

<br>

### 🏁 [Final Optimal Solution]():

The optimal solution was reached at the end of Iteration 1]():

x₁ = 3  
x₂ = 0  
Z(max) = 12

**All constraints are satisfied.**

<br>

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

<br>


# IX - [Extras Excercise]():

<br>

## 1- 📊 [Linear Programming Mathematical Model — Production Optimization]()

<br>

### ✅ [Problem Statement]():

A company, after going through a production streamlining process, ended up with the availability of 3 productive resources: **R1**, **R2**, and **R3**.

A study on resource usage showed the possibility of producing two products: **P1** and **P2**. After evaluating costs and consulting the sales department, it was found that:

- **P1 yields a profit of 120 monetary units per unit**
- **P2 yields a profit of 150 monetary units per unit**

<br>

The production department provided the following **resource usage** table:

| Product | R1/unit | R2/unit | R3/unit |
|---------|---------|---------|---------|
| **P1**  |    2    |    3    |    5    |
| **P2**  |    4    |    0    |    3    |

<br>

And the **monthly resource availability**:

| Resource | Monthly Availability |
|----------|----------------------|
| **R1**   | 100                  |
| **R2**   | 90                   |
| **R3**   | 120                  |

<br>

### ➢ [Objective]():

### ***Mathematically model the **Linear Programming (LP)** problem to **maximize profit** under resource constraints***.

<br>

### ➢[Step-by-Step Modeling]()

### 1. [Decision Variables]():

- Let:

x₁ = quantity produced of product P1

x₂ = quantity produced of product P2

<br>

☟ Or in LaTeX (for use in documents):

```latex
x_1 = \text{quantity produced of product P1} \\

x_2 = \text{quantity produced of product P2}
```

<br>

### 2. [Objective Function]():

#### Maximize total profit:

### $\text{Maximize: } Z = 120x_1 + 150x_2$

```latex
\text{Maximize: } Z = 120x_1 + 150x_2
```

<br>

### 3. [Resource Constraints]():

#### Each resource has limited availability:
	
#### ➢ [R1]() Constraint:

### $2x_1 + 4x_2 \leq 100$

```latex
2x_1 + 4x_2 \leq 100
```

#### ➢ [R2]() Constraint:

### $3x_1 \leq 90$

```latex
$3x_1 \leq 90
```

#### ➢ [R3]() Constraint:

### $5x_1 + 3x_2 \leq 120$

```latex
5x_1 + 3x_2 \leq 120
```

<br>

### 4. [Non-Negativity Constraints]()

### ***We cannot produce a negative quantity of products***:

### $x_1 \geq 0, \quad x_2 \geq 0$

```latex
x_1 \geq 0, \quad x_2 \geq 0
```
<br>

### 5. [Complete Mathematical Model]():

<br>

$$
\boxed{
\begin{cases}
\text{Maximize } Z = 120x_1 + 150x_2 \\
2x_1 + 4x_2 \leq 100 \\
3x_1 \leq 90 \\
5x_1 + 3x_2 \leq 120 \\
x_1 \geq 0, \quad x_2 \geq 0
\end{cases}
}
$$

```latex
\boxed{
\begin{cases}
\text{Maximize } Z = 120x_1 + 150x_2 \\
2x_1 + 4x_2 \leq 100 \\
3x_1 \leq 90 \\
5x_1 + 3x_2 \leq 120 \\
x_1 \geq 0, \quad x_2 \geq 0
\end{cases}
}
```
<br>

## 📌 Summary Tables

### 🔢 Profit per Product

| Product | Profit per Unit (u.m.) |
|:--------|:----------------------:|
| **P1**  | 120                    |
| **P2**  | 150                    |

<br>
  
### 🧰 Resource Usage per Unit

| Product | R1/unit | R2/unit | R3/unit |
|:--------|:-------:|:-------:|:-------:|
| **P1**  |   2     |   3     |   5     |
| **P2**  |   4     |   0     |   3     |

<br>

### 📦 Monthly Resource Availability

| Resource | Available Units |
|:---------|:----------------:|
| **R1**   |      100         |
| **R2**   |       90         |
| **R3**   |      120         |


<br>

### 🧠 [Notes]():

• This LP model can be solved using methods such as the Simplex Algorithm.
 
• Can also be implemented in software such as Python (PuLP), MATLAB, or Excel Solver.


<br><br>

## 2- 📈 [Graphical Solution to the Linear Programming (LP) Problem]():

<br>

### ➢ [**Objective:**]():

$
Z = 4x_1 + 3x_2
$


```latex
Z = 4x_1 + 3x_2
```

<br>

### ➢ [**Subject to:**]():

$$
\begin{cases}
x_1 + 3x_2 \leq 7 \\
2x_1 + 2x_2 \leq 8 \\
x_1 + x_2 \leq 3 \\
x_2 \leq 2 \\
x_1 \geq 0, \quad x_2 \geq 0
\end{cases}
$$

```latex
\begin{cases}
x_1 + 3x_2 \leq 7 \\
2x_1 + 2x_2 \leq 8 \\
x_1 + x_2 \leq 3 \\
x_2 \leq 2 \\
x_1 \geq 0, \quad x_2 \geq 0
\end{cases}
```

<br>

###  [Step 1]() ➢ Plot the Constraints:

Convert inequalities into equalities to draw the lines:

<br>

### [1](). $x_1 + 3x_2 = 7$
   - If $x_1 = 0 \Rightarrow x_2 = \frac{7}{3} \approx 2.33$
   - If $x_2 = 0 \Rightarrow x_1 = 7$
  
<br>

```latex
x_1 + 3x_2 = 7$
   - If x_1 = 0 \Rightarrow x_2 = \frac{7}{3} \approx 2.33
   - If x_2 = 0 \Rightarrow x_1 = 7
```
  
<br>

### [2](). $2x_1 + 2x_2 = 8$
   - If $x_1 = 0 \Rightarrow x_2 = 4$
   - If $x_2 = 0 \Rightarrow x_1 = 4$

<br>

```latex
x_1 + 2x_2 = 8
   - If x_1 = 0 \Rightarrow x_2 = 4
   - If x_2 = 0 \Rightarrow x_1 = 4
```

<br>

### [3](). $x_1 + x_2 = 3$
   - If $x_1 = 0 \Rightarrow x_2 = 3$
   - If $x_2 = 0 \Rightarrow x_1 = 3$

<br>

```latex
x_1 + x_2 = 3
   - If x_1 = 0 \Rightarrow x_2 = 3
   - If x_2 = 0 \Rightarrow x_1 = 3
```

<br>

### [4](). $x_2 = 2$ → horizontal line

<br>

```latex
x_2 = 2 → horizontal line
```

<br>

### [Step 2]()  ➢ Identify the Feasible Region:

- The feasible region is the intersection of all shaded regions that satisfy the constraints.
- Must include $x_1 \geq 0$ and $x_2 \geq 0$.

 <br> 

```latex
x_1 \geq 0$ and $x_2 \geq 0
```

<br><br>

###  [Step 3]() ➢ Find Intersection Points (Vertices):

 <br> 

### [1](). Intersection of $x_1 + 3x_2 = 7$ and $2x_1 + 2x_2 = 8$:
   - Multiply first by 2: $2x_1 + 6x_2 = 14$
   - Subtract: $4x_2 = 6 \Rightarrow x_2 = 1.5$, $x_1 = 2.5$
   - Point: **(2.5, 1.5)**

 <br> 

```latex
Intersection of x_1 + 3x_2 = 7 and 2x_1 + 2x_2 = 8:
   - Multiply first by 2: 2x_1 + 6x_2 = 14
   - Subtract: 4x_2 = 6 \Rightarrow x_2 = 1.5$, $x_1 = 2.5
   - Point: **(2.5, 1.5)**
```

<br>

### [2](). Intersection of $x_1 + 3x_2 = 7$ and $x_1 + x_2 = 3$:
   - Subtract: $2x_2 = 4 \Rightarrow x_2 = 2$, $x_1 = 1$
   - Point: **(1, 2)**

 <br> 

```latex
 Intersection of x_1 + 3x_2 = 7 and x_1 + x_2 = 3:
   - Subtract: 2x_2 = 4 \Rightarrow x_2 = 2$, x_1 = 1
   - Point: **(1, 2)**
```

<br>

### [3](). Intersection of $x_1 + x_2 = 3$ and $x_2 = 2$:
   - $x_1 = 1$
   - Point: **(1, 2)**

<br>

### [4](). Intersection of $2x_1 + 2x_2 = 8$ and $x_2 = 2$:
   - $x_1 = 2$
   - Point: **(2, 2)**

<br>

### [5](). $x_1 + x_2 = 3$ and $x_1 = 0 \Rightarrow x_2 = 3$ ❌ (Invalid since $x_2 \leq 2$)

<br>

### [6](). $x_1 + 3x_2 = 7$ and $x_1 = 0 \Rightarrow x_2 = 7/3 \approx 2.33$ ❌ (Invalid since $x_2 \leq 2$)


<br><br>

### [Step 4]() ➢ Evaluate Objective Function at Each Vertex:

## Feasible Vertices:

- A: (0, 0)
- B: (0, 2)
- C: (1, 2)
- D: (2, 2)
- E: (2, 0)
- F: (3, 0)

<br>

| Point | $x_1$ | $x_2$ | $Z = 4x_1 + 3x_2$ |
|:-----:|:-----:|:-----:|:-----------------:|
| A     | 0     | 0     | 0                 |
| B     | 0     | 2     | 6                 |
| C     | 1     | 2     | 10                |
| D     | 2     | 2     | 14 ❌             |
| E     | 2     | 0     | 8                 |
| F     | 3     | 0     | 12                |


<br><br>

##  [Step 5]() ➢ Check Feasibility:

- **(2,2)** violates: $x_1 + 3x_2 = 2 + 6 = 8 > 7$ ❌
- All others: ✅

<br>

### ✅ Final Step: Choose the Best Feasible Point

| Point | $Z$ | Feasible |
|:-----:|:---:|:--------:|
| A     | 0   | Yes      |
| B     | 6   | Yes      |
| C     | 10  | Yes      |
| E     | 8   | Yes      |
| F     | 12  | ✅ Best   |
| D     | 14  | No       |


<br><br>

## 🏁 [Conclusion]():

- **Optimal solution:** $x_1 = 3$, $x_2 = 0$
- **Maximum value:** $Z = 12$

<br>

```latex
- **Optimal solution:** x_1 = 3$, $x_2 = 0
- **Maximum value:** Z = 12
```

<br><br>


# X - [Transportation Problem (Linear Programming)]()

#### ➣ [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-MathModeling-LinearProgramming/blob/3a8ebd38925f06e8a7152ffd0a94637aab8dc170/class__10-Northwest%20Corner%20Method/class_9%20-%20Transportation%20Problem%20(Linear%20Programming).pdf) to access Theoretical and Pratical Material. 


#### ➢ [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-MathModeling-LinearProgramming/tree/3a8ebd38925f06e8a7152ffd0a94637aab8dc170/class__10-Northwest%20Corner%20Method) and access Transportation Exercises


<br>

### [Definition]():

The transportation problem is a type of **linear programming** model where the objective is to determine the most **cost-efficient** way to transport goods from multiple sources (e.g., warehouses) to multiple 

<br>

### [Key Concepts]():

- **Origins (Sources)**: Where goods are located.
- **Destinations (Sinks)**: Where goods are needed.
- **Supply**: Available quantity at each origin.
- **Demand**: Required quantity at each destination.
- **Cost Matrix**: Unit cost of transporting goods from each origin to each destination.
- **Decision Variable**: Quantity to transport from each origin to each destination.

<br>

### [The Case of Unbalanced Systems]():

The standard transportation model assumes total supply equals total demand. However, in real-world scenarios, systems can be **unbalanced**.

- If total **supply ≠ demand**, the model can be adjusted by **adding a dummy origin or destination** to absorb the difference.
- The unit transportation **cost for dummy cells is zero**.
- Any quantity sent from or to dummy cells reflects **unfulfilled demand or leftover supply**, allowing simulation of **shortages or surpluses**.
constraints.

<br>

### [Example: Unbalanced Transportation Problem]():

### ➠ [Initial Unbalanced Model]():

<br>

|      | D1 | D2 | D3 | Supply |
|------|----|----|----|--------|
| O1   | 10 | 12 | 9  | 20     |
| O2   | 4  | 9  | 8  | 30     |
| O3   | 6  | 12 | 10 | 10     |
|      |    |    |    |        |
| **Demand** | 25 | 36 | 5  | **Total: 66** |

<br>

```latex
\[
\begin{array}{c|ccc|c}
 & D1 & D2 & D3 & \text{Supply} \\
\hline
O1 & 10 & 12 & 9 & 20 \\
O2 & 4  & 9  & 8 & 30 \\
O3 & 6  & 12 & 10 & 10 \\
\hline
\text{Demand} & 25 & 36 & 5 & \text{Total: } 66 \\
\end{array}
\]
```

<br>

### ➢ Total supply = [60]()  
### ➢ Total demand = [66]() → ⚠️ **Unbalanced** 

#

### ➠ [Adjusted Balanced Model (Dummy Origin A Added)]():

<br>

|      | D1 | D2 | D3 | Supply |
|------|----|----|----|--------|
| O1   | 10 | 12 | 9  | 20     |
| O2   | 4  | 9  | 8  | 30     |
| O3   | 6  | 12 | 10 | 10     |
| A    | 0  | 0  | 0  | 6      |
|      |    |    |    |        |
| **Demand** | 25 | 36 | 5  | **66** |


<br>

```latex
\[
\begin{array}{c|ccc|c}
 & D1 & D2 & D3 & \text{Supply} \\
\hline
O1 & 10 & 12 & 9 & 20 \\
O2 & 4  & 9  & 8 & 30 \\
O3 & 6  & 12 & 10 & 10 \\
A  & 0  & 0  & 0 & 6 \\
\hline
\text{Demand} & 25 & 36 & 5 & 66 \\
\end{array}
\]
```

### ➢ Now the model is **balanced**: [66 = 66]()

#

### ➠ [Feasible Solution Example]():

<br>

|      | D1 | D2 | D3 | Supply |
|------|----|----|----|--------|
| O1   | 0  | 20 | 0  | 20     |
| O2   | 5  | 25 | 0  | 30     |
| O3   | 0  | 10 | 0  | 10     |
| A    | 20 | 1  | 5  | 6      |
|      |    |    |    |        |
| **Demand** | 25 | 36 | 5  | **66** |

🟡 The values in the matrix represent the **quantities transported**.  
🟠 Quantities from the dummy origin A represent **unsatisfied demand**.

<br>

```latex
\[
\begin{array}{c|ccc|c}
 & D1 & D2 & D3 & \text{Supply} \\
\hline
O1 & 0 & 20 & 0 & 20 \\
O2 & 5 & 25 & 0 & 30 \\
O3 & 0 & 10 & 0 & 10 \\
A  & 20 & 1 & 5 & 6 \\
\hline
\text{Demand} & 25 & 36 & 5 & 66 \\
\end{array}
\]
```

🟡 The values in the matrix represent the **quantities transported**.  
🟠 $begin:math:text$ X_{A2} = 1 $end:math:text$, $begin:math:text$ X_{A3} = 5 $end:math:text$: These are **unsatisfied demands**.


## 🧠 [Relation to Algorithms]()

The transportation problem is a special type of **Linear Programming** that can be solved with:

- **Simplex Method**: General LP solver; can handle transportation problems but not optimized for them.
- **Specialized Algorithms**:
  - Northwest Corner Rule
  - Least Cost Method
  - Vogel’s Approximation Method (VAM)
  - MODI (Modified Distribution Method)

These specialized algorithms are **faster** and **simpler** due to the regular structure of the transportation tableau.

<br>


## 📈 [Transportation Algorithm & Simplex Connection]():

The transportation algorithm follows the **same logic as the Simplex method**, but with **simplifications** tailored to the structure of transportation problems:

###  [1st Phase](): Initial Basic Feasible Solution

We will use two methods to find a basic solution:

- **Northwest Corner Method**
- **Least Cost Method**

These provide starting points for optimization.


###  [2nd Phase](): Optimality Check:

After obtaining a feasible solution, we check for optimality using methods like:

- **MODI Method** (Modified Distribution)
- **Stepping Stone Method**

These determine whether cost can be further reduced by adjusting flows along loops in the matrix.

<br>

# XI- 🧭 [Northwest Corner Method (Transportation]()


#### ➢ [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-MathModeling-LinearProgramming/blob/3a8ebd38925f06e8a7152ffd0a94637aab8dc170/class__10-Northwest%20Corner%20Method/class_9%20-%20Transportation%20Problem%20(Linear%20Programming).pdf) to access Theoretical and Pratical Material. 


#### ➣ [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-MathModeling-LinearProgramming/tree/3a8ebd38925f06e8a7152ffd0a94637aab8dc170/class__10-Northwest%20Corner%20Method) and access Transportation Exercices


This is a method to generate an initial feasible solution without considering transportation costs.

<br>

### ➢ [Steps]():

1. **Start in the top-left (northwest) corner** of the transportation table.
   - This is always cell $begin:math:text$ x_{11} $end:math:text$.
2. **Allocate as much as possible** to the selected cell, respecting the available supply and demand.
3. **Block the row or column** where the supply or demand has been fully used (but only one if both are zero simultaneously).
   - Mark the blocked row/column with an 'x'.
   - This ensures that some basic variables have zero values (necessary for basic feasible solution).
4. **Repeat** the steps with the next unblocked cell in the top-left of the remaining matrix.

🔁 Continue until all cells are either allocated or blocked.

🟢 This method is **simple and quick**, but not necessarily optimal — further optimization is done in the next phase.

<br>

## 💸  [Least Cost Method (Método do Custo Mínimo]():

This method takes into account the transportation costs to guide the initial allocation.

<br>

### ➢ [Steps]():

1. **Identify the cell with the lowest unit cost** in the cost matrix among the remaining unallocated cells.
2. **Allocate as much as possible** to this cell, without exceeding supply or demand constraints.
3. **Adjust the supply and demand** for the row and column of the allocated cell.
4. **Remove** (cross out) the row or column where supply or demand becomes zero. If both are zero simultaneously, cross out only one to maintain feasibility.
5. **Repeat** the steps until all supplies and demands are met.

<br>
   
⚠️ Unlike the Northwest Corner, this method **considers the costs** and usually leads to a **better initial solution**, closer to the optimal.

<br>

### 🔍  [Link to Risk Analysis]():

- Unbalanced models simulate **shortage/surplus risks**.
- Dummy rows/columns help visualize **operational failures**.
- Solutions help identify:
  - Where **stockouts** will occur
  - How to **redistribute resources**
  - Costs of **unserved demands**
 
<br>

This makes the model highly applicable to **supply chain risk management, disaster response logistics, and critical infrastructure planning**.

<br>

### 📐 [Initial Basic Feasible Solution]():

A basic feasible solution must:
1. Satisfy **all row (supply)** and **column (demand)** constraints.
2. Include exactly **(m + n − 1)** basic variables (with m origins and n destinations).
3. Avoid **closed loops (cycles)** in the tableau — these are patterns where allocation forms a polygon that violates independence.

These principles ensure a **non-degenerate** starting point for iterative improvement algorithms like MODI.

<br>

### 🧩 [Summary]():

The transportation problem provides a clear, visual way to:
- Model **linear resource flows**,
- Simulate **imbalances and failure points**,
- Optimize with **tailored algorithms**, and
- Integrate with **Simplex** and **risk frameworks** for smarter planning.
  
<br>


It's a cornerstone of **Operational Research**, **Logistics**, and **Decision Science**.

<br>

# XII - [ Northwest Corner Method - Exercise - Optimal Solution]()


#### ➢ [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-MathModeling-LinearProgramming/blob/e6bee6582b53949aed266b384bb7ba6c15271480/class__10-Northwest%20Corner%20Method/class_9%20-%20Transportation%20Problem%20(Linear%20Programming).pdf) to access Theoretical and Pratical Material. 


#### ➣ [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-MathModeling-LinearProgramming/blob/e6bee6582b53949aed266b384bb7ba6c15271480/class__10-Northwest%20Corner%20Method/2-excel-Northwest%20Corner%20Method%20.md.md) and accessNorthwest Corner Method  Exercises

<br>


The initial solution obtained via the Northwest Corner Method has a total cost of 9690 but is not optimal. After one iteration of the transportation algorithm, the solution improves, but the process reveals complexities in achieving optimality. Here's the detailed analysis:

<br>

### [Step 1](): Optimality Check Using Multipliers

### - [**Multipliers calculation**]():
  
### - Set $u_1 = 0$, leading to $v_1 = 12$, $u_2 = 6$, $v_2 = 18$, $u_3 = -3$, and $v_3 = 37$.

```latex
u_1 = 0, leading to v_1 = 12, u_2 = 6, v_2 = 18, u_3 = -3, and v_3 = 37.
```
 
    
### - [**Reduced costs** for non-basic variables]():
    
### - $\bar{c}_{12} = -4$
### - $\bar{c}_{13} = 7$
### - $\bar{c}_{23} = 11$
### - $\bar{c}_{31} = -13$

```latex
\bar{c}_{12} = -4
\bar{c}_{13} = 7
\bar{c}_{23} = 11
\bar{c}_{31} = -13
```

#### - [**Negative reduced costs indicate non-optimality**]().

<br>

## [Step 2](): Improving the Solution:

### - **Entering variable**: $x_{31}$ (most negative reduced cost: $-13$).

### - **Loop construction**: Adjustments involve $x_{31}$, $x_{32}$, $x_{22}$, and $x_{21}$, with a minimum adjustment of 10 units.
 
### - **Updated solution**:
  
  - $x_{31} = 10$, $x_{21} = 10$, $x_{22} = 130$, $x_{32} = 0$.
    
  - Total cost increases to **9820** due to an incorrect loop adjustment in manual calculations.
 
<br>

### [Step 3](): Rechecking Optimality:

### - **Recalculated multipliers** (after correction)
  
  - $u =$, $v =$.
    
### - **New reduced costs**:
   
  - $\bar{c}_{12} = -4$, $\bar{c}_{13} = -6$, $\bar{c}_{23} = -2$, $\bar{c}_{31} = 0$.

  - $\bar{c}_{12} = -4$, $\bar{c}_{13} = -6$, $\bar{c}_{23} = -2$, $\bar{c}_{31} = 0$

  - ![equation](https://latex.codecogs.com/png.image?\bar{c}_{12}=-4,\ \bar{c}_{13}=-6,\ \bar{c}_{23}=-2,\ \bar{c}_{31}=0)

c̄₁₂ = -4, c̄₁₃ = -6, c̄₂₃ = -2, c̄₃₁ = 0

\bar{c}_{12} = -4,\quad \bar{c}_{13} = -6,\quad \bar{c}_{23} = -2,\quad \bar{c}_{31} = 0

$$\bar{c}_{12} = -4,\quad \bar{c}_{13} = -6,\quad \bar{c}_{23} = -2,\quad \bar{c}_{31} = 0$$

$\bar{c}_{12} = -4,\quad \bar{c}_{13} = -6,\quad \bar{c}_{23} = -2,\quad \bar{c}_{31} = 0$


      
### - Remaining negative reduced costs necessitate further iterations.
 

<br>

















### Under Construction 🚛

<br><br><br><br><br><br><br><br><br>

 
# XIII - [Designation]():


#### ➢ [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-MathModeling-LinearProgramming/blob/159b37b68be9228482c7959bd831b791f28bbdc4/class__11%20-Designation/Designation.pdf) to access Theoretical and Pratical Material. 

#### ➣ [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-MathModeling-LinearProgramming/tree/159b37b68be9228482c7959bd831b791f28bbdc4/class__11%20-Designation) and access Desgnation Exercises -Mathematical Modeling using the Hungarian Method , Excel Solver , and Python 🐍

<br>

### Task Designation - [Hungarian Method]()

### Theoretical Explanation

The **Assignment Problem** aims to allocate *n* tasks to *n* agents (machines, workers) at minimum cost, ensuring each task and agent is assigned exactly once.**

 
### [Problem Statement]():

**Three tasks must be assigned to three machines. Each task can be performed on any machine, but with different costs. Assign each task to one machine, and each machine to one task, minimizing the total cost.**

#### Cost Matrix

|         | Machine 1 | Machine 2 | Machine 3 |
|---------|-----------|-----------|-----------|
| Task 1  |     2     |     4     |     3     |
| Task 2  |     1     |     3     |     2     |
| Task 3  |     5     |     2     |     4     |


<br>


## 1. [Hungarian Method]() (Step by Step):

### [**Step 1](): Subtract Row Minimums**

#### Subtract the minimum value in each row from all elements in that row.

- Row 1 min: 2 → [0, 2, 1]
- Row 2 min: 1 → [0, 2, 1]
- Row 3 min: 2 → [3, 0, 2]

<br>

#### [**Matrix after row subtraction:**]()

|         | M1 | M2 | M3 |
|---------|----|----|----|
| Task 1  |  0 |  2 |  1 |
| Task 2  |  0 |  2 |  1 |
| Task 3  |  3 |  0 |  2 |


<br>

### [**Step 2](): Subtract Column Minimums**

### Problem Recap

- **3 tasks** must be assigned to **3 machines**.
- Each task can be done by any machine, but with different costs.
- Each task must be assigned to exactly one machine, and each machine to exactly one task.
- **Goal:** Minimize total assignment cost.

### Cost Table

|         | Machine 1 | Machine 2 | Machine 3 |
|---------|-----------|-----------|-----------|
| Task 1  |     2     |     4     |     3     |
| Task 2  |     1     |     3     |     2     |
| Task 3  |     5     |     2     |     4     |

---

## Step 1: Set Up the Excel Spreadsheet

### 1. Enter the Cost Matrix

|     | B    | C    | D    |
|-----|------|------|------|
|     | M1   | M2   | M3   |
| T1  |  2   |  4   |  3   |
| T2  |  1   |  3   |  2   |
| T3  |  5   |  2   |  4   |

- Place this table in cells **B2:D4**.

### 2. Create the Decision Variable Table

|     | G    | H    | I    |
|-----|------|------|------|
|     | M1   | M2   | M3   |
| T1  | x11  | x12  | x13  |
| T2  | x21  | x22  | x23  |
| T3  | x31  | x32  | x33  |

- Place this table in **G2:I4**.
- These cells will be filled with 0 or 1 by the Solver (1 = assigned, 0 = not assigned).

### 3. Calculate the Total Cost

In cell **K2**, enter:

```bash
=SUMPRODUCT(B2:D4, G2:I4)
```

This formula multiplies each assignment by its cost and sums the total.

### 4. Add Row and Column Sums for Constraints

#### Row Sums (Each Task Assigned Once)

- In **J2**: `=SUM(G2:I2)`
- In **J3**: `=SUM(G3:I3)`
- In **J4**: `=SUM(G4:I4)`

#### Column Sums (Each Machine Assigned Once)

- In **G5**: `=SUM(G2:G4)`
- In **H5**: `=SUM(H2:H4)`
- In **I5**: `=SUM(I2:I4)`

<br>

## Step 2: Configure Excel Solver

1. **Go to**: Data > Solver
2. **Set Objective**:  
   - Set **K2** (total cost) to **Minimize**.
3. **By Changing Variable Cells**:  
   - Select **G2:I4**.
4. **Add Constraints**:
   - **J2:J4 = 1** (each task assigned once)
   - **G5:I5 = 1** (each machine assigned once)
   - **G2:I4 = binary** (only 0 or 1 allowed)
5. **Choose Solving Method**:  
   - Use "Simplex LP" or "GRG Nonlinear" (either works for this size).
6. **Click Solve**.

<br>

## Step 3: Solution Example

After running Solver, you should get a solution like:

|     | M1 | M2 | M3 | Row Sum |
|-----|----|----|----|---------|
| T1  |  1 |  0 |  0 |   1     |
| T2  |  0 |  0 |  1 |   1     |
| T3  |  0 |  1 |  0 |   1     |
|Col Sum| 1|  1 |  1 |         |

- **Task 1 → Machine 1** (cost 2)
- **Task 2 → Machine 3** (cost 2)
- **Task 3 → Machine 2** (cost 2)

**Total minimum cost:** 6

<br>

## Excel Table and Formula Summary

|     | M1   | M2   | M3   | Row Sum |
|-----|------|------|------|---------|
| T1  | G2   | H2   | I2   | J2      |
| T2  | G3   | H3   | I3   | J3      |
| T3  | G4   | H4   | I4   | J4      |
|Col Sum|G5 | H5   | I5   |         |

- **Total Cost:** `=SUMPRODUCT(B2:D4, G2:I4)`
- **Row Sums:** `=SUM(G2:I2)`, etc.
- **Column Sums:** `=SUM(G2:G4)`, etc.

<br>

### [Result]():

**The optimal assignment is:**
- Task 1 to Machine 1 (cost 2)
- Task 2 to Machine 3 (cost 2)
- Task 3 to Machine 2 (cost 2)

### [**Total minimum cost:** 6]()


<br><br>

   


<!--
Let:
- **A** be the mix with half cherry and half mint chocolates, and let **x₁** be the number of kilograms prepared of this mix.
- **B** be the mix with one-third cherry and two-thirds mint chocolates, and let **x₂** be the number of kilograms prepared of this mix.

### Decision Variables:
- \( x_1 \) is the quantity (in kg) of mix A prepared.
- \( x_2 \) is the quantity (in kg) of mix B prepared.

### Objective Function:
Mix A is sold for R$ 20 per kg, and mix B is sold for R$ 12.50 per kg. Therefore, the objective function to be maximized is:

$Z = 20x_1 + 12.5x_2\$

### Constraints:
Each kilogram of mix A contains half a kilogram of cherry chocolates, and each kilogram of mix B contains one-third of a kilogram of cherry chocolates. Therefore, the total amount of cherry chocolates used is:

$\frac{x_1}{2} + \frac{x_2}{3} \leq 130\$

Each kilogram of mix A contains half a kilogram of mint chocolates, and each kilogram of mix B contains two-thirds of a kilogram of mint chocolates. Therefore, the total amount of mint chocolates used is:

$\frac{x_1}{2} + \frac{2x_2}{3} \leq 170\$

Additionally, we have the non-negativity constraints:

$x_1 \geq 0, \quad x_2 \geq 0\$

### Mathematically Modeled Problem:

$\text{Maximize } Z = 20x_1 + 12.5x_2\$

Subject to:

$\frac{x_1}{2} + \frac{x_2}{3} \leq 130\$

$\frac{x_1}{2} + \frac{2x_2}{3} \leq 170\$

$x_1 \geq 0, \quad x_2 \geq 0\$
-->




## [Contribute]()

Contributions are welcome! If you want to add more examples, correct errors, or improve the documentation, please submit a pull request. Let's learn and grow together on the journey of integral calculus.

<br>

## [How to Contribute]()

Any contributions are highly appreciated.  You can contribute in two ways:

   1. Create an issue and tell us your idea 💡. Make sure that you use the new idea label in this case;

   2. Fork the project and submit a full requesto with your new idea. Before doing that, please make sure that you read and follow the [Contributions Guide](https://github.com/Mindful-AI-Assistants/.github/blob/9e7e98f98af07a1d6c4bdeb349e1a9db04f8ed0e/CONTRIBUTIBNG.md). ⊹🔭๋

<br>

## Main Contributors

- [Fabiana 🚀 Campanari](https://github.com/FabianaCampanari) 

<br>

## Sources

➢ 1.  [Simulation-optimization: how to combine them in decision-making](https://logweb.com.br/simulacao-otimizacao-como-combina-las-na-tomada-de-decisoes-e-na-resolucao-de-problemas-na-logistica-e-supply-chain/)

➢ 2. [What is optimization? / VirtualCAE](https://virtualcae.com.br/2022/11/25/o-que-e-otimizacao/) 

➢ 3. [Optimization in simulation models: a study](http://www.din.uem.br/sbpo/sbpo2011/pdf/87592) 

➢ 4. [Simulation-Optimization: Why and How to Combine Them?](https://www.podesenvolvimento.org.br/podesenvolvimento/article/view/623) 

➢ 5. [Invited Tutorial: Simulation-Optimization](https://revistapodes.emnuvens.com.br/podesenvolvimento/article/download/623/412/4420) 

➢ 6. [Optimization and Simulation Models / DCA / Unicamp](https://www.dca.fee.unicamp.br/~gomide/courses/EA044/transp/EA_044_ModelosOtimizacaoSimulacao.pdf)

➢ 7. [Process Simulation and Optimization: Efficient Planning](https://paragon.com.br/simulacao-e-otimizacao-de-processos-planejamento-eficiente/)

➢ 8. [Simulation Modeling vs Optimization: How to Choose](https://www.linkedin.com/advice/0/how-do-you-choose-between-simulation-modeling?lang=pt)



#

###### <p align="center"> Copyright 2025 Quantum Software Development. Code released under the [MIT License license.](https://github.com/Quantum-Software-Development/Math/blob/3bf8270ca09d3848f2bf22f9ac89368e52a2fb66/LICENSE)
