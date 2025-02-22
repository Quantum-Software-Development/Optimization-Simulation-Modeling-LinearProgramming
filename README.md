
<br>

#  <p align="center">  Integrated Mathematics Project
###  <p align="center">  [Optimization / Simulation / Modelin / Linear Programming / Simplex Algorithm / Matrix / Mathematics]()


<br>

<!--### <p align="center">  <img src="https://github.githubassets.com/images/icons/emoji/octocat.png" width="46">  -->
### <p align="center"> [![Sponsor Quantum Software Development](https://img.shields.io/badge/Sponsor-Quantum%20Software%20Development-brightgreen?logo=GitHub)](https://github.com/sponsors/Quantum-Software-Development)

<br>


### This Repo is focused on mathematical concepts, taught during the third semester of the Data Science and Artificial Intelligence bachelor's program at PUC-SP in 2022, under the instruction of Professor [Daniel Rodrigues da Silva]()


<br><br>

## [Introduction to optimization problems and their basic properties]():

Constrained and unconstrained optimization. Linear Programming: formulation, geometric solution, simplex method, and duality. Network flow models: Transportation, Assignment, Shortest Path, and Maximum Flow problems. Integer programming. Multiobjective programming. Monte Carlo and discrete event simulation.


Optimization and simulation are two key areas in Operations Research, used for problem-solving and decision-making, but they approach these tasks differently[4][5]. Simulation creates a virtual model to analyze a system's behavior under various conditions, allowing for experimentation by varying parameters[1]. Optimization, on the other hand, employs mathematical algorithms to identify the best configuration of these parameters, aiming to maximize or minimize a specific objective, such as reducing costs or increasing efficiency[1][2].

**Sim-Opt (Simulation-Optimization)**
Sim-opt combines simulation and optimization techniques to provide a comprehensive and dynamic understanding of a system[1]. This approach integrates real-world uncertainties with the search for ideal solutions[1]. By simulating the impact of each parameter and comparing it to an ideal scenario, sim-opt helps identify the factors that most influence a system's performance, leading to more strategic decisions[1].

[**Benefits of Sim-Opt**]()
*   **Analyzing uncertain scenarios:** Sim-opt evaluates the impact of unpredictable events and helps plan strategies to manage risks[1].
*   **Optimizing processes:** It identifies bottlenecks and opportunities for improvement and defines the best practices for various situations[1].
*   **Making informed decisions:** Sim-opt bases decisions on data and simulations, reducing uncertainty and the risk of errors[1].

[**How to Implement Optimization in Simulation Models**]()

1.  **Define decision variables:** Identify the variables that affect the simulation model's outputs and will be tested by the optimization algorithm[3].
2.  **Define variable types and limits:** Determine whether each decision variable is real or integer and set lower and upper limits. The optimization algorithm will search for solutions within these limits[3].
3.  **Define the objective function:** Establish a function to evaluate the solutions tested by the algorithm. This function can be designed to minimize, maximize, or use both types of variables, depending on the study's objectives[3].
4.  **Select population size:** Choose the number of solutions for the evolutionary algorithm. The population size affects the reliability and time required for the search. Also, define other parameters such as the required precision, significance level, and number of replications[3].
5.  **Analyze solutions:** After the search, analyze the solutions found. Compare all solutions based on the objective function to identify the best and other competitive solutions[3].

The key difference between sim-opt and other analytical tools is its ability to model the complexity and dynamics of real-world systems, including data uncertainty and variability[1]. This allows for the creation of more robust and adaptable plans[1].

<br>

## Optimization Problem

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


## Simplex Algorithm

The simplex algorithm is used to solve linear problems. Although there isn't a specific command for it, we can describe it in text or use tables to show the steps of the algorithm.

### Matrix

A matrix can be created using the `amsmath` package:

$$
A =
\begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{bmatrix}
$$






<br>

## [Contribute]()

Contributions are welcome! If you want to add more examples, correct errors, or improve the documentation, please submit a pull request. Let's learn and grow together on the journey of integral calculus.

### [How to Contribute]()

Any contributions are highly appreciated.  You can contribute in two ways:

   1. Create an issue and tell us your idea 💡. Make sure that you use the new idea label in this case;

   2. Fork the project and submit a full requesto with your new idea. Before doing that, please make sure that you read and follow the [Contributions Guide](https://github.com/Mindful-AI-Assistants/.github/blob/9e7e98f98af07a1d6c4bdeb349e1a9db04f8ed0e/CONTRIBUTIBNG.md). ⊹★🔭๋࣭


### [Main Contributors]() 

- [Fabiana 🚀 Campanari](https://github.com/FabianaCampanari) 

<br>

## [Sources]()

[1] Simulação-otimização: como combiná-las na tomada de decisões e ... https://logweb.com.br/simulacao-otimizacao-como-combina-las-na-tomada-de-decisoes-e-na-resolucao-de-problemas-na-logistica-e-supply-chain/

[2] O que é otimização? - VirtualCAE https://virtualcae.com.br/2022/11/25/o-que-e-otimizacao/

[3] [PDF] otimização em modelos de simulação: um estudo http://www.din.uem.br/sbpo/sbpo2011/pdf/87592.

[4] SIMULAÇÃO-OTIMIZAÇÃO: PORQUE E COMO COMBINÁ-LAS? https://www.podesenvolvimento.org.br/podesenvolvimento/article/view/623

[5] [PDF] TUTORIAL CONVIDADO SIMULAÇÃO-OTIMIZAÇÃO: PORQUE E ... https://revistapodes.emnuvens.com.br/podesenvolvimento/article/download/623/412/4420

[6] [PDF] Modelos de Otimização e Simulação - DCA https://www.dca.fee.unicamp.br/~gomide/courses/EA044/transp/EA_044_ModelosOtimizacaoSimulacao.pdf

[7] Simulação e Otimização de processos: planejamento eficiente https://paragon.com.br/simulacao-e-otimizacao-de-processos-planejamento-eficiente/

[8] Modelagem de Simulação vs Otimização: Como Escolher - LinkedIn https://www.linkedin.com/advice/0/how-do-you-choose-between-simulation-modeling?lang=pt



#

###### <p align="center"> Copyright 2025 Quantum Software Development. Code released under the [MIT License license.](https://github.com/Quantum-Software-Development/Math/blob/3bf8270ca09d3848f2bf22f9ac89368e52a2fb66/LICENSE)
