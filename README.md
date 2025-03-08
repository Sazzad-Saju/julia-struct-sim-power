# Simulation code for structural models, non-linear estimation, and RCT power analysis in Julia

This repository demonstrates three key statistical simulation concepts in Julia:

- **Structural Model Simulation:**  
  Generate synthetic data using a simple structural model where the outcome is a linear combination of a baseline intercept, a treatment effect (random Boolean), a continuous predictor, and random error.

- **Non-Linear Estimation:**  
  Fit a non-linear model of the form  
  <strong> Y=a+b×exp(c×X) </strong> <br>
  using the LsqFit package to estimate the parameters \([a, b, c]\).

- **RCT Power Calculation:**  
  Simulate randomized controlled trials to calculate statistical power by comparing means between treatment and control groups and determining the proportion of trials where the effect is statistically significant.

The code below provides a complete workflow to:
- Generate synthetic data,
- Fit a non-linear model to that data,
- And perform a simulation-based power analysis for an RCT.


## How to Run This Code on Windows

This code cannot be executed using online tools (e.g., https://www.tutorialspoint.com/execute_julia_online.php) because it requires local installation of several packages. Follow these steps on your PC:

1. **Install VS Code:** Download and install Visual Studio Code.
2. **Install Julia:** Download Julia from [julialang.org/downloads](https://julialang.org/downloads/) and install it.
3. **Configure Environment Variable:**  
   Add `C:\Users\sazzad\AppData\Local\Programs\Julia-1.11.3\bin` to your system's PATH (via System Variables > Path).
4. **Install Julia Extension in VS Code.**
5. **Open the Terminal:**  
   Open a command prompt or terminal in the repository folder.
6. **Install Required Packages:**  
   Open the Julia REPL by typing `julia` in your terminal and run:
   ```julia
   import Pkg
   Pkg.add("Random")
   Pkg.add("Distributions")
   Pkg.add("LsqFit")
   Pkg.add("Statistics")

7. Run the Code:
   
```

julia test.jl

```

You should see output similar to:

```

Estimated parameters (a, b, c): [-42.140736147204, 44.149488196903015, 0.010340370142542665]
Estimated power for the RCT with n=200: 1.0

```
