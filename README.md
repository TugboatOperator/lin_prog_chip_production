# Linear Programming Chip Production

## Project Description
This project aims to maximize the weekly profit of a chip manufacturing plant given certain constraints.

## Problem Statement
Given time as a resource to produce a chip, the profit per unit and the cost per unit determine at most 5 products to be utilized while maximizing profit.

<i>*Specific constraints are defined in the model creation notebook.

## Objective
To maximize the profit we establish two decision variables and three associated coefficients to drive production constraints.

![image](https://github.com/user-attachments/assets/a8fe0ad5-d3a6-451f-8eb3-ad659b1cee9f)

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
