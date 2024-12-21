# Integrating Symbolic Regression with Physics-Informed Neural Networks for Simulating Nonlinear Wave Dynamics in Arterial Blood Flow

## Overview

This repository hosts the code and data associated with our research publication titled "Integrating Symbolic Regression with Physics-Informed Neural Networks for Simulating Nonlinear Wave Dynamics in Arterial Blood Flow" in a Q1-ranked SCIE international journal named **Physics of Fluids** (Vol 36, Issue 12, page 121924), authored by **Satyasaran Changdar, Bivas Bhaumik, Nabanita Sadhukhan, Sumit Pandey, Sabyasachi Mukhopadhyay, Soumen De, and Serafim Bakalis**. The study investigates a hybrid framework that integrates machine learning techniques and symbolic regression to model and analyze nonlinear wave propagation in arterial blood flow.

---

## Abstract

This research introduces a mathematical and computational framework for studying the nonlinear propagation of waves in viscoelastic arterial blood flow, under assumptions of long wavelength and large Reynolds numbers. A **fifth-order nonlinear evolutionary equation**, derived through reductive perturbation theory, is used to model wave behavior in a viscoelastic tube, accounting for the tube wall's bending.

The following approaches were implemented:

1. **Physics-Informed Neural Networks (PINNs):**
   - Solved the governing PDEs across the spatial-temporal domain [-1, 1]x [0, 2].
   - Bayesian hyperparameter optimization was employed for improved model performance.
   - Achieved mean absolute residue error of O(10^{-3}).
<img src="https://github.com/satyasaran/FifthOrderPDEPinnSymReg/blob/main/pinn.png" hight= "300" width="1000"/>

2. **Machine Learning Integration:**
   - Solutions under three distinct initial conditions were merged using a random forest algorithm, achieving **99% accuracy** on the testing dataset.
   - The results were benchmarked against an artificial neural network (ANN).

3. **Symbolic Regression:**
   - Analytical solutions were derived using genetic programming for symbolic regression, resulting in interpretable models with a mean square error of \(O(10^{-3})\).
<img src="https://github.com/satyasaran/FifthOrderPDEPinnSymReg/blob/main/Highlight%20Image.jpeg" hight= "300" width="1000"/>
These methods offer new insights into modeling cardiovascular parameters and demonstrate the potential of integrating machine learning with symbolic regression for solving complex scientific problems.

---

## Repository Structure

```plaintext
.
├── Cos/                       # Code and Results from cosine-based initial conditions
├── Exp/                       # Code and Results from exponential-based initial conditions
├── MLandSymReg/               # Code and results from Machine learning and symbolic regression scripts
├── combined_data_solution.csv # Combined dataset of solutions for ML analysis
├── README.md                  # Project documentation
