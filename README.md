# Multi-Index Allocation Optimization with Pyomo 🎯

This repository contains a multi–index mixed-integer optimization model implemented using **Pyomo**, with a solver backend of **GAMS/CPLEX**.  
The notebook demonstrates how to construct a 3-dimensional binary assignment model using compatibility matrices and capacity restrictions.

---

## 📂 Contents
- **Modeling.ipynb** – Main Jupyter notebook containing:
  - Data import and preprocessing (`NumPy` matrices `s` and `a`)
  - Pyomo set and index structure creation
  - 3-index binary decision variable design  
    `delta[c, d, h] ∈ {0,1}`
  - Objective function involving a variable `model.w`
  - Constraint sets (capacity, compatibility, selection limits)
  - Solver interaction using GAMS/CPLEX
  - Printing optimal allocations and the objective value

---

## 🔍 Problem Overview

The optimization problem involves:

### **Data Inputs**
- `s` – A binary compatibility matrix  
- `a` – A secondary matrix with capacity or adjacency structure  
- Sets:
  - `dset` – items/days/demands
  - `jset` – time periods or machines
  - `cset` – categories, classes, or clusters
  - Additional structural sets created in the notebook

### **Decision Variable**

delta[c, d, h] ∈ {0, 1}

- 1 → assignment is chosen  
- 0 → assignment is not chosen  



### **Objective**
A scalar optimization target represented by:

