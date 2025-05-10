
# Exer. 5b -  Factory Task Assignment Using Excel Solver  

### Problem Statement

In a factory there are 4 different cutting machines. 4 tasks must be processed daily. Tasks can be performed on any of the machines. The table below represents the processing times, in hours, of each task on each of the machines. Designate a machine for each task in such a way as to minimize the total time spent.
 

---

## Step 1: Input the Cost Matrix in Excel  
Enter the processing times (hours) in a 4x4 grid.  

| Machine \ Task | Task 1 | Task 2 | Task 3 | Task 4 |
|----------------|--------|--------|--------|--------|
| **Machine 1**  | 5      | 24     | 13     | 7      |
| **Machine 2**  | 10     | 25     | 3      | 23     |
| **Machine 3**  | 28     | 9      | 8      | 5      |
| **Machine 4**  | 10     | 17     | 15     | 3      |

---

## Step 2: Create the Assignment Matrix  
Add a 4x4 grid for binary decision variables (0 or 1).  

| Machine \ Task | Task 1 | Task 2 | Task 3 | Task 4 |
|----------------|--------|--------|--------|--------|
| **Machine 1**  | 0      | 0      | 0      | 0      |
| **Machine 2**  | 0      | 0      | 0      | 0      |
| **Machine 3**  | 0      | 0      | 0      | 0      |
| **Machine 4**  | 0      | 0      | 0      | 0      |

---

## Step 3: Define Formulas  

### **Objective Function (Total Time)**  
In cell `B10`, calculate the total time using:  
```

=SUMPRODUCT(B2:E5, B8:E11)

```

### **Constraints**  
- **Each machine assigned to one task**:  
  In cells `F8:F11` (row sums):  
```

=SUM(B8:E8)  // For Machine 1

```
- **Each task assigned to one machine**:  
In cells `B12:E12` (column sums):  
```

=SUM(B8:B11)  // For Task 1

```

---

## Step 4: Configure Excel Solver  

1. **Open Solver**:  
 Go to `Data` > `Solver`.  

2. **Set Parameters**:  
 - **Objective**: `B10` (Minimize).  
 - **Variables**: `B8:E11` (Assignment matrix).  
 - **Constraints**:  
   - `B8:E11 = binary` (binary variables).  
   - `F8:F11 = 1` (each machine assigned once).  
   - `B12:E12 = 1` (each task assigned once).  

3. **Solve**:  
 Click `Solve` and select `Keep Solver Solution`.  

---

## Step 5: Optimal Assignment  

| Machine \ Task | Task 1 | Task 2 | Task 3 | Task 4 |
|----------------|--------|--------|--------|--------|
| **Machine 1**  | 0      | 0      | 0      | 1      |
| **Machine 2**  | 0      | 0      | 1      | 0      |
| **Machine 3**  | 0      | 1      | 0      | 0      |
| **Machine 4**  | 1      | 0      | 0      | 0      |

**Total Time**:  
- Machine 1 → Task 4: 7  
- Machine 2 → Task 3: 3  
- Machine 3 → Task 2: 9  
- Machine 4 → Task 1: 10  
**Total = 7 + 3 + 9 + 10 = 19**  

---

## Final Excel Setup  

|          | B       | C       | D       | E       | F       |
|----------|---------|---------|---------|---------|---------|
| **8**    | 0       | 0       | 0       | 1       | `=SUM(B8:E8)` → 1 |
| **9**    | 0       | 0       | 1       | 0       | `=SUM(B9:E9)` → 1 |
| **10**   | 0       | 1       | 0       | 0       | `=SUM(B10:E10)` → 1 |
| **11**   | 1       | 0       | 0       | 0       | `=SUM(B11:E11)` → 1 |
| **12**   | 1       | 1       | 1       | 1       |         |

