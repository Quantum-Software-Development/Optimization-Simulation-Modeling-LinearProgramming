
<br>

#  <p align="center">  Integrated Mathematics Project 
####  <p align="center">  LOGISTICS, FINANCE, CREDIT, ENGINEERING, HEALTH AND OTHERS
#####  <p align="center">  [Optimization / Modeling and Simulation / Linear Programming / Graphic Method - Maximization and Minimization/ Simplex Algorithm / Matrix / Mathematical Modeling]()


<br><br>

### This Repo is focused on mathematical concepts, taught during the third semester of the Data Science and Artificial Intelligence bachelor's program at PUC-SP in 2025, under the instruction of [***Professor Doctor in Mathematics Daniel Rodrigues da Silva***](https://www.linkedin.com/in/daniel-rodrigues-048654a5/)


<br><br>


<!--### <p align="center">  <img src="https://github.githubassets.com/images/icons/emoji/octocat.png" width="46">  -->
### <p align="center"> [![Sponsor Quantum Software Development](https://img.shields.io/badge/Sponsor-Quantum%20Software%20Development-brightgreen?logo=GitHub)](https://github.com/sponsors/Quantum-Software-Development)


<br><br>


#### ➣ [Access Tutoril]() about solving LP problems using [Geogebra](https://youtu.be/nHYNeWIDd3g?si=n_UaKVjFmTM1Nhst)




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

## I- Example of a [Optimization Problem]()

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

## II- [Modeling - Writing Mathematical Models]()

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
   
## Solve the system using the **Simplex Method** or an optimization tool.

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


## Steps to Solve Graphically

<br>

1. **[Plot the Constraints]():** FFor each constraint, treat it as an equality and plot the corresponding straight line on the Cartesian plane ($x_1$ on the horizontal axis, $x_2$ on the vertical axis) [3].

 <br>

2. **[Identify the Feasible Region]():** For each inequality constraint, determine which side of the line satisfies the inequality. This can be done by testing a point (e.g., the origin $\(0,0)\)$; if it's not on the line) in the inequality. The feasible region is the area where all the shaded regions of the inequalities overlap. If there are non-negativity constraints $\(x_1 \geq 0\)$ and $\(x_2 \geq 0\)$, the feasible region will be in the **[first quadrant]()** [3].

 <br>

3.  **Identify the Vertices:** Determine the coordinates of all the vertices (corner points) of the feasible region [4, 6]. These are the points where the boundary lines intersect.

 <br>
 
4.  **Evaluate the Objective Function at Each Vertex:** Substitute the coordinates of each vertex into the objective function to find the value of the objective function at that point [6].


 <br>

5.  **Determine the Optimal Solution:**
    *   For a **maximization** problem, the vertex that yields the **largest** value of the objective function is the optimal solution [1, 6].
    *   For a **minimization** problem, the vertex that yields the **smallest** value of the objective function is the optimal solution [2, 7].


<br><br>

## Possible Scenarios

*   **Unique Optimal Solution:** The objective function achieves its maximum or minimum value at a single vertex of the feasible region [3, 5, 6].

*   **Multiple Optimal Solutions:** The objective function achieves its optimal value at more than one point, typically along an edge connecting two adjacent vertices. In this case, all points on that edge are optimal solutions [5].

*   **Unbounded Feasible Region:** If the feasible region extends infinitely in some direction, the objective function might also be unbounded (it can increase or decrease indefinitely without reaching a maximum or minimum value) [5]. However, if an optimal solution exists even with an unbounded region, it will still occur at a vertex [5].

*   **Empty Feasible Region:** If the constraints are inconsistent and there are no points that satisfy all of them simultaneously, the feasible region is empty, and the linear programming problem has no solution [4].

  <br>

## Theorem on Optimal Solutions

If the feasible region of a linear programming problem is **non-empty and bounded**, then the objective function attains both a **maximum and a minimum value**, and these occur at **extreme points (vertices)** of the feasible region [5].

If the feasible region is **unbounded**, and if the objective function attains a maximum or minimum value, it will also occur at an **extreme point (vertex)** [5].

  <br>

## Examples

The source provides several examples [6-8] that illustrate the graphical method for both maximization and minimization problems with different sets of constraints. These examples demonstrate how to plot the constraints, identify the feasible region, find the vertices, and evaluate the objective function to determine the optimal solution and its value. For instance, Example 1 [6] finds the maximum of $x_1 + 2x_2$ subject to several constraints.

  <br>

## Conclusion about the Graphical Method

The graphical method is a useful tool for solving linear programming problems with two decision variables, providing a clear visual representation of the solution process. It helps in understanding the concepts of feasible solutions, feasible regions, and the role of vertices in finding the optimal solution. However, this method is limited to problems with only two decision variables. For problems with more variables, more advanced techniques like the simplex algorithm are required.

<br><br>

# IV- The Simplex Method

#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/blob/5d0f89d3a4d9f67f900463505cb7d4b4e72d186a/class_4-Simplex%20Method/class_4-Simplex%20Method.pdf) to access Theoretical and Pratical Material. 


#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/tree/f9cef4452ad8486d03c8273aa83885de625c2da8/class_4-Simplex%20Method/SIMPLEX%20IMPLEMENT%20and%20CALCULUS%20EXERCISES) and access Simplex Implementation and Calculus Exercises Manually Solved

<br>

# V- Two-Stage Simplex

#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/blob/e09ce2c81b12f47975bdb0ed6b3acd77b2195532/class_6-Two-Stage%20Simplex./two-stage%20simplex..pdf) to access Theoretical and Pratical Material.

#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/tree/83b16e5330d7e467cb5df57827e7d02076ac0f84/class_6-Two-Stage%20Simplex/Exercise_1-Two-StageSimplex-Solved%20with%20Multiple%20Iteraties) and access Two-StageS Simplex with Multiple Iteraties - Implementation and Calculus Exercise Manually Solved

#### [Click here](https://github.com/Quantum-Software-Development/Optimization-Simulation-Modeling-LinearProgramming/tree/caf816701eac73bdf1289997519ea3560f72956e/class_6-Two-Stage%20Simplex/Exercise_2-Two-StageSimplex-Solved%20with%20Only%20%20One%20Iteration) and access Two-Stage Simplex with Only  One Iteration - Implementation and Calculus Exercise Manually Solved


<br>

# VI - Excel Solver for Linear Programming - Simplex


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


## Simplex Method using Excel Solver

This example shows how to solve a Linear Programming (LP) problem using the **Simplex Method** via **Excel Solver**.

---

### Problem

Maximize the objective function:

Z = 3x + 5y

Subject to the constraints:

x + 2y ≤ 100
2x + y ≤ 80
x, y ≥ 0

---

### Excel Spreadsheet Setup

Fill the spreadsheet with the following structure:

#### Variables and Objective

| Cell | Description            | Formula / Value      |
|------|------------------------|----------------------|
| B1   | x (Decision Variable)  | *(leave blank)*      |
| B2   | y (Decision Variable)  | *(leave blank)*      |
| B3   | Objective Function Z   | `=3*B1 + 5*B2`        |

#### Constraints Left-Hand Side (LHS)

| Cell | Description                | Formula             |
|------|----------------------------|---------------------|
| B5   | Constraint 1 LHS           | `=1*B1 + 2*B2`       |
| B6   | Constraint 2 LHS           | `=2*B1 + 1*B2`       |

#### Constraints Right-Hand Side (RHS)

| Cell | Description                | Value               |
|------|----------------------------|---------------------|
| C5   | Constraint 1 RHS           | `100`               |
| C6   | Constraint 2 RHS           | `80`                |

---

### Solver Configuration (Simplex LP)

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

---

### Solution

After running Solver

x = 20
y = 40
Z = 320 + 540 = 260


Z = 260


——


## Excel Solver Example – Linear Programming with Simplex

This example demonstrates how to use Excel Solver to solve a Linear Programming problem using the **Simplex Method**.

### Problem Statement

Maximize:

Z = 40x + 30y

Subject to:

2x + y ≤ 40
x + 2y ≤ 50
x, y ≥ 0


### Excel Setup

| Cell | Description              | Formula / Value     |
|------|--------------------------|---------------------|
| B1   | x (Decision Variable)    | (leave blank)       |
| B2   | y (Decision Variable)    | (leave blank)       |
| B3   | Objective Function (Z)   | `=40*B1 + 30*B2`     |
| B5   | Constraint 1 (LHS)       | `=2*B1 + 1*B2`       |
| B6   | Constraint 2 (LHS)       | `=1*B1 + 2*B2`       |

| Cell | Constraint RHS           | Value               |
|------|--------------------------|---------------------|
| C5   | Constraint 1 (RHS)       | 40                  |
| C6   | Constraint 2 (RHS)       | 50                  |

### Solver Configuration

1. Set Objective: **B3**  
2. To: **Maximize**  
3. By Changing Variable Cells: **B1:B2**  
4. Subject to the Constraints:
   - **B5 <= C5**
   - **B6 <= C6**
   - **B1 >= 0**
   - **B2 >= 0**
5. Choose **Simplex LP** as the solving method.

Click **Solve** to find the optimal solution.

### Solution Output

After running Solver:

- **x = 10**
- **y = 20**
- **Z = 40×10 + 30×20 = 1000**

<br>

## Extras Excercise:

<br>

### 1. [Develop a Mathematical Model – Linear Programming (LP)]():

📘 Problem Statement in English

A company, after a production rationalization process, has 3 available productive resources: R1, R2, and R3. A study indicated the feasibility of manufacturing two products: P1 and P2. After analyzing costs and consulting the sales department, it was found that P1 yields a profit of 120 u.m. per unit and P2 yields 150 u.m. per unit. The production department provided the following resource usage table:

| Product | R1/unit | R2/unit | R3/unit |
|---------|---------|---------|---------|
| P1      |   2     |   3     |   5     |
| P2      |   4     |   0     |   3     |

| Resource Availability per month | R1 = 100 | R2 = 90 | R3 = 120 |







<br><br>


### **2.** [Solve graphically the LP presented below]():

<br>

$$
\
\begin{aligned}
\textbf{Max.} \quad & Z = 4x_1 + 3x_2 \\
\textbf{S.a.} \quad &
\begin{cases}
x_1 + 3x_2 \leq 7 \\
2x_1 + 2x_2 \leq 8 \\
x_1 + x_2 \leq 3 \\
x_2 \leq 2 \\
x_1 \geq 0 \text{ e } x_2 \geq 0
\end{cases}
\end{aligned}
\
$$




<br><br>


### **3.** [Solve the following linear programming problem using the Simplex method]():

<br>

$$
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
$$






   










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


<br>













<br><br><br><br><br><br>

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
