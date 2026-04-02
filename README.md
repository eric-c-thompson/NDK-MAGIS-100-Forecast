# Null-Directional Kinematics (NDK): Emergent Quantum Dynamics & LMT Interferometry

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

This repository contains the LaTeX source files and compiled PDFs for two papers in the **Null-Directional Kinematics (NDK)** research program. These papers bridge the foundational geometry of the NDK master action to emergent Schrödinger dynamics, and explicitly map that transport geometry to a falsifiable prediction for Large-Momentum-Transfer (LMT) atom interferometry.

## 📄 The Papers

### 1. Emergent Schrödinger Dynamics from Fisher Transport on the Null Sphere Bundle
**Subtitle:** *Angular Reduction, Reversible Transport Completion, and the Quantum Action Scale* **DOI:** [10.5281/zenodo.19338222](https://doi.org/10.5281/zenodo.19338222)

**Overview:** This paper rigorously derives the structure of quantum mechanics from the real, classical-looking Fisher transport sector of the NDK master action. It demonstrates that the complex Schrödinger wavefunction is not a fundamental postulate, but emerges as the necessary, compact packaging of a canonically conjugate pair $(\rho, S)$ forced by the requirement of reversible probability transport. 

**Key Results:**
* **Emergent $\hbar$:** Proves that the quantum action scale ($\hbar_{\mathrm{eff}}$) is not an arbitrary constant, but an emergent combination of the substrate's spacetime Fisher cost and angular stiffness.
* **Origin of Mass:** Derives inertial mass ($m_{\mathrm{eff}}$) strictly from the geometric drag of the vacuum resisting spatial transport.
* **Weak Equivalence Principle:** Matches the canonically normalized matter envelope to the Schrödinger-Poisson system to prove $m_{\mathrm{grav}} = m_{\mathrm{inert}}$.

### 2. Macroscopic Dephasing in LMT Atom Interferometry from a Fixed-Cell Transport Model
**Subtitle:** *A Short Letter on the NDK Momentum-Quadratic Contrast Floor* **DOI:** [10.5281/zenodo.19074887](https://doi.org/10.5281/zenodo.19074887)

**Overview:** This Letter acts as the phenomenological bridge between the foundational NDK transport law and upcoming 100-meter-scale atom interferometers (such as MAGIS-100). It establishes a fixed-cell transport model to predict a macroscopic geometric dephasing floor.

**Key Results:**
* **Falsifiable Scaling Law:** Predicts a residual geometric contrast loss whose leading dependence is strictly quadratic in LMT order at fixed interrogation time: $D_{\mathrm{pred}} \propto T\,n^2 k_{\mathrm{eff}}^2$.
* **Thermal Ratio Test:** Shows that under a thermal identification of the pre-split coherence cell, the quadratic dephasing coefficient must scale linearly with source temperature.
* **Regime Separation:** Demonstrates that current $n \sim 10^2$ instruments remain parametrically below this dephasing window, while $n \sim 10^3$ architectures act as the critical threshold to trigger the NDK transport penalty.

---

## 🛠️ Compilation Instructions

The documents are written in standard LaTeX and use standard packages (`amsmath`, `amssymb`, `geometry`, `hyperref`, `cleveref`). 

To compile the PDFs locally:
```bash
pdflatex emergent_schrodinger_dynamics.tex
pdflatex lmt_dephasing_prediction.tex
