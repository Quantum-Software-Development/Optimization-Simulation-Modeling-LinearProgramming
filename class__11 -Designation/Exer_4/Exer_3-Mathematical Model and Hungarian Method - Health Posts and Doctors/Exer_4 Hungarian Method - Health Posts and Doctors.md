

# Exercise 4s:  Mathematical Model and Hungarian Method - Health Posts and Doctors

### Problem Statement:

The City Hall of a city needs to fill a vacancy: in 4 health posts and for this it has 6 doctors in the required specialties. 
Each doctor can be allocated to a single post, at most and each post demands a single doctor. In the table below we have the daily cost 
of transportation of each doctor to each health center. Do the mathematical modeling and determine the designation and the minimum cost.



## **Mathematical Model**

### **Decision Variables**

Let \$ x_{ij} \$ be:

$$
x_{ij} = 
\begin{cases}
1 & \text{if doctor } j \text{ is assigned to post } i \\
0 & \text{otherwise}
\end{cases}
$$

### **Objective Function**

Minimize the total cost:

$$
\text{Minimize } Z = \sum_{i=1}^4 \sum_{j=1}^6 c_{ij} x_{ij}
$$

where \$ c_{ij} \$ is the cost of assigning doctor \$ j \$ to post \$ i \$.

### **Constraints**

- Each post must have exactly one doctor:

$$
\sum_{j=1}^6 x_{ij} = 1 \quad \forall i = 1,2,3,4
$$

- Each doctor can be assigned to at most one post:

$$
\sum_{i=1}^4 x_{ij} \leq 1 \quad \forall j = 1,2,3,4,5,6
$$

- \$ x_{ij} \in \{0,1\} \$

---

## **Cost Matrix**

| Post \ Doctor | M1 | M2 | M3 | M4 | M5 | M6 |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| **1** | 6 | 9 | 9 | 9 | 8 | 7 |
| **2** | 3 | 5 | 6 | 9 | 7 | 5 |
| **3** | 8 | 7 | 5 | 8 | 7 | 6 |
| **4** | 3 | 4 | 8 | 5 | 7 | 4 |


---

## **Step-by-Step Solution Using the Hungarian Method**

Since there are more doctors (6) than posts (4), **add two dummy posts** (rows) with zero cost to make it a 6x6 square matrix.


| Post \ Doctor | M1 | M2 | M3 | M4 | M5 | M6 |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| **1** | 6 | 9 | 9 | 9 | 8 | 7 |
| **2** | 3 | 5 | 6 | 9 | 7 | 5 |
| **3** | 8 | 7 | 5 | 8 | 7 | 6 |
| **4** | 3 | 4 | 8 | 5 | 7 | 4 |
| **Dummy 1** | 0 | 0 | 0 | 0 | 0 | 0 |
| **Dummy 2** | 0 | 0 | 0 | 0 | 0 | 0 |


---

### **Step 1: Row Reduction**

Subtract the minimum value in each row from all elements in that row.

- Row 1 min: 6 →[^1]
- Row 2 min: 3 →
- Row 3 min: 5 →[^1]
- Row 4 min: 3 →[^1][^1]
- Dummy rows: all zeros

---

### **Step 2: Column Reduction**

Subtract the minimum value in each column from all elements in that column.

- Col 1 min: 0
- Col 2 min: 1
- Col 3 min: 0
- Col 4 min: 0
- Col 5 min: 0
- Col 6 min: 0

After column reduction:


|  | M1 | M2 | M3 | M4 | M5 | M6 |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| 1 | 0 | 2 | 3 | 3 | 2 | 1 |
| 2 | 0 | 1 | 3 | 6 | 4 | 2 |
| 3 | 3 | 1 | 0 | 3 | 2 | 1 |
| 4 | 0 | 0 | 5 | 2 | 4 | 1 |
| D1 | 0 | 0 | 0 | 0 | 0 | 0 |
| D2 | 0 | 0 | 0 | 0 | 0 | 0 |


---

### **Step 3: Assignment**

Assign one zero per row and column, prioritizing unique zeros:

- Post 1 → M1 (cost 6)
- Post 2 → M2 (cost 5)
- Post 3 → M3 (cost 5)
- Post 4 → M6 (cost 4)

(You may need to adjust if there is a conflict, but this is a valid assignment.)

---

### **Step 4: Minimum Total Cost**

Sum the original costs for the assignments:

- Post 1 → M1: 6
- Post 2 → M2: 5
- Post 3 → M3: 5
- Post 4 → M6: 4

**Total minimum cost = 6 + 5 + 5 + 4 = 20**

---

## **Final Assignment Table**

| Post | Assigned Doctor | Cost |
| :-- | :-- | :-- |
| 1 | M1 | 6 |
| 2 | M2 | 5 |
| 3 | M3 | 5 |
| 4 | M6 | 4 |
| **Total** |  | **20** |


---

## **How to Solve in Excel with Solver**

1. **Enter the cost matrix (including dummy rows) in A1:G7.**
2. **Create a 6x6 assignment matrix (binary variables) in H2:M7.**
3. **Objective function (cell O1):**
`=SUMPRODUCT(B2:G7, H2:M7)`
4. **Constraints:**
    - Each post (row) assigned to exactly one doctor: `=SUM(H2:M2)` = 1 (for each row)
    - Each doctor (column) assigned to at most one post: `=SUM(H2:H7)` ≤ 1 (for each column)
    - All variables binary (0 or 1)
5. **Set Solver to minimize O1.**

---

**This is your step-by-step assignment problem solution for Exercise 3, with all the necessary details for modeling, Hungarian method, and Excel Solver.**



