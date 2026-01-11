# Pyomo Introduction
This repository demonstrates the use of **Pyomo** for solving different classes of optimization problems, including:

| Term  | Description                              |
| ----- | ---------------------------------------- |
| LP    | Linear Programming                       |
| MILP  | **Mixed-Integer** Linear Programming     |
| QP    | Quadratic Programming                    |
| NLP   | **Nonlinear** Programming                |
| MINLP | **Mixed-Integer Nonlinear** Programming  |

## Getting Started
### Installing with Conda
The required solvers and native dependencies are included in `environment.yml`
```bash
conda env create -f environment.yml
conda activate pyomo_env
```

### Installing with pip
```bash
pip install -r requirements.txt
```

#### <b style="color:red">IMPORTANT NOTE</b> something beginners often miss
Pyomo is a modeling language — it builds mathematical models,  
but **external solvers are required to actually solve them**.  
  
Therefore the solver **must already be installed** on your system.  

Example checks:
```bash
glpsol --version
ipopt -v
```
---

#### Types of Solver
Each Solver can handle a specific task.  
Note: Not every solver supports integer variables or nonlinear constraints.  
Always match the solver to the problem type.  
##### Open-source solvers
| Solver | Task it Solves |
| ------ | -------------- |
| **GLPK** | LP, MILP |
| **CBC** | MILP |
| **HiGHS** | LP, MILP, QP |
| **Ipopt** | NLP (continuous only) |
| **Couenne** | MINLP |
| **SCIP** | MILP, MINLP |
| **APOPT** | NLP, MINLP |
| **BONMIN** | MINLP |
##### Commercial solvers (licensed)
| Solver | Task it Solves |
| ------ | -------------- |
| **Gurobi** | LP, QP, MILP |
| **CPLEX** | LP, QP, MILP |
| **KNITRO** | NLP, MINLP |
| **BARON** | global NLP, MINLP |
| **MOSEK** | LP, QP, conic | 

#### Solver References
The following solvers are used or demonstrated in this repository:  
[![GLPK](https://img.shields.io/badge/GLPK-blue?style=plastic)](https://www.gnu.org/software/glpk/#downloading)  
[![IPOPT](https://img.shields.io/badge/IPOPT-blue?style=plastic)](https://coin-or.github.io/Ipopt/INSTALL.html)  
[![HiGHS](https://img.shields.io/badge/HiGHS-blue?style=plastic)](https://ergo-code.github.io/HiGHS/dev/installation/)  
[![BONMIN](https://img.shields.io/badge/BONMIN-blue?style=plastic)](https://dev.ampl.com/solvers/bonmin/index.html)

## Sources for Each Notebook
The notebooks in this repository are inspired by and adapted from the following Pyomo tutorial videos.  
Each link corresponds to the concepts implemented in the notebook.  

### [Notebook 01: Linear Programming](01_Linear_Programming.ipynb):
- [4.1: Solving problems using Pyomo - simple example](https://youtu.be/0YzdcaxCc4c?si=HTDFNO58keMnax5p)
- [4.2: Solving problems using pyomo - simple example](https://youtu.be/Sf2raGjlJNg?si=7O0d0zVAdCrbk76-)

### [Notebook 02: Linear Programming (Battery Scheduling Problem)](02_Linear_Scheduling.ipynb):
- [5.1 Solving problems using Pyomo - less simple example](https://youtu.be/rU6sszNuaj8?si=51cvfmR0Uj4PMIHH)
- [5.2 Solving problems using Pyomo - less simple example](https://youtu.be/WNknYqjBPnw?si=tHOqvPl9M2VSdjv1)
- [5.3 Solving problems using Pyomo - less simple example](https://youtu.be/QbYd3DOf-T4?si=1w7NyNdykjaCZ67y)
- [5.4 Solving problems using Pyomo - less simple example](https://youtu.be/-AgN9PeDMmk?si=HVSqzzlExJ1x3jXC)
- [5.5 Solving problems using Pyomo - less simple example](https://youtu.be/kx7JqF_1js0?si=x8dUOXGBVxWlqrxt)

### [Notebook 03: Mixed-Integer Linear Programming (Battery Scheduling Problem)](03_Mixed_Integer_Linear_Programming.ipynb):
- [7.1: Integer programming example in Pyomo - problem statement](https://youtu.be/XmL6PSNOLC8?si=ux_KOHvIP5Y33vXW)
- [7.2: Integer programming example in Pyomo - implementation and solution](https://youtu.be/yejuQjXAuds?si=6XoDD0z0hkWl6_OZ)
- [7.3: Integer programming example in Pyomo - solver log](https://youtu.be/hSINXlDKvRw?si=zOAC5TsuDr6_a3Eg)

### [Notebook 04: Quadratic Programming](04_Quadratic_Programming.ipynb):
- [Overview of Quadratic Programming (QP)](https://youtu.be/GZb9647X8sg?si=s_lR1ugYpgMK1Abg)

### [Notebook 05: Non-Linear Programming](05_Non_Linear_Programming.ipynb):
- [Nonlinear Programming Optimization](https://gaurav-adarshi.medium.com/nonlinear-programming-optimization-df65f0576998)

### [Notebook 06: Mixed-Integer Non-Linear Programming](06_Mixed_Integer_Non_Linear_Programming.ipynb):
- [Nonlinear Programming Optimization](https://gaurav-adarshi.medium.com/nonlinear-programming-optimization-df65f0576998)