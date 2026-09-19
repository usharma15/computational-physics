# Computational Physics

Python notebooks by **Udayan Sharma**, developed for PHYS 580 computational physics coursework in Spring 2026. The collection explores how numerical methods connect physical models to trajectories, fields, statistical observables, and quantum states.

The 21 notebooks are organized by subject and named for their contents. They retain their original code comments, acknowledgments, and saved outputs; each has a short descriptive introduction.

## Explore the notebooks

### Numerical Methods

| Notebook | Topics |
| --- | --- |
| [Radioactive Decay Integrators and Python Basics](radioactive-decay-integrators-and-python-basics.ipynb) | Plotting and animation, Euler stability and error, and comparisons with second- and fourth-order Runge–Kutta methods. |
| [Decay Chains, Drag, and Pendulum Experiments](decay-chains-drag-and-pendulum-experiments.ipynb) | Coupled nuclear decay, bicycle terminal speed, atmospheric projectile motion, and driven-pendulum Poincaré samples. |

### Classical Mechanics

| Notebook | Topics |
| --- | --- |
| [Projectile Motion with Atmospheric Drag](projectile-motion-with-atmospheric-drag.ipynb) | Euler trajectories for vacuum and drag models, altitude-dependent air density, and optimal launch angles. |
| [Pendulum Integrators, Damping, and Nonlinearity](pendulum-integrators-damping-and-nonlinearity.ipynb) | Euler, Euler–Cromer, and midpoint Runge–Kutta integration for harmonic, driven, damped, and nonlinear pendulums. |

### Nonlinear Dynamics

| Notebook | Topics |
| --- | --- |
| [Driven Pendulum Chaos and Poincaré Sections](driven-pendulum-chaos-and-poincare-sections.ipynb) | Periodic and chaotic regimes, sensitivity to initial conditions, and the effects of sampling phase and frequency. |
| [Nonlinear Oscillators, Lyapunov Exponents, and Bifurcations](nonlinear-oscillators-lyapunov-exponents-and-bifurcations.ipynb) | Damping scans, amplitude-dependent oscillator periods, trajectory separation, and period-doubling bifurcations. |
| [Hyperion Chaotic Rotation and Lyapunov Analysis](hyperion-chaotic-rotation-and-lyapunov-analysis.ipynb) | Coupled orbital and rotational dynamics of a dumbbell model of Hyperion, with angular separation and Lyapunov fits. |

### Orbital Mechanics

| Notebook | Topics |
| --- | --- |
| [Kepler Orbits, Comets, and Three-Body Perturbations](kepler-orbits-comets-and-three-body-perturbations.ipynb) | Bound and unbound orbits, comet periods, and Earth–Jupiter perturbations with fixed and mobile Sun models. |
| [Pendulum Quadrature, Mercury Precession, and N-Body Orbits](pendulum-quadrature-mercury-precession-and-n-body-orbits.ipynb) | Numerical quadrature of the pendulum period, orbital integration error, Mercury perihelion precession, and Earth–Moon dynamics. |
| [Mercury Perihelion Precession with Baseline Correction](mercury-perihelion-precession-baseline-correction.ipynb) | A standalone Mercury precession study that subtracts numerical baseline drift and extrapolates a modified-force parameter. |

### Electromagnetism

| Notebook | Topics |
| --- | --- |
| [Laplace and Poisson Relaxation Solvers](laplace-and-poisson-relaxation-solvers.ipynb) | Capacitor potentials and electric fields using Jacobi and Gauss–Seidel relaxation, plus localized charge sources. |
| [SOR Electrostatics and Biot–Savart Quadrature](sor-electrostatics-and-biot-savart-quadrature.ipynb) | Jacobi versus successive over-relaxation scaling, a point charge in a grounded box, and straight-wire magnetic-field integration. |
| [Magnetic Fields of Current Loops and Solenoids](magnetic-fields-of-current-loops-and-solenoids.ipynb) | Numerical Biot–Savart fields for paired current loops and helical coils, compared with analytical on-axis results. |

### Stochastic Processes

| Notebook | Topics |
| --- | --- |
| [Monte Carlo Integration and Random Walks](monte-carlo-integration-and-random-walks.ipynb) | Monte Carlo quadrature and error scaling, continuous two-dimensional random walks, and self-avoiding walks. |
| [Diffusion, Entropy, Escape, and Percolation Fractals](diffusion-entropy-escape-and-percolation-fractals.ipynb) | Three-dimensional diffusion, self-avoiding walk scaling, mixing entropy, escape through a hole, and spanning-cluster fractal dimension. |

### Statistical Mechanics

| Notebook | Topics |
| --- | --- |
| [Percolation Finite-Size Scaling and Critical Exponents](percolation-finite-size-scaling-and-critical-exponents.ipynb) | Cluster labeling, order parameter and susceptibility measurements, and estimates of beta, gamma, and nu near the percolation threshold. |
| [Ising Model: Metropolis Equilibration and Phase Transition](ising-model-metropolis-equilibration-and-phase-transition.ipynb) | Two-dimensional Ising simulations across temperature and external field, transient removal, and magnetization and energy measurements. |
| [Ising Critical Scaling and Maxwell Gas Statistics](ising-critical-scaling-and-maxwell-gas-statistics.ipynb) | Ising magnetization fits, specific heat, susceptibility scaling collapse, and a Lennard–Jones gas speed distribution compared with the two-dimensional Maxwell law. |

### Molecular Dynamics

| Notebook | Topics |
| --- | --- |
| [Lennard–Jones Dynamics, Heating, and Melting](lennard-jones-dynamics-heating-and-melting.ipynb) | Periodic boundaries and Verlet integration, energy and temperature tracking, particle displacement, staged heating, and comparisons between initial conditions. |

### Quantum Mechanics

| Notebook | Topics |
| --- | --- |
| [Quantum Bound States: Shooting, Matrix, and Variational Methods](quantum-bound-states-shooting-matrix-and-variational-methods.ipynb) | Square-well eigenstates with a central barrier, plus Lennard–Jones bound states from finite-difference diagonalization and stochastic variation. |
| [Finite-Well Tunneling and Variational Monte Carlo](finite-well-tunneling-and-variational-monte-carlo.ipynb) | Finite-well decay lengths, variational Monte Carlo for a quartic potential, and matching-method eigenstates of coupled wells. |

## Running

Open an individual `.ipynb` file on GitHub to browse its saved results, or open it in Google Colab. To work locally with Python 3:

```bash
python -m pip install -r requirements.txt
python -m jupyterlab
```

NumPy 2 or later is needed by notebooks using `numpy.trapezoid`. SciPy and mpmath support selected quantum and quadrature calculations. Most notebooks use NumPy and Matplotlib.

### Execution notes

- These are coursework notebooks containing independent experiments and, in some cases, abbreviated snippet cells. Read a cell before running it; some reuse names or require the preceding full experiment.
- Several notebooks request parameters with `input()`. Large Monte Carlo, molecular-dynamics, eigenvalue, and orbital sweeps can take substantial time.
- The introductory Python notebook reads `/number.txt` for one file-summing exercise. That data file was not included in the Colab notebook collection; provide a whitespace-separated integer file and adjust the path, or skip that cell.
- The introductory notebook requests Matplotlib's `TkAgg` backend. For a headless environment or Colab, select an inline backend or remove that backend selection before running those cells.
- Some notebooks save plots to local paths. Adjust output paths for your environment.
- Saved outputs are from the original notebooks, not a fresh execution of this repository. All code cells were checked for Python syntax during import; numerical results and full execution have not been independently revalidated.

## Source and import notes

The collection contains all 21 notebooks owned by this account in its Colab Notebooks folder: 13 labs, 7 homework notebooks, and a standalone Mercury-precession notebook. Shared lecture notebooks in the recent-files history are not included.

See [the source index](SOURCE_INDEX.md) for the original-to-descriptive filename mapping. The import adds a title and description to each notebook and corrects one duplicated semicolon in the Ising specific-heat snippets cell. Original source comments, including attribution and AI-use acknowledgments, and saved outputs are preserved.
