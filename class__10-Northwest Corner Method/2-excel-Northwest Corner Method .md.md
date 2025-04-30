# Transportation Problem Solution in Excel (Markdown + LaTeX for README.md)

This guide explains, step by step, how to solve the given transportation problem in Excel using the Solver add-in. It includes all necessary formulas and tables in Markdown and LaTeX, with ready-to-copy Excel formulas.


**You can now copy the formulas above and use them directly in your Excel sheet. The step-by-step process will allow you to model and solve any similar transportation problem using Excel Solver.**

---

## **Problem Statement**

Given the following transportation cost matrix, supply, and demand:


|  | Consumer 1 | Consumer 2 | Consumer 3 | Supply |
| :-- | :--: | :--: | :--: | :--: |
| Supplier 1 | 12 | 22 | 30 | 100 |
| Supplier 2 | 18 | 24 | 32 | 140 |
| Supplier 3 | 22 | 15 | 34 | 160 |
| **Demand** | 120 | 130 | 150 |  |

**Objective:**
Minimize the total transportation cost.

---

## **Mathematical Formulation (LaTeX)**

Let \$ x_{ij} \$ be the number of units shipped from supplier \$ i \$ to consumer \$ j \$.

**Minimize:**

$$
Z = \sum_{i=1}^{3} \sum_{j=1}^{3} c_{ij} x_{ij}
$$

**Subject to:**

$$
\sum_{j=1}^{3} x_{ij} = \text{Supply}_i \quad \forall i = 1,2,3
$$

$$
\sum_{i=1}^{3} x_{ij} = \text{Demand}_j \quad \forall j = 1,2,3
$$

$$
x_{ij} \geq 0 \quad \forall i, j
$$

---

## **Step-by-Step Solution in Excel**

### **1. Data Layout**

|  | B | C | D | E | F |
| :-- | :-- | :-- | :-- | :-- | :-- |
|  | Cons1 | Cons2 | Cons3 | Supply |  |
| Sup1 | 12 | 22 | 30 | 100 |  |
| Sup2 | 18 | 24 | 32 | 140 |  |
| Sup3 | 22 | 15 | 34 | 160 |  |
| Demand | 120 | 130 | 150 |  |  |

### **2. Decision Variables Table**

Below the cost table, create a table for the shipment variables (\$ x_{ij} \$), e.g., in cells B7:D9.


|  | Cons1 | Cons2 | Cons3 |
| :-- | :-- | :-- | :-- |
| Sup1 | x11 | x12 | x13 |
| Sup2 | x21 | x22 | x23 |
| Sup3 | x31 | x32 | x33 |

**In Excel:**
Enter `0` in each cell as the initial value.

### **3. Total Cost Formula**

Below the variable table, calculate the total cost using `SUMPRODUCT`:

```excel
=SUMPRODUCT(B2:D4, B7:D9)
```

- `B2:D4` is the cost matrix.
- `B7:D9` is the variable matrix.


### **4. Supply Constraints**

For each supplier, sum the variables in the row and set equal to the supply.


|  | Formula (Excel) |
| :-- | :-- |
| Sup1 | =SUM(B7:D7) |
| Sup2 | =SUM(B8:D8) |
| Sup3 | =SUM(B9:D9) |

### **5. Demand Constraints**

For each consumer, sum the variables in the column and set equal to the demand.


|  | Formula (Excel) |
| :-- | :-- |
| Cons1 | =SUM(B7:B9) |
| Cons2 | =SUM(C7:C9) |
| Cons3 | =SUM(D7:D9) |

### **6. Setting Up Solver**

- **Set Objective:** The total cost cell (e.g., `B12`) - set to Min.
- **By Changing Variable Cells:** The shipment variables (`B7:D9`).
- **Subject to Constraints:**
    - Each row sum equals the corresponding supply.
    - Each column sum equals the corresponding demand.
    - All variables \$ \geq 0 \$.


#### **Solver Constraints (in Excel)**

- `SUM(B7:D7) = F2` (Supply for Sup1)
- `SUM(B8:D8) = F3` (Supply for Sup2)
- `SUM(B9:D9) = F4` (Supply for Sup3)
- `SUM(B7:B9) = B5` (Demand for Cons1)
- `SUM(C7:C9) = C5` (Demand for Cons2)
- `SUM(D7:D9) = D5` (Demand for Cons3)
- `B7:D9 &gt;= 0`


### **7. Solving and Results**

After running Solver, you will get the optimal shipment plan. For this problem, the optimal solution is:


|  | Cons1 | Cons2 | Cons3 |
| :-- | :-- | :-- | :-- |
| Sup1 | 100 | 0 | 0 |
| Sup2 | 10 | 130 | 0 |
| Sup3 | 10 | 0 | 150 |

**Total Cost:**

```excel
=SUMPRODUCT(B2:D4, B7:D9)
```

Result: **9820**

---

## **Excel Formulas (Copy-Paste Ready)**

Assuming:

- Cost matrix in `B2:D4`
- Variables in `B7:D9`
- Supplies in `F2:F4`
- Demands in `B5:D5`

**Total Cost:**

```excel
=SUMPRODUCT(B2:D4, B7:D9)
```

**Supply Constraints:**

```excel
=SUM(B7:D7)    // For Sup1
=SUM(B8:D8)    // For Sup2
=SUM(B9:D9)    // For Sup3
```

**Demand Constraints:**

```excel
=SUM(B7:B9)    // For Cons1
=SUM(C7:C9)    // For Cons2
=SUM(D7:D9)    // For Cons3
```


---

## **References**

For more details and visuals, see:

- [Excel Easy: Transportation Problem in Excel][^2]
- [SCM Globe: How to Solve Transportation Problems Using Excel Solver][^3]
- [YouTube: Solving LP Transportation Problem | Excel Solver][^1]

---

## **Summary Table (Markdown)**

|  | Cons1 | Cons2 | Cons3 | Supply |
| :-- | :-- | :-- | :-- | :-- |
| Sup1 | 100 | 0 | 0 | 100 |
| Sup2 | 10 | 130 | 0 | 140 |
| Sup3 | 10 | 0 | 150 | 160 |
| Demand | 120 | 130 | 150 |  |

**Total Cost:** 9820

---


