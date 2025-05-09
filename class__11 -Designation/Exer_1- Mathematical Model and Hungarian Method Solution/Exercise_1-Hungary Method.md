## Exercise 1: Mathematical Model and Hungarian Method Solution

## Problem Statement

**Three tasks must be assigned to three machines. Each task can be performed on any machine, but with different costs. Assign each task to one machine, and each machine to one task, minimizing the total cost.**

### Cost Matrix

|         | Machine 1 | Machine 2 | Machine 3 |
|---------|-----------|-----------|-----------|
| Task 1  |     2     |     4     |     3     |
| Task 2  |     1     |     3     |     2     |
| Task 3  |     5     |     2     |     4     |

---

## 1. Hungarian Method (Step by Step)

### **Step 1: Subtract Row Minimums**

Subtract the minimum value in each row from all elements in that row.

- Row 1 min: 2 → [0, 2, 1]
- Row 2 min: 1 → [0, 2, 1]
- Row 3 min: 2 → [3, 0, 2]

**Matrix after row subtraction:**

|         | M1 | M2 | M3 |
|---------|----|----|----|
| Task 1  |  0 |  2 |  1 |
| Task 2  |  0 |  2 |  1 |
| Task 3  |  3 |  0 |  2 |

---

### **Step 2: Subtract Column Minimums**

Subtract the minimum value in each column from all elements in that column.

- Col 1 min: 0 → [0, 0, 3]
- Col 2 min: 0 → [2, 2, 0]
- Col 3 min: 1 → [0, 0, 1]

**Matrix after column subtraction:**

|         | M1 | M2 | M3 |
|---------|----|----|----|
| Task 1  |  0 |  2 |  0 |
| Task 2  |  0 |  2 |  0 |
| Task 3  |  3 |  0 |  1 |

---

### **Step 3: Assignment (Cover Zeros)**

- Cover all zeros using the minimum number of lines (rows or columns).
- Assign tasks to machines where possible (one zero per row/column).

**Optimal Assignment:**
- Task 1 → Machine 1 (cost 2)
- Task 2 → Machine 3 (cost 2)
- Task 3 → Machine 2 (cost 2)

**Total Minimum Cost = 2 + 2 + 2 = 6**

---

## 2. Excel Solver Step-by-Step

### **A. Excel Table Setup**

#### 1. **Cost Table (A1:D4)**

|     | B    | C    | D    |
|-----|------|------|------|
|     | M1   | M2   | M3   |
| T1  |  2   |  4   |  3   |
| T2  |  1   |  3   |  2   |
| T3  |  5   |  2   |  4   |

#### 2. **Decision Variables Table (F1:I4)**

|     | G    | H    | I    |
|-----|------|------|------|
|     | M1   | M2   | M3   |
| T1  | x11  | x12  | x13  |
| T2  | x21  | x22  | x23  |
| T3  | x31  | x32  | x33  |

Each cell is 0 or 1 (to be filled by Solver).

#### 3. **Objective Function (K2)**

```

=SUMPRODUCT(B2:D4, G2:I4)

```

#### 4. **Row Constraints (One task per machine)**

- J2: `=SUM(G2:I2)` (should be 1)
- J3: `=SUM(G3:I3)` (should be 1)
- J4: `=SUM(G4:I4)` (should be 1)

#### 5. **Column Constraints (One machine per task)**

- G5: `=SUM(G2:G4)` (should be 1)
- H5: `=SUM(H2:H4)` (should be 1)
- I5: `=SUM(I2:I4)` (should be 1)

---

### **B. Solver Configuration**

- **Set Objective:** K2 (Minimize)
- **By Changing Variables:** G2:I4
- **Add Constraints:**
  - J2:J4 = 1
  - G5:I5 = 1
  - G2:I4 = binary

---PAREI AQUI !!!!___

### **C. Example of Solution Table**

|     | M1 | M2 | M3 | Row Sum |
|-----|----|----|----|---------|
| T1  |  1 |  0 |  0 |   1     |
| T2  |  0 |  0 |  1 |   1     |
| T3  |  0 |  1 |  0 |   1     |
|Col Sum| 1|  1 |  1 |         |

---

## **Result (in English)**

**The optimal assignment is:**
- Task 1 to Machine 1 (cost 2)
- Task 2 to Machine 3 (cost 2)
- Task 3 to Machine 2 (cost 2)

**Total minimum cost:** 6

-