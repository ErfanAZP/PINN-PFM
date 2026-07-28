# PINN-PFM: Physics-Informed Neural Networks for Phase-Field Fracture

An energy-based (deep energy method) physics-informed neural network framework for
phase-field modeling of fracture, with stochastic minibatch integration of the
energy functional. Extension to hydrogen-assisted fracture also will be included in the repo.

The network is trained by directly minimizing the discretized potential energy of 
the body, aligned with DEM formulation of phase-field fracture. 

The energy integral is estimated from random minibatches of the integration points; 
ADAM training cost would be reduced.
Boundary conditions are imposed exactly through the network ansatz.

This is an ongoing project aimed at data-efficient, mesh-free
alternatives to conventional phase-field fracture modeling. f

Benchmarks are provided as a self-contained notebooks

## Requirements

- Python 3.x
- PyTorch
- NumPy, SciPy, pandas, matplotlib

## Running

Each notebook runs top to bottom and produced the fracture phase-field contour plots,
force-displacement diagrams, and energy loss plot per iteration. 

Note that the stochastic minibatch fraction is set via `batch_frac` variable; `batch_frac = 1` recovers full-batch training.

The notebooks run without modification in Kaggle platform.
