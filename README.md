# toy_code

### 1. Gaussian Mixture Model

#### Files
* ```GMM_EM.m```: expectation maximization for Gaussian mixture model.
* ```GMM_VI.m```: variational inference for Gaussian mixture model.
* ```GMM_MCMC.m```: Gibbs sampling for Gaussian mixture model.
* ```data.mat```: input sample.

### 2. Monte Carlo Solver

#### Files

* ```Solver_MonteCarlo.cpp```: Monte Carlo solution of integral equations in the form:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![equation](http://latex.codecogs.com/gif.latex?%5Cinline%20%5Cdpi%7B100%7D%20%5CLARGE%20I%3D%5Cint_%7Bx_1%7D%5E%7Bx_2%7D%5Cint_%7By_1%7D%5E%7By_2%7D%5Cint_%7Bz_1%7D%5E%7Bz_2%7Dx%5E%7Bx_0%7Dy%5E%7By_0%7D&plus;z_0%20e%5E%7B-z%7Ddxdydz)

#### Run

* For example: x0 = 2, x1 = 0, x2 = 2, y0 = 4, y1 = -1, y2 = 1, z0 = 3, z1 = 1, z2 = 1.5.

```
$ g++ -o mc.o Solver_MonteCarlo.cpp 
$ ./mc.o 1000000 2 0 2 4 -1 1 3 1 1.5
```

### 3. Newton Solver

#### Files

* ```Solver_Newton.cpp```: Newton solver of t, s.t. f(t) = val, where f(t) is in the form:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![equation](http://latex.codecogs.com/gif.latex?%5Cinline%20%5Cdpi%7B100%7D%20%5CLARGE%20f%28t%29%3Dw_1%20e%5E%7B-w_2t%7D%5Ccos%20%28w_3t%29%5Ctextup%7B%7D)

#### Run

* For example: w1 = 9, w2 = 1, w3 = 2, val = 3. 

```
$ g++ -o newton.o Solver_Newton.cpp 
$ ./newton.o  9 1 2 3
```

### 4. Strassen Solver Solver

#### Files

* ```Solver_Strassen.cpp```: Strassen solver of matrix multiplication C = A * B.
* ```a.txt```: contains matrix A.
* ```b.txt```: contains matrix B.

#### Run

```
$ g++ -o strassen.o Solver_Strassen.cpp 
$ ./strassen.o 
```

### 5. Partial Diffusion Equation

#### Files

* ```Solver_PDE_string.cpp```:  solve partial differential equation for a vibrating string.
* ```Solver_PDE_heat.cpp```: solve partial differential equation for a heat.

#### Run

```
$ g++ -o pde_string.o Solver_PDE_string.cpp 
$ ./pde_string.o 
$ g++ -o pde_heat.o Solver_PDE_heat.cpp 
$ ./pde_heat.o 
```


