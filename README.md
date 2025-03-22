
<br>

#  <p align="center">  Integrated Mathematics Project
###  <p align="center">  [Optimization / Modeling and Simulation / Linear Programming / Graphic Method - Maximization and Minimization/ Simplex Algorithm / Matrix / Mathematical Modeling]()


<br>

<!--### <p align="center">  <img src="https://github.githubassets.com/images/icons/emoji/octocat.png" width="46">  -->
### <p align="center"> [![Sponsor Quantum Software Development](https://img.shields.io/badge/Sponsor-Quantum%20Software%20Development-brightgreen?logo=GitHub)](https://github.com/sponsors/Quantum-Software-Development)

<br>


### This Repo is focused on mathematical concepts, taught during the third semester of the Data Science and Artificial Intelligence bachelor's program at PUC-SP in 2025, under the instruction of Professor [Daniel Rodrigues da Silva](https://www.linkedin.com/in/daniel-rodrigues-048654a5/)


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

### [Matrix]()

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

### [Simulation]()

Simulation generally involves complex mathematical models that can be described using differential or integral equations.

$$
y(t) = A e^{kt}
$$

```latex
y(t) = A e^{kt}
```
<br>

#### This equation represents a simple solution to an ordinary differential equation.

<br><br>

## II- [Modeling - Writing Mathematical Models]()


### Example 1: [Maximizing Profit for a Chocolate Manufacturer]()

A chocolate manufacturer has a stock of chocolates, consisting of 130 kg with cherry filling and 170 kg with mint filling. He decides to sell the stock in the form of two different assorted packages. One package contains a mix with half the weight in cherry chocolates and half in mint chocolates and sells for R$ 20.00 per kg. The other package contains a mix of one-third cherry chocolates and two-thirds mint chocolates and sells for R$ 12.50 per kg. How many kilograms of each mix should the seller prepare to maximize his sales profit?

### [Solution]():

###  Objective Function

#### [Maximize]():

$$
Z = 20x_1 + 12.5x_2
$$


#### [Subject to Constraints]():

$$
\begin{cases}
    \frac{x_1}{2} + \frac{x_2}{3} \leq 130 \\
    \frac{x_1}{2} + \frac{2x_2}{3} \leq 170 \\
    x_1 \geq 0, \quad x_2 \geq 0
\end{cases}
$$


### Solution Steps

1. Express the cherry chocolate constraint:
   
   $$\frac{x_1}{2} + \frac{x_2}{3} \leq 130$$
   
2. Express the mint chocolate constraint:
   
   $$\frac{x_1}{2} + \frac{2x_2}{3} \leq 170$$
   
 Solve the system using the **Simplex Method** or an optimization tool.

<br>

### Optimal Solution:

#### [Solving the system yields]():

$$
(x_1, x_2) = (180, 120)
$$

#### [Maximum Profit Calculation]()

$$
Z = 20(180) + 12.5(120)
$$

$$
Z = 3600 + 1500 = 5100
$$

<br>

Thus, the maximum profit achievable is [**R$ 5,100**]().


<br><br>


## III- [Graphical Method for Linear Programming]() (LP)

<br>

The **graphical method** for solving simple linear programming (LP) problems involving **two decision variables**. The graphical method provides a visual way to understand the constraints, the feasible region, and how to find the optimal solution that either maximizes or minimizes the objective function.

#

### [Key]() Concepts:

- **[Decision Variables]():** These are the variables that we want to determine the values of to optimize the ***[OBJECTIVE FUNCTION]()*** (e.g.):

   #### $$\(x_1\)$$ and $$\(x_2\)$$

<br>
 
- **[Objective Function]():** This is the linear function that we aim to maximize or minimize. For example:

  $$\max/\min \quad Z$$ = $$c_1x_1 + c_2x_2$$

  
<br>

- **[Constraints]():** These are linear inequalities or equalities that restrict the values the decision variables can take.
  - Equality constraint:


     #### $$a_{i1}x_1 + a_{i2}x_2$$ = $$b_i$$


  <br>


  - Less than or equal to constraint:

     #### $$a_{i1}x_1$$ + $$a_{i2}x_2 \leq b_i$$

    <br>

  - Greater than or equal to constraint:

     #### $$a_{i1}x_1$$ + $$a_{i2}x_2 \geq b_i$$

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

1. **[Plot the Constraints]():** For each constraint, treat it as an equality and plot the corresponding straight line on the Cartesian plane $\(x_1\)$ on the horizontal axis, $\(x_2\)$ on the vertical axis.

 <br>

3. **[Identify the Feasible Region]():** For each inequality constraint, determine which side of the line satisfies the inequality. This can be done by testing a point (e.g., the origin $\(0,0)\)$; if it's not on the line) in the inequality. The feasible region is the area where all the shaded regions of the inequalities overlap. If there are non-negativity constraints $\(x_1 \geq 0\)$ and $\(x_2 \geq 0\)$, the feasible region will be in the **[first quadrant]()**.

 <br>
 
 4. **Evaluate the Objective Function at Each Vertex:** Substitute the coordinates of each vertex into the objective function to find the value of the objective function at that point.

 <br>

5. **Determine the Optimal Solution:**
   - For a **maximization** problem, the vertex that yields the **largest** value of the objective function is the optimal solution.














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

### [How to Contribute]()

Any contributions are highly appreciated.  You can contribute in two ways:

   1. Create an issue and tell us your idea 💡. Make sure that you use the new idea label in this case;

   2. Fork the project and submit a full requesto with your new idea. Before doing that, please make sure that you read and follow the [Contributions Guide](https://github.com/Mindful-AI-Assistants/.github/blob/9e7e98f98af07a1d6c4bdeb349e1a9db04f8ed0e/CONTRIBUTIBNG.md). ⊹🔭๋


### [Main Contributors]() 

- [Fabiana 🚀 Campanari](https://github.com/FabianaCampanari) 

<br>

## [Sources]()

- [1]() Simulation-optimization: how to combine them in decision-making and ... - https://logweb.com.br/simulacao-otimizacao-como-combina-las-na-tomada-de-decisoes-e-na-resolucao-de-problemas-na-logistica-e-supply-chain/

- [2]() What is optimization? / VirtualCAE -  https://virtualcae.com.br/2022/11/25/o-que-e-otimizacao/

- [3]() Optimization in simulation models: a study - http://www.din.uem.br/sbpo/sbpo2011/pdf/87592.

- [4]() Simulation-Optimization: Why and How to Combine Them? -  https://www.podesenvolvimento.org.br/podesenvolvimento/article/view/623

- [5]() Invited Tutorial: Simulation-Optimization – Why and... -  https://revistapodes.emnuvens.com.br/podesenvolvimento/article/download/623/412/4420

- [6]() Optimization and Simulation Models / DCA / Unicamp - https://www.dca.fee.unicamp.br/~gomide/courses/EA044/transp/EA_044_ModelosOtimizacaoSimulacao.pdf

- [7]() Process Simulation and Optimization: Efficient Planning -  https://paragon.com.br/simulacao-e-otimizacao-de-processos-planejamento-eficiente/

- [8]() Simulation Modeling vs Optimization: How to Choose - LinkedIn - https://www.linkedin.com/advice/0/how-do-you-choose-between-simulation-modeling?lang=pt



#

###### <p align="center"> Copyright 2025 Quantum Software Development. Code released under the [MIT License license.](https://github.com/Quantum-Software-Development/Math/blob/3bf8270ca09d3848f2bf22f9ac89368e52a2fb66/LICENSE)
