Suboptimal Travelling Salesman Problem (TSP) solver
===================================================
In pure Python.

This project provides a pure Python code for searching sub-optimal solutions to the TSP.
Additionally, demonstration scripts for visualization of results are provided.


The library does not requires any libraries, but demo scripts require:
- Numpy
- PIL (Python imaging library)
- Matplotlib

### Modules provided:
- **tsp_solver.greedy** : Basic greedy TSP solver in Python
- **tsp_solver.greedy_numpy** : Version that uses Numpy matrices, which reduces memory use, but performance is several percents lower
- **tsp_solver.demo** : Code for the demo applicaiton

### Scripts provided

- **demo_tsp** : Generates random TSP, solves it and visualises the result. Optionally, result can be saved to the numpy-format file.
- **tsp_numpy2svg** : Generates neat SVG image from the numpy file, generated by the **demo_tsp**.

Both applications support a variety of command-line keys, run them with --help option to see additional info.

 
Installation
------------
Install from PyPi:
```sh
 # pip install tsp_solver
```
or
```sh
 $ pip install --user tsp_solver
```
 
Manual installation:

```sh
 # python setup.py install
```

Usage 
-----

The library provides a greedy solver for the symmetric Travelling Salesman Problem (TSP).

Basic usage is the following:

```python
from tsp_solver.greedy import solve_tsp

#Prepare a left-triangular distance matrix for 3 nodes:
#Distance from 0 to 1 is 1.0
#                1 to 2 is 3.0
#                0 to 2 is 2.0
D = [[]],
     [ 1.0],
     [ 2.0, 3.0]]

path = solve_tsp( D )

will print [1,0,2], path with total length of 3.0 units
print path
```

