# Linear Programming Chip Production

## Project Description
This project aims to maximize the weekly profit of a chip manufacturing plant given certain constraints.

## Problem Statement
Given time as a resource to produce a chip, the profit per unit and the cost per unit determine at most 5 products to be utilized while maximizing profit.

<i>*Specific constraints are defined in the model creation notebook.

## Objective
To maximize the profit we establish two decision variables and three associated coefficients to drive production constraints.

### Decision Variables
$X_i$ = The number of microchips of product $i$ to produce in a week $(i = 1,2,3...10)$<br>
$Y_i$ = A binary variable identifying whther to produce (1); or not to produce a product $i$ in a week $(i = 1,2,3...10)$

### Coefficients
$T_i$ = Time to produce $i$ product in minutes $(i=1,2,3...10)$ <br>
$P_i$ = Profit per unit for produt $i$ $(i=1,2,3...10)$<br>
$C_i$ = Cost per unit for product $i$ $(i=1,2,3...10)$<br>


```math
Maximize \sum_{i = 1}^{10}X_i(P_i-C_i) \\
Given \begin{align}
\sum_{i=1}^{10} X_i T_i &\leq 7200 \\
\sum_{i=1}^{10} X_i &\leq 750 \\
\sum_{i=1}^{10} Y_i &= 5 \\
X_i &\geq 100Y_i \quad \forall i \in \{1,2,3 \ldots 10\} \\
X_i &\leq 750Y_i \quad \forall i \in \{1,2,3 \ldots 10\} \\
Y_i &\in \{1,0\} \quad \forall i \in \{1,2,3 \ldots 10\} \\
X_i &\geq 0 \quad \forall i \in \{1,2,3 \ldots 10\}
\end{align}
```
### Formulation Notes
Constraints 4 and 5 create a logical connection between units produced and whether to produce an item or not.They ensure each amount produced is either produced between the minimum and the maximum or not at all.

## Final conclusion
Implementing the above formulation in python Linear Programming we determine the below are the most optimal products to produce for maximum profit

### Final Production Variables

| Product | Product Decision | Quantity to Produce |
|---------|------------------|---------------------|
| 1       | Y                | 100                 |
| 2       | N                | 0                   |
| 3       | Y                | 100                 |
| 4       | Y                | 200                 |
| 5       | N                | 0                   |
| 6       | N                | 0                   |
| 7       | Y                | 250                 |
| 8       | N                | 0                   |
| 9       | Y                | 100                 |
| 10      | N                | 0                   |
