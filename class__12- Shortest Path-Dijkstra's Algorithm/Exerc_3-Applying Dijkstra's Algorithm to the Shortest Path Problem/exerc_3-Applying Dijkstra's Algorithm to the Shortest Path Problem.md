

## Example 3: Step-by-Step Tableau for Dijkstra's Algorithm

Below are the tableaus (tabulações) representing each iteration of Dijkstra's algorithm for Example 3, as described in the PDF[^1].

### **Network Data**

- Nodes: A (source), B, C, D, E (destination)
- Arc weights (in seconds):  
  - A→B: 25  
  - A→C: 28  
  - B→D: 22  
  - D→E: 18  

### **Tableau 1: Initialization**

| Node | Distance | Predecessor | Status   |
|------|----------|-------------|----------|
| A    | 0        | -           | Permanent|
| B    | ∞        | -           | Temporary|
| C    | ∞        | -           | Temporary|
| D    | ∞        | -           | Temporary|
| E    | ∞        | -           | Temporary|

### **Tableau 2: After Visiting A**

- Update B: 0 + 25 = 25 (Predecessor: A)
- Update C: 0 + 28 = 28 (Predecessor: A)

| Node | Distance | Predecessor | Status   |
|------|----------|-------------|----------|
| A    | 0        | -           | Permanent|
| B    | 25       | A           | Temporary|
| C    | 28       | A           | Temporary|
| D    | ∞        | -           | Temporary|
| E    | ∞        | -           | Temporary|

### **Tableau 3: After Visiting B**

- Update D: 25 + 22 = 47 (Predecessor: B)

| Node | Distance | Predecessor | Status   |
|------|----------|-------------|----------|
| A    | 0        | -           | Permanent|
| B    | 25       | A           | Permanent|
| C    | 28       | A           | Temporary|
| D    | 47       | B           | Temporary|
| E    | ∞        | -           | Temporary|

### **Tableau 4: After Visiting C**

- No updates (C has no outgoing arcs).

| Node | Distance | Predecessor | Status   |
|------|----------|-------------|----------|
| A    | 0        | -           | Permanent|
| B    | 25       | A           | Permanent|
| C    | 28       | A           | Permanent|
| D    | 47       | B           | Temporary|
| E    | ∞        | -           | Temporary|

### **Tableau 5: After Visiting D**

- Update E: 47 + 18 = 65 (Predecessor: D)

| Node | Distance | Predecessor | Status   |
|------|----------|-------------|----------|
| A    | 0        | -           | Permanent|
| B    | 25       | A           | Permanent|
| C    | 28       | A           | Permanent|
| D    | 47       | B           | Permanent|
| E    | 65       | D           | Temporary|

### **Tableau 6: After Visiting E (Final)**

| Node | Distance | Predecessor | Status   |
|------|----------|-------------|----------|
| A    | 0        | -           | Permanent|
| B    | 25       | A           | Permanent|
| C    | 28       | A           | Permanent|
| D    | 47       | B           | Permanent|
| E    | 65       | D           | Permanent|

---

### **Optimal Path and Cost**

- **Path:** A → B → D → E
- **Total Time:** 65 seconds

These tableaus follow the standard Dijkstra's procedure, allowing step-by-step verification and understanding of the shortest path calculation in the network.



[
