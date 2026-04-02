# A MAGIS-100 Experimental Forecast for Momentum-Quadratic Dephasing

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

This repository contains the LaTeX source files, compiled PDF, and figure assets for the technical note: **"A MAGIS-100 Experimental Forecast for Momentum-Quadratic Dephasing: A Short Technical Note on Experimental Discriminants for the Fixed-Cell Transport Signature."**

This note translates the momentum-quadratic dephasing prediction of the Null-Directional Kinematics (NDK) fixed-cell transport model into a concrete, experimentally oriented forecast for the 100-meter-scale MAGIS-100 atom interferometer. 

## 🎯 Purpose and Scope
The goal of this note is not to rederive the underlying transport geometry, but to provide experimentalists with a practical discrimination program. It outlines exactly how to separate standard technical contrast loss (e.g., pulse inefficiency, wavefront effects, laser phase noise) from the predicted intrinsic, geometric transport burden of the informational vacuum.

## 📊 The 3D Forecast Plot
Included in this repository is the code/asset for the 3D dephasing forecast plot (`magis-focused_dephasing_forecast.png`). This visualization illustrates the joint scaling law of the predicted geometric drag, highlighting the parametric separation between current $n \sim 10^2$ platforms and the $n \sim 10^3$ MAGIS-100 regime. It explicitly maps how the source temperature ($\Theta$) acts as a vertical rescaling knob on the log-log surface without altering the fundamental $n^2$ shape.

## 🎛️ The Experimental Discrimination Program
The central claim is a residual contrast-loss law that survives ordinary technical mitigation. The note proposes four concrete sweeps to isolate or falsify this signature:

1. **LMT Sweep ($n^2$ scaling):** At fixed time and temperature, the residual dephasing exponent must scale quadratically with the large-momentum-transfer order ($D_{\mathrm{pred}} \propto n^2$).
2. **Source-Preparation Sweep (The $\Theta$ knob):** At fixed LMT and time, a hotter source corresponds to a smaller pre-split coherence cell, resulting in a linear strengthening of the quadratic coefficient ($D_{\mathrm{pred}} \propto \Theta$).
3. **Interrogation-Time Sweep ($T$ scaling):** At fixed preparation and LMT, the burden grows linearly with the time the wavepacket spends in a split state ($D_{\mathrm{pred}} \propto T$).
4. **Pulse-Optimization Sweep:** If the $n^2$ trend disappears after standard pulse engineering and laser-noise reduction, the NDK signature is falsified.

The combined residual scaling law is therefore:
$$D_{\mathrm{pred}} \propto T\,n^2\,k_{\mathrm{eff}}^2\,\Theta$$

---

## 🛠️ Compilation Instructions

The document is written in standard LaTeX. To compile the PDF locally:
```bash
pdflatex magis_forecast_note.tex
pdflatex magis_forecast_note.tex
