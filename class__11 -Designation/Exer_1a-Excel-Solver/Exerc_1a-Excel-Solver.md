


# Exercise 1:  Problem in Excel: Step-by-Step Solution

This guide shows how to solve the assignment problem from the image using **Excel Solver**. All formulas, tables, and steps are included so you can reproduce the solution in Excel.

---

### Problem Statement

Three tasks must be assigned to three machines and all tasks can be done on any machine,
but with different costs, as described in the scheme below.

<br>

### Problem Recap

- **3 tasks** must be assigned to **3 machines**.
- Each task can be done by any machine, but with different costs.
- Each task must be assigned to exactly one machine, and each machine to exactly one task.
- **Goal:** Minimize total assignment cost.

### Cost Table

|         | Machine 1 | Machine 2 | Machine 3 |
|---------|-----------|-----------|-----------|
| Task 1  |     2     |     4     |     3     |
| Task 2  |     1     |     3     |     2     |
| Task 3  |     5     |     2     |     4     |

---

## Step 1: Set Up the Excel Spreadsheet

### 1. Enter the Cost Matrix

|     | B    | C    | D    |
|-----|------|------|------|
|     | M1   | M2   | M3   |
| T1  |  2   |  4   |  3   |
| T2  |  1   |  3   |  2   |
| T3  |  5   |  2   |  4   |

- Place this table in cells **B2:D4**.

### 2. Create the Decision Variable Table

|     | G    | H    | I    |
|-----|------|------|------|
|     | M1   | M2   | M3   |
| T1  | x11  | x12  | x13  |
| T2  | x21  | x22  | x23  |
| T3  | x31  | x32  | x33  |

- Place this table in **G2:I4**.
- These cells will be filled with 0 or 1 by the Solver (1 = assigned, 0 = not assigned).

### 3. Calculate the Total Cost

In cell **K2**, enter:

```

=SUMPRODUCT(B2:D4, G2:I4)

```

This formula multiplies each assignment by its cost and sums the total.

### 4. Add Row and Column Sums for Constraints

#### Row Sums (Each Task Assigned Once)

- In **J2**: `=SUM(G2:I2)`
- In **J3**: `=SUM(G3:I3)`
- In **J4**: `=SUM(G4:I4)`

#### Column Sums (Each Machine Assigned Once)

- In **G5**: `=SUM(G2:G4)`
- In **H5**: `=SUM(H2:H4)`
- In **I5**: `=SUM(I2:I4)`

---

## Step 2: Configure Excel Solver

1. **Go to**: Data > Solver
2. **Set Objective**:  
   - Set **K2** (total cost) to **Minimize**.
3. **By Changing Variable Cells**:  
   - Select **G2:I4**.
4. **Add Constraints**:
   - **J2:J4 = 1** (each task assigned once)
   - **G5:I5 = 1** (each machine assigned once)
   - **G2:I4 = binary** (only 0 or 1 allowed)
5. **Choose Solving Method**:  
   - Use "Simplex LP" or "GRG Nonlinear" (either works for this size).
6. **Click Solve**.

---

## Step 3: Solution Example

After running Solver, you should get a solution like:

|     | M1 | M2 | M3 | Row Sum |
|-----|----|----|----|---------|
| T1  |  1 |  0 |  0 |   1     |
| T2  |  0 |  0 |  1 |   1     |
| T3  |  0 |  1 |  0 |   1     |
|Col Sum| 1|  1 |  1 |         |

- **Task 1 → Machine 1** (cost 2)
- **Task 2 → Machine 3** (cost 2)
- **Task 3 → Machine 2** (cost 2)

**Total minimum cost:** 6

---

## Excel Table and Formula Summary

|     | M1   | M2   | M3   | Row Sum |
|-----|------|------|------|---------|
| T1  | G2   | H2   | I2   | J2      |
| T2  | G3   | H3   | I3   | J3      |
| T3  | G4   | H4   | I4   | J4      |
|Col Sum|G5 | H5   | I5   |         |

- **Total Cost:** `=SUMPRODUCT(B2:D4, G2:I4)`
- **Row Sums:** `=SUM(G2:I2)`, etc.
- **Column Sums:** `=SUM(G2:G4)`, etc.

---

## Result (in English)

**The optimal assignment is:**
- Task 1 to Machine 1 (cost 2)
- Task 2 to Machine 3 (cost 2)
- Task 3 to Machine 2 (cost 2)

**Total minimum cost:** 6



