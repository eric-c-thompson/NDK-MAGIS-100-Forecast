# A MAGIS-100 Experimental Forecast for Momentum-Quadratic Dephasing

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/) [![DOI:10.5281/zenodo.19389059](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.19389059-blue.svg)](https://doi.org/10.5281/zenodo.19389059)

**Author:** Eric C. Thompson
*Independent Researcher, Fulshear, Texas, USA*

[ORCID: 0009-0001-4127-1742](https://orcid.org/0009-0001-4127-1742) | Email: ethompson06@gmail.com

---

This repository contains the LaTeX source files, compiled PDF, figure assets, and supporting computational code for the technical note:

**"A MAGIS-100 Experimental Forecast for Momentum-Quadratic Dephasing: A Short Technical Note on Experimental Discriminants for the Fixed-Cell Transport Signature."**

This note translates the momentum-quadratic dephasing prediction of the Null-Directional Kinematics (NDK) fixed-cell transport model into a concrete, experimentally oriented forecast for the 100-meter-scale MAGIS-100 atom interferometer.

## Purpose and Scope

The goal of this note is not to rederive the underlying transport geometry, but to provide experimentalists with a practical discrimination program. It outlines exactly how to separate standard technical contrast loss (e.g., pulse inefficiency, wavefront effects, laser phase noise) from the predicted intrinsic, geometric transport burden of the informational vacuum.

## The 3D Forecast Plot

Included in this repository is the code and asset for the 3D dephasing forecast plot (`magis-focused_dephasing_forecast.png`). This visualization illustrates the joint scaling law of the predicted geometric drag, highlighting the parametric separation between current $n \sim 10^2$ platforms and the $n \sim 10^3$ MAGIS-100 regime. It explicitly maps how the source temperature acts as a vertical rescaling knob on the log-log surface without altering the fundamental $n^2$ shape.

## Supporting Code

The `code/` directory contains Python scripts used to generate the figures and verify the numerical predictions in the note:

- **`dephasing_forecast_3d.py`** — Generates the 3D dephasing forecast surface plot showing the joint ($n$, $T$, $\Theta$) scaling law.
- **`casimir_sign.py`** — Computes the one-loop Casimir remainder of the NDK mode tower, verifying the EFT-defined compact vacuum energy and its sign structure.
- **`dark_energy_ansatz.py`** — Explores ansatz combinations for the dark energy magnitude using the NDK strain formula, scanning over mass scales and strain values.

All scripts require Python 3 with NumPy and SciPy.

## The Experimental Discrimination Program

The central claim is a residual contrast-loss law that survives ordinary technical mitigation. The note proposes four concrete sweeps to isolate or falsify this signature:

1. **LMT Sweep ($n^2$ scaling):** At fixed time and temperature, the residual dephasing exponent must scale quadratically with the large-momentum-transfer order.
2. **Source-Preparation Sweep (the $\Theta$ knob):** At fixed LMT and time, a hotter source corresponds to a smaller pre-split coherence cell, resulting in a linear strengthening of the quadratic coefficient.
3. **Interrogation-Time Sweep ($T$ scaling):** At fixed preparation and LMT, the burden grows linearly with the time the wavepacket spends in a split state.
4. **Pulse-Optimization Sweep:** If the $n^2$ trend disappears after standard pulse engineering and laser-noise reduction, the NDK signature is falsified.

The combined residual scaling law is therefore:

$$D_{\mathrm{pred}} \propto T\,n^2\,k_{\mathrm{eff}}^2\,\Theta$$

## Broader NDK Program Context

This experimental forecast relies on the theoretical foundation, transport scaling, and primitive-cell closures developed in the broader NDK research program. For the mathematical derivations and cosmological calibrations that inform this forecast, see the upstream Zenodo records:

- **The Transport Model & LMT Letter:** [10.5281/zenodo.19186680](https://doi.org/10.5281/zenodo.19186680)
- **Emergent Schrödinger Dynamics from Fisher Transport:** [10.5281/zenodo.19338222](https://doi.org/10.5281/zenodo.19338222)
- **Conditional Primitive-Cell Closure ($G$ and $\hbar$):** [10.5281/zenodo.19375997](https://doi.org/10.5281/zenodo.19375997)
- **The NDK Master Action:** [10.5281/zenodo.19011014](https://doi.org/10.5281/zenodo.19011014)

## Compilation Instructions

The document is written in standard LaTeX. To compile the PDF locally:

```bash
pdflatex magis_forecast_note.tex
pdflatex magis_forecast_note.tex
