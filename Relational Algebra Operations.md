# Database as a Set of Relations
- A database is represented as **relations (tables)**.
- Each relation contains multiple **tuples (rows)**.
- Each tuple **must** be **unique**.

---
## Three Core Operators

**1. Filtering (Select σ)**  
- Selects rows based on a condition.  
- Operand: One relation.  

**2. Slicing (Project π)**  
- Selects specific columns.  
- Operand: One relation.  

**3. Combining (Join ⋈)**  
- Combines two relations. 
- Types of joins:  
  - **General Join / Theta Join (⋈θ)**: two operands, condition-based  
  - **Equi Join (⋈)**: equality-based  
  - **Natural Join (⨝)**: automatically joins on all common attributes  

Always ensure the operator and operand are in the correct order.

---
## Example Relation

**R (A, B, C)**

| A | B | C | Note |
|---|---|---|---|
| 1 | 2 | 3 | |
| 4 | 5 | 6 | <- all tuples must be DISTINCT |
| 7 | 8 | 9 | |

---
## Selection (σ)

**Condition:** `B = 5 AND A >= 3`

| A | B | C | → σ (B=5 AND A>=3)(R) |
|---|---|---|---|
| 4 | 5 | 6 | |
| 7 | 5 | 6 | |

Selection returns only tuples satisfying the condition.

---
## Projection (π)

- Select specific columns (attributes).  
- May produce duplicate tuples.

**Example:** Project C and B from R1

| B | C |
|---|---|
| 6 | 5 |
| 6 | 5 |

---
## Cartesian Product (×) [CROSS PRODUCT]

**T(A, B)**

| A | B |
|---|---|
| 1 | 2 |
| 3 | 4 |
| 5 | 6 |

**S (B, C, D)**

| B | C | D |
|---|---|---|
| 2 | 5 | 6 |
| 4 | 7 | 8 |
| 9 | 10 | 11 |

**Result of T × S (9 tuples):** (Concatenation)

| A | T.B | S.B | C | D |
|---|-----|-----|---|---|
| 1 | 2 | 2 | 5 | 6 |
| 1 | 2 | 4 | 7 | 8 |
| 1 | 2 | 9 | 10 | 11 |
| 3 | 4 | 2 | 5 | 6 |
| 3 | 4 | 4 | 7 | 8 |
| 3 | 4 | 9 | 10 | 11 |
| 5 | 6 | 2 | 5 | 6 |
| 5 | 6 | 4 | 7 | 8 |
| 5 | 6 | 9 | 10 | 11 |
| 5 | 6 | 2 | 5 | 6 |
| 5 | 6 | 4 | 7 | 8 |
| 5 | 6 | 9 | 10 | 11 |

---
## Joins

### 1. General Join / Theta Join (⋈θ)
**Symbol:** `⋈θ`

- Joins two relations based on a **condition**.

**Example:** `T ⋈(A >= C) S`

**General Condition:**
- T × S
- A >= C

| A | T.B | S.B | C | D |
|---|-----|-----|---|---|
| 5 | 6 | 2 | 5 | 6 |

---
### 2. Equi-Cross Product
**Symbol:** `σ (T.B = S.B) (T × S)`

- Cartesian product filtered by equality.

| A | T.B | S.B | C | D | Note |
|---|-----|-----|---|---|---|
| 1 | 2 | 2 | 5 | 6 | EQUI CROSS PRODUCT |
| 3 | 4 | 4 | 7 | 8 | 2 TUPLES |

---
### 3. Equi Join (⋈)

**Symbol:** `T ⋈(T.B = S.B) S`

- Combines tuples where specified attributes are equal.

**U (A, B, C)**

| A | B | C |
|---|---|---|
| 1 | 2 | 3 |
| 6 | 7 | 8 |
| 9 | 7 | 8 |

**W (B, C, D)**

| B | C | D |
|---|---|---|
| 2 | 3 | 4 |
| 2 | 3 | 5 |
| 7 | 8 | 10 |

**Condition:** 
- `U.B = W.B` AND `U.C = W.C`

**Result:**

| A | U.B | U.C | W.B | W.C | D |
|---|-----|-----|-----|-----|---|
| 1 | 2 | 3 | 2 | 3 | 4 |
| 1 | 2 | 3 | 2 | 3 | 5 |
| 6 | 7 | 8 | 7 | 8 | 10 |
| 9 | 7 | 8 | 7 | 8 | 10 |

---
### 4. Natural Join (⨝)

**Symbol:** `⨝`

- Automatically joins on all **common attributes**.  
- Common columns appear **only once** in the result.

**Conditions of Natural Join:**
- Equi Join
- Joins on all common domains
- The common domains are not repeated in the result

**Example:** `U ⨝ W`

- `U.B = W.B` AND `U.C = W.C`

**Equi-Join:**

| A | U.B | U.C | W.B | W.C | D |
|---|-----|-----|-----|-----|---|
| 1 | 2 | 3 | 2 | 3 | 4 |
| 1 | 2 | 3 | 2 | 3 | 5 |
| 6 | 7 | 8 | 7 | 8 | 10 |
| 9 | 7 | 8 | 7 | 8 | 10 |

**Natural Join:**

| A | B | C | D |
|---|---|---|---|
| 1 | 2 | 3 | 4 |
| 1 | 2 | 3 | 5 |
| 6 | 7 | 8 | 10 |
| 9 | 7 | 8 | 10 |

- Natural joins remove duplicates automatically.  
- Always ensure tuples are distinct.  
- Use small, clear examples to visualize joins.

---
