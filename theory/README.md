# Theory of Computation Sprint Challenge

## Computation

Fill out truth tables for the following expressions:

1. `(A ∧ ¬B)`   
(alternate: `(A && !B)`)
```
A     B     result
-------------------
0     0       0 && 1 = 0
0     1       0 && 0 = 0
1     0       1 && 1 = 1
1     1       1 && 0 = 0
```

2. `(¬A ∨ B) ∧ ¬(A ∧ ¬B)`   
(alternate: `(!A || B) && !(A && !B)`)
```
A     B     result
-------------------
0     0       (1 || 0) && !(0 && 1) = 1 && !0 = 1
0     1       (1 || 1) && !(0 && 0) = 1 && !0 = 1
1     0       (0 || 0) && !(1 && 1) = 0 && !1 = 0
1     1       (0 || 1) && !(1 && 0) = 1 && !0 = 1
```

3. `¬(A ∧ B) ∨ ( (A ∧ C) ∧ ¬(B ∨ ¬C) )`   
(alternate: `!(A && B) || ( (A && C) && !(B || !C) )`)
  * (Hint: Is it possible to calculate this using code?)
```
A     B     C     result
-------------------------
0     0     0       1
0     0     1       1
0     1     0       1
0     1     1       1
1     0     0       1
1     0     1       1
1     1     0       0
1     1     1       0
```
<!-- 
def table3(A, B, C):
	return not (A and B) or ( (A and C) and not (B or not C) )

print(table3(0, 0, 0)); #1 
print(table3(0, 0, 1)); #1
print(table3(0, 1, 0)); #1
print(table3(0, 1, 1)); #1
print(table3(1, 0, 0)); #1
print(table3(1, 0, 1)); #1
print(table3(1, 1, 0)); #0
print(table3(1, 1, 1)); #0 
-->

## STRETCH GOAL

The sum of two binary digits can be represented with the following truth table:

* A + B
```
A     B     CARRY   SUM
------------------------
0     0       0      0
0     1       0      1
1     0       0      1
1     1       1      0
```
This can be represented with boolean algebra like so:

* `SUM = A ⊕ B`  (alternate: `A ^ B` or `A xor B`)
* `CARRY = A ∧ B`  (alternate: `A && B`)


How can you represent the SUM and CARRY of adding THREE digits with a truth table and in boolean algebra?

* A + B + C
```
A     B     C      carry   sum
--------------------------------
0     0     0        ?      ?
0     0     1        ?      ?
0     1     0        ?      ?
0     1     1        ?      ?
1     0     0        ?      ?
1     0     1        ?      ?
1     1     0        ?      ?
1     1     1        ?      ?
```
* SUM = ?
* CARRY = ?
