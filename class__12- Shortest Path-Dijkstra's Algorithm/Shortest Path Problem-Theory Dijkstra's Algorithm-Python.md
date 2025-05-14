
# Shortest Path Problem: Theory, Mathematical Formulation, and Dijkstra's Algorithm

## 1. Theoretical Explanation

The **Shortest Path Problem** (also called the minimum path problem) seeks to find the path between two nodes in a network that minimizes the total distance, cost, or travel time.  
- The network consists of a single supply node (origin) and a single demand node (destination), with all other nodes being transshipment nodes (zero supply and demand).
- The problem can be solved using mathematical programming or graph algorithms such as Dijkstra's algorithm.

---

## 2. Mathematical Formulation

Let:

- **Parameters:**  
  \( c_{ij} \) = distance, cost, or time from node \( i \) to node \( j \).

- **Decision Variables:**  
  \( x_{ij} = \begin{cases} 
      1 & \text{if arc } (i, j) \text{ is included in the shortest path} \\
      0 & \text{otherwise}
    \end{cases} \)

- **Objective Function:**  
  Minimize the total cost of the path from the origin to the destination:
  \[
  \min z = \sum_{(i,j)} c_{ij} x_{ij}
  \]

- **Constraints:**  
  - The total flow out of the origin is 1.
  - The total flow into the destination is 1.
  - For all intermediate nodes, the flow in equals the flow out.

---

## 3. Dijkstra's Algorithm: Step-by-Step Procedure

**Initialization:**
- Let \( R \) be the set of labeled (closed) nodes, initially empty.
- Let \( NR \) be the set of unlabeled (open) nodes, initially all nodes.
- Assign distance 0 to the source node and \( \infty \) to all other nodes.

**Algorithm Steps:**
1. While \( NR \) is not empty:
   - Select the node \( k \) in \( NR \) with the smallest tentative distance.
   - Move \( k \) from \( NR \) to \( R \).
   - For each unlabeled successor \( j \) of \( k \):
     - If \( \text{distance}(k) + c_{kj} < \text{distance}(j) \), update \( \text{distance}(j) \) and set \( k \) as the predecessor of \( j \).

---

## 4. Example 3: Oil Company Logistics Network

**Problem:**  
An oil company analyzes the flow of its products in a logistics network from node **A** (origin) to node **E** (destination), passing through intermediate nodes **B, C, D**. Arc weights represent flow time in seconds.

### **Network Structure**

- **A → B:** 25
- **A → C:** 28
- **B → D:** 22
- **C:** No outgoing arcs
- **D → E:** 18

### **Dijkstra's Algorithm Tableaus**

#### **Tableau 1: Initialization**

| Node | Distance | Predecessor | Status     |
|------|----------|-------------|------------|
| A    | 0        | -           | Permanent  |
| B    | ∞        | -           | Temporary  |
| C    | ∞        | -           | Temporary  |
| D    | ∞        | -           | Temporary  |
| E    | ∞        | -           | Temporary  |

#### **Tableau 2: After Visiting A**

| Node | Distance | Predecessor | Status     |
|------|----------|-------------|------------|
| A    | 0        | -           | Permanent  |
| B    | 25       | A           | Temporary  |
| C    | 28       | A           | Temporary  |
| D    | ∞        | -           | Temporary  |
| E    | ∞        | -           | Temporary  |

#### **Tableau 3: After Visiting B**

| Node | Distance | Predecessor | Status     |
|------|----------|-------------|------------|
| A    | 0        | -           | Permanent  |
| B    | 25       | A           | Permanent  |
| C    | 28       | A           | Temporary  |
| D    | 47       | B           | Temporary  |
| E    | ∞        | -           | Temporary  |

#### **Tableau 4: After Visiting C**

| Node | Distance | Predecessor | Status     |
|------|----------|-------------|------------|
| A    | 0        | -           | Permanent  |
| B    | 25       | A           | Permanent  |
| C    | 28       | A           | Permanent  |
| D    | 47       | B           | Temporary  |
| E    | ∞        | -           | Temporary  |

#### **Tableau 5: After Visiting D**

| Node | Distance | Predecessor | Status     |
|------|----------|-------------|------------|
| A    | 0        | -           | Permanent  |
| B    | 25       | A           | Permanent  |
| C    | 28       | A           | Permanent  |
| D    | 47       | B           | Permanent  |
| E    | 65       | D           | Temporary  |

#### **Tableau 6: After Visiting E (Final)**

| Node | Distance | Predecessor | Status     |
|------|----------|-------------|------------|
| A    | 0        | -           | Permanent  |
| B    | 25       | A           | Permanent  |
| C    | 28       | A           | Permanent  |
| D    | 47       | B           | Permanent  |
| E    | 65       | D           | Permanent  |

---

### **Optimal Path and Total Time**

- **Path:** A → B → D → E
- **Total Time:** 25 + 22 + 18 = **65 seconds**

```

graph LR
A --25--> B --22--> D --18--> E

```

---

## 5. Python Implementation Example

```

import heapq

def dijkstra(graph, start):
distances = {node: float('inf') for node in graph}
predecessors = {node: None for node in graph}
distances[start] = 0
queue = [(0, start)]
while queue:
curr_dist, curr_node = heapq.heappop(queue)
for neighbor, weight in graph[curr_node].items():
distance = curr_dist + weight
if distance < distances[neighbor]:
distances[neighbor] = distance
predecessors[neighbor] = curr_node
heapq.heappush(queue, (distance, neighbor))
return distances, predecessors

# Example 3 Graph

graph = {
'A': {'B': 25, 'C': 28},
'B': {'D': 22},
'C': {},
'D': {'E': 18},
'E': {}
}

distances, predecessors = dijkstra(graph, 'A')
print("Distances:", distances)
print("Predecessors:", predecessors)

```

---

## 6. References

- [Class Material PDF: Caminho Mínimo e LP - PUC-SP](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/27709701/1f6878e6-1eb2-41b6-835a-7bb02c00cc10/class_12-Caminho-Minimoe-LP.pdf)

---

**This README provides a comprehensive overview, mathematical formulation, algorithmic steps, tableaus, and a worked example for the shortest path problem as presented in your course material.**


