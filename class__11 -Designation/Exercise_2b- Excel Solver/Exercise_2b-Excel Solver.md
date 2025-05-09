


## Exercise 2b: Solved Excel Solver

### Problem Statement :

Make the mathematical model and determining the designation and the minimum cost of the process.


## **Step 1: Enter the Cost Matrix in Excel**

|  | A | B | C | D | E |
| :-- | :-- | :-- | :-- | :-- | :-- |
|  |  | T1 | T2 | T3 | T4 |
| 2 |  |  |  |  |  |
| 3 | A | 5 | 24 | 13 | 7 |
| 4 | B | 10 | 25 | 3 | 23 |
| 5 | C | 28 | 9 | 8 | 5 |
| 6 | D | 10 | 17 | 15 | 3 |


---

## **Step 2: Create the Assignment Matrix**

Next to your cost matrix, create a 4x4 grid for assignments (let’s say in G3:J6).
Each cell will be a binary variable (0 or 1):

- 1 if the operator is assigned to that task, 0 otherwise.

|  | G | H | I | J |
| :-- | :-- | :-- | :-- | :-- |
|  | T1 | T2 | T3 | T4 |
| 3 |  |  |  |  |
| 4 |  |  |  |  |
| 5 |  |  |  |  |
| 6 |  |  |  |  |


---

## **Step 3: Objective Function (Total Cost)**

In a cell (say, **L2**), calculate the total cost using the SUMPRODUCT function:

```excel
=SUMPRODUCT(B3:E6, G3:J6)
```

This multiplies each cost by its assignment (0 or 1) and sums the result.

---

## **Step 4: Add Constraints for Solver**

You need to ensure:

- Each worker is assigned to **exactly one** task.
- Each task is assigned to **exactly one** worker.

**For each row (worker):**
In K3: `=SUM(G3:J3)` (copy down to K6)
Set each to **equal 1** in Solver.

**For each column (task):**
In G7: `=SUM(G3:G6)` (copy right to J7)
Set each to **equal 1** in Solver.

---

## **Step 5: Configure Solver**

1. Go to **Data** > **Solver**.
2. **Set Objective:**
    - Set Objective: `L2` (or wherever your total cost is).
    - To: **Min**
3. **By Changing Variable Cells:**
    - `G3:J6` (your assignment matrix)
4. **Add Constraints:**
    - `G3:J6` = binary (use "bin" in Solver)
    - `K3:K6` = 1 (each worker assigned to one task)
    - `G7:J7` = 1 (each task assigned to one worker)
5. Click **Solve**.

---

## **Step 6: Interpret the Results**

Solver will fill the assignment matrix with 0s and 1s.
For each row, the "1" indicates which task that worker is assigned to.

### **Example Solution (Optimal):**

| Worker | Task Assigned | Cost |
| :-- | :-- | :-- |
| A | 1 | 5 |
| B | 3 | 3 |
| C | 2 | 9 |
| D | 4 | 3 |
| **Total** |  | **20** |


---

## **Summary Table for README**

| Worker | Task 1 | Task 2 | Task 3 | Task 4 | Assignment |
| :-- | :-- | :-- | :-- | :-- | :-- |
| A | 5 | 24 | 13 | 7 | 1 (T1) |
| B | 10 | 25 | 3 | 23 | 3 (T3) |
| C | 28 | 9 | 8 | 5 | 2 (T2) |
| D | 10 | 17 | 15 | 3 | 4 (T4) |

**Minimum total time: 20**

---

## **Tips**

- Use **conditional formatting** to highlight the "1"s in the assignment matrix for clarity.
- If Solver is not enabled, go to **File > Options > Add-ins > Solver Add-in**.

---

**Ready! You have solved the assignment problem step by step in Excel using Solver, ensuring the minimum total cost is 20.**

