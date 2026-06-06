# 2D Electrostatic Modeling of MOSFET

Course project — Budapest University of Technology and Economics (BME).
Supervisor: Dr. József Pávó.

## Overview
A simplified 2D electrostatic model of a MOSFET in the OFF-state, used to
compute the parasitic (partial) capacitances between its electrodes. The
potential distribution is solved with the Finite Element Method (FEM) using
the MATLAB PDE Toolbox, and electrode surface charges are integrated to
extract the capacitance matrix.

## Methods
- **Model:** 2D vertical cross-section of the device; gate, source, drain,
  and bulk treated as electrodes, with the depletion region, SiO2, and Si3N4
  spacers as dielectrics (εr = 11.7 / 3.9 / 7.5).
- **Governing equation:** Laplace/Poisson equation (ρ = 0 in OFF-state),
  div(ε·grad U) = 0, with Dirichlet boundary conditions on the electrodes.
- **Capacitance extraction:** unit-voltage configuration (1 V on one
  electrode, others grounded); electrode charges Q computed by integrating
  −ε·∂U/∂n along the boundaries, then assembled into the partial
  capacitance matrix.
- **Tools:** MATLAB PDE Toolbox (GUI + command line).

## Key Result
Extracted drain-related capacitances, e.g. drain–bulk ≈ 1.12 fF (assuming
1 µm device width), consistent with the typical 1–5 fF junction-capacitance
range for micron-scale technologies.

## Contents
- `MOSFET_2D_Electrostatic_Model.pdf` — full project report (in Hungarian)
