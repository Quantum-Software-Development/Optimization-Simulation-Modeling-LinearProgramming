
# Exercise 1: Dijkstra's Algorithm – Step-by-Step Solution

## Problem Statement

A US transportation company delivers packages daily in New York City from origin node 1 (Queens) to destination node 6 (Manhattan), using different possible routes as shown in the graph below. The flow on the arcs represents the cost to transport the required demand between neighborhoods.  
**Task:** Determine the best route using Dijkstra's algorithm.

![Graph and Tableaus](https://pplx-res.cloudinary.com/image/private/user_uploads/27709701/a31aabec-aeef-42c0-b4cd-9024927871af/Screenshot-2025-05-14-at-13.24.26.jpg)

<br>

## Step-by-Step Solution with Tableaus

### Initialization

Assign value 0 to the source node (1) and ∞ (infinity) to all other nodes.

| 1* | 2* | 3* | 4* | 5* | 6* |
|----|----|----|----|----|----|
| 0  | ∞  | ∞  | ∞  | ∞  | ∞  |

---

### Iteration 1: Visit Node 1 (current minimum: 0)

- Update 2: 0 + 6 = 6, predecessor 1
- Update 3: 0 + 9 = 9, predecessor 1

| 1* | 2*    | 3*    | 4* | 5* | 6* |
|----|-------|-------|----|----|----|
| 0  | (1,6) | (1,9) | ∞  | ∞  | ∞  |

---

### Iteration 2: Visit Node 2 (current minimum: 6)

- Update 4: 6 + 4 = 10, predecessor 2
- Update 5: 6 + 7 = 13, predecessor 2

| 1* | 2*    | 3*    | 4*     | 5*     | 6* |
|----|-------|-------|--------|--------|----|
| 0  | 6     | (1,9) | (2,10) | (2,13) | ∞  |

---

### Iteration 3: Visit Node 3 (current minimum: 9)

(No better paths found from 3.)

| 1* | 2*    | 3*    | 4*     | 5*     | 6* |
|----|-------|-------|--------|--------|----|
| 0  | 6     | 9     | (2,10) | (2,13) | ∞  |

---

### Iteration 4: Visit Node 4 (current minimum: 10)

- Update 5: 10 + 2 = 12, predecessor 4 (improves from 13 to 12)
- Update 6: 10 + 7 = 17, predecessor 4

| 1* | 2*    | 3*    | 4* | 5*     | 6*     |
|----|-------|-------|----|--------|--------|
| 0  | 6     | 9     | 10 | (4,12) | (4,17) |

---

### Iteration 5: Visit Node 5 (current minimum: 12)

- Update 6: 12 + 3 = 15, predecessor 5 (improves from 17 to 15)

| 1* | 2*    | 3*    | 4* | 5* | 6*     |
|----|-------|-------|----|----|--------|
| 0  | 6     | 9     | 10 | 12 | (5,15) |

---

### Iteration 6: Visit Node 6 (current minimum: 15)

| 1* | 2*    | 3*    | 4* | 5* | 6* |
|----|-------|-------|----|----|----|
| 0  | 6     | 9     | 10 | 12 | 15 |

---

## Minimum Path and Cost

- **Path:** 1 → 2 → 4 → 5 → 6
- **Total Cost:** 15

---

## Explanation of Tableaus

- Each cell (X, Y) indicates the predecessor node (X) and the cumulative cost to reach the node (Y).
- At each step, only the best (lowest cost) paths are kept and updated.
- The algorithm stops when the destination node (6) receives a permanent label.

---

## Python Implementation

```

import heapq

def dijkstra(graph, start, end):
distances = {node: float('inf') for node in graph}
predecessors = {node: None for node in graph}
distances[start] = 0
queue = [(0, start)]
while queue:
curr_dist, curr_node = heapq.heappop(queue)
if curr_node == end:
break
for neighbor, weight in graph[curr_node].items():
distance = curr_dist + weight
if distance < distances[neighbor]:
distances[neighbor] = distance
predecessors[neighbor] = curr_node
heapq.heappush(queue, (distance, neighbor))
\# Reconstruct path
path = []
node = end
while node is not None:
path.append(node)
node = predecessors[node]
path.reverse()
return distances[end], path

# Graph from the example

graph = {
1: {2: 6, 3: 9},
2: {4: 4, 5: 7},
3: {},
4: {5: 2, 6: 7},
5: {6: 3},
6: {}
}

cost, path = dijkstra(graph, 1, 6)
print(f"Minimum cost: {cost}, Path: {path}")

```

---

## Excel Solver Step-by-Step

1. **Model the Network:**
    - Create a table with nodes as rows and columns, filling in arc costs (use a large number or blank for non-existent arcs).

2. **Define Decision Variables:**
    - For each arc (i, j), create a binary variable \( x_{ij} \) (1 if the arc is used, 0 otherwise).

3. **Objective Function:**
    - Minimize the total cost:  
      \[
      \text{Minimize} \quad Z = \sum_{(i,j)} c_{ij} x_{ij}
      \]

4. **Constraints:**
    - **Flow conservation:**  
      - For the source node: Outflow - Inflow = 1  
      - For the destination node: Inflow - Outflow = 1  
      - For all other nodes: Inflow - Outflow = 0

5. **Set Up Solver:**
    - Set the objective cell to the sum of selected arc costs.
    - Add constraints for flow conservation and binary variables.
    - Run Solver to find the minimum cost path.

---

## References

- [PUC-SP Class Material](https://pplx-res.cloudinary.com/image/private/user_uploads/27709701/a31aabec-aeef-42c0-b4cd-9024927871af/Screenshot-2025-05-14-at-13.24.26.jpg)
- Dijkstra, E. W. (1959). A note on two problems in connexion with graphs.

#

This README provides a complete, clear, and actionable guide for solving Example 1 with Dijkstra’s algorithm, including all tableaus, explanations, and step-by-step solutions in both Python and Excel Solver.



