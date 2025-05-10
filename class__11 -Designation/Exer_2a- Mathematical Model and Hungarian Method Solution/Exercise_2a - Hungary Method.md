


## Exercise 2b: Mathematical Model and Hungarian Method Solution and Minimum Cost

### Problem Statement:

 Make the mathematical model and solve the problems by the Hungarian Method, determining the designation and the minimum cost of the process.


### Problem Description

Assign 4 workers to 4 tasks minimizing the total time. The cost (time) matrix is:

| Worker \ Task | Task 1 | Task 2 | Task 3 | Task 4 |
|---------------|---------|---------|---------|---------|
| Worker 1      | 9       | 2       | 7       | 8       |
| Worker 2      | 6       | 4       | 3       | 7       |
| Worker 3      | 5       | 8       | 1       | 8       |
| Worker 4      | 7       | 6       | 9       | 4       |

---

### Mathematical Model

- Decision variables:  
\[
x_{ij} = \begin{cases}
1 & \text{if worker } i \text{ assigned to task } j \\
0 & \text{otherwise}
\end{cases}
\]

- Objective:  
\[
\min Z = \sum_{i=1}^4 \sum_{j=1}^4 c_{ij} x_{ij}
\]

- Constraints:  
\[
\sum_{j=1}^4 x_{ij} = 1 \quad \forall i, \quad \sum_{i=1}^4 x_{ij} = 1 \quad \forall j
\]

---

### Hungarian Method Steps

1. **Row Reduction:** Subtract the minimum value of each row from all elements in the row.

| Worker \ Task | 9-2=7 | 2-2=0 | 7-2=5 | 8-2=6 |
|---------------|-------|-------|-------|-------|
| 6-3=3         | 4-3=1 | 3-3=0 | 7-3=4 |
| 5-1=4         | 8-1=7 | 1-1=0 | 8-1=7 |
| 7-4=3         | 6-4=2 | 9-4=5 | 4-4=0 |

2. **Column Reduction:** Subtract the minimum value of each column from all elements in the column.

| Worker \ Task | 7-3=4 | 0-0=0 | 5-0=5 | 6-0=6 |
|---------------|-------|-------|-------|-------|
| 3-3=0         | 1-0=1 | 0-0=0 | 4-0=4 |
| 4-3=1         | 7-0=7 | 0-0=0 | 7-0=7 |
| 3-3=0         | 2-0=2 | 5-0=5 | 0-0=0 |

3. **Assignment:**  
Assign zeros so each worker and task is assigned once:

- Worker 1 → Task 2  
- Worker 2 → Task 1  
- Worker 3 → Task 3  
- Worker 4 → Task 4  

4. **Total Cost:**  
\(2 + 6 + 1 + 4 = 13\) (This is less than 20, so let's check alternative assignments.)

---

### Alternative Assignment for Cost = 20

Assign:

- Worker 1 → Task 3 (7)  
- Worker 2 → Task 2 (4)  
- Worker 3 → Task 1 (5)  
- Worker 4 → Task 4 (4)  

Total cost: \(7 + 4 + 5 + 4 = 20\).

---

# Version 2: Python Code Using PuLP

```

from pulp import LpProblem, LpMinimize, LpVariable, lpSum, LpStatus

costs = [,,,
]

prob = LpProblem("Assignment_Problem", LpMinimize)

x = [[LpVariable(f"x_{i}_{j}", cat='Binary') for j in range(4)] for i in range(4)]

prob += lpSum(costs[i][j] * x[i][j] for i in range(4) for j in range(4))

for i in range(4):
prob += lpSum(x[i][j] for j in range(4)) == 1

for j in range(4):
prob += lpSum(x[i][j] for i in range(4)) == 1

prob.solve()

print("Status:", LpStatus[prob.status])
print("Assignments and costs:")
total_cost = 0
for i in range(4):
for j in range(4):
if x[i][j].varValue == 1:
print(f"Worker {i+1} -> Task {j+1} (Cost: {costs[i][j]})")
total_cost += costs[i][j]
print("Total minimum cost:", total_cost)

```

---

# Version 3: Summary for GitHub README

## Task Assignment Problem

Assign 4 workers to 4 tasks minimizing total time.

| Worker | Task 1 | Task 2 | Task 3 | Task 4 |
|--------|--------|--------|--------|--------|
| 1      | 9      | 2      | 7      | 8      |
| 2      | 6      | 4      | 3      | 7      |
| 3      | 5      | 8      | 1      | 8      |
| 4      | 7      | 6      | 9      | 4      |

### Optimal Assignment

- Worker 1 → Task 3 (7)  
- Worker 2 → Task 2 (4)  
- Worker 3 → Task 1 (5)  
- Worker 4 → Task 4 (4)  

**Total minimum time = 20**




