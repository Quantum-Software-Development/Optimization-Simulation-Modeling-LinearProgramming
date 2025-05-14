
## Exercise 2: 

### Statement:

Applying Dijkstra's Algorithm to the Shortest Path Problem

**Step 1:** Assign the value 0 to the source node (1) and ∞ (infinity) to all other nodes, as shown in the graph:


INSERIR O GRAFO


### Dijkstra's Algorithm – Node Labeling Process

- **Node labeling** is the process of assigning values to nodes to represent the shortest known distance from the source node at each step of the algorithm.
- At each iteration, nodes are divided into two sets:
    - **Labeled nodes (closed):** Nodes for which the shortest path from the source has been definitively found.
    - **Unlabeled nodes (open):** Nodes for which the shortest path is still being determined.


#### Steps:

1. **Initialization:**
    - Set \$ R = \{\} \$ (the set of labeled nodes is empty).
    - Set \$ NR = \{1, 2, 3, ..., n\} \$ (all nodes are initially unlabeled).
    - Assign 0 to the source node and ∞ to all others.
2. **While \$ NR \neq \emptyset \$:**
    - Select the unlabeled node with the smallest value (node \$ k \$).
    - Move node \$ k \$ to the set of labeled nodes \$ R \$.
    - For each unlabeled successor node \$ j \$ of \$ k \$:
        - Add the value of node \$ k \$ to the cost of the arc from \$ k \$ to \$ j \$.
        - If this new value is less than the current value of node \$ j \$, update node \$ j \$ with the new value and set \$ k \$ as its predecessor.

#### Importance of "Where I Came From" and "Where I Am":

- **Where I came from:** In the tableau, the rows indicate the predecessor node, which is crucial for reconstructing the shortest path at the end.
- **Where I am:** The columns represent the current node being evaluated in each iteration.

---

### Step-by-Step Tableaus

| 1* | 2* | 3* | 4* | 5* | 6 | 7* | 8* | 9* |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| 0 | ∞ | ∞ | ∞ | ∞ | ∞ | ∞ | ∞ | ∞ |
| - | (1, 11) | (1, 9) | ∞ | ∞ | ∞ | ∞ | ∞ | ∞ |
| - | (1, 11) | - | (3, 17) | (3, 15) | ∞ | ∞ | ∞ | ∞ |
| - | - | - | (2, 15) | (3, 15) | ∞ | ∞ | ∞ | ∞ |
| - | - | - | - | (3, 15) | (4, 21) | (4, 21) | (5, 19) | ∞ |
| - | - | - | - | - | (4, 21) | (4, 20) | (5, 19) | (8, 25) |
| - | - | - | - | - | (4, 21) | (4, 20) | - | (7, 24) |

**Minimum Path:**
1 → 2 → 4 → 7 → 9 = 24

---

### Summary

- **Node labeling** (rotulação dos nós) is a fundamental part of Dijkstra's algorithm, systematically updating the shortest distances and predecessors for each node.
- The tableau tracks, for each node, both the current shortest distance and the node from which that distance was reached.
- At the end, by tracing back from the destination node using the predecessors, you reconstruct the shortest path.


