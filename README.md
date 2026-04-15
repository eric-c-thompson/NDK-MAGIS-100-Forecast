# A MAGIS-100 Experimental Forecast for Momentum-Quadratic Dephasing

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/) [![DOI:10.5281/zenodo.19389059](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.19389059-blue.svg)](https://doi.org/10.5281/zenodo.19389059)

**Author:** Eric C. Thompson  
*Independent Researcher, Fulshear, Texas, USA*

[ORCID: 0009-0001-4127-1742](https://orcid.org/0009-0001-4127-1742) | Email: ethompson06@gmail.com

---

This repository contains the LaTeX source files, compiled PDF, figure assets, and supporting computational code for the technical note:

**"A MAGIS-100 Experimental Forecast for Momentum-Quadratic Dephasing: A Short Technical Note on Experimental Discriminants for a Parameter-Free Transport Prediction."**

This note translates the momentum-quadratic dephasing prediction of the Null-Directional Kinematics (NDK) framework into a concrete, experimentally oriented forecast for the 100-meter-scale MAGIS-100 atom interferometer. In the present formulation, the forecast is **closure-normalized**: the overall normalization is fixed by the primitive-cell sector of the theory through the action-scale closure rather than by an external fixed-cell ansatz. :contentReference[oaicite:0]{index=0}

## Purpose and Scope

The goal of this note is not to rederive the full transport framework, but to present a practical discrimination program for experiment. The central question is whether a residual contrast-loss component remains after ordinary technical channels are modeled and mitigated, and whether that residual follows the characteristic NDK transport scaling rather than standard pulse-infidelity, wavefront, inhomogeneity, or readout trends. :contentReference[oaicite:1]{index=1}

## Forecast Figures and Notebook Outputs

This repository includes code and figure assets for several complementary views of the closure-normalized forecast:

- **Main residual dephasing forecast** (`magis-focused_dephasing_forecast.png`)  
  A single-baseline 2D forecast showing the predicted residual dephasing as a function of LMT order $n$, with a baseline operating point at $T=9\,\mathrm{s}$ and $\Theta=400\,\mathrm{pK}$, together with a model-side transfer sensitivity band from sweeps in $\Theta$, $k_{\rm eff}$, and $w_{\mathrm{coh}}$.

- **Experimental transfer reach figure** (`magis-focused_dephasing_transfer_reach.png`)  
  A preparation-side reach map evaluated at fixed $T=9\,\mathrm{s}$ and $n=1000$, showing how the predicted residual grows with transverse coherence-support width $w_{\mathrm{coh}}$ across temperature families from $200$ to $600\,\mathrm{pK}$. This figure is intended to highlight where source-preparation changes provide the strongest experimental leverage.

- **Illustrative 3D surface**  
  A single-parameter-choice visualization of the joint $n$ and $T$ dependence of the closure-normalized residual law. This surface is included for intuition rather than as a sensitivity-band forecast.

- **Quick single-point calculator**  
  A direct numerical calculator for evaluating $D_{\mathrm{pred}}$ and the corresponding fractional visibility loss for a selected operating point.

## Supporting Code

The computational code in this repository reproduces the forecast figures and calculator outputs used in the note. In its current form, the notebook/codebase is organized around:

- a **main forecast generator** for the \(n\)-dependent closure-normalized residual law,
- a **transfer-reach plot** showing the preparation-side leverage of \(w_{\mathrm{coh}}\) and \(\Theta\),
- an **illustrative 3D surface** for the joint \(n\) and \(T\) scaling,
- and a **single-point calculator** for direct operating-point estimates.

These calculations implement the closure-normalized thermal forecast law used in the paper rather than the older fixed-cell external-normalization formulation. 

## The Experimental Discrimination Program

The note proposes a compact four-part program for isolating or falsifying the predicted transport signature:

1. **LMT Sweep (\(n^2\) scaling):**  
   At fixed preparation and fixed interrogation time, the residual dephasing exponent should scale quadratically with LMT order.

2. **Source-Preparation Sweep:**  
   At fixed \(n\) and \(T\), the residual should strengthen as pre-split coherence support is broadened and, under the thermal identification, as source temperature increases.

3. **Interrogation-Time Sweep (\(T\) scaling):**  
   At fixed preparation and fixed LMT order, the residual grows linearly with interrogation time.

4. **Pulse-Optimization Sweep:**  
   If an apparent \(n^2\) trend disappears under ordinary pulse optimization and technical mitigation, the transport interpretation is disfavored. :contentReference[oaicite:5]{index=5}

The residual law is expressed most generally as

$$
D_{\mathrm{pred}} \propto T\,n^2\,k_{\rm eff}^2\left(\frac{w_{\mathrm{coh}}}{\lambda_{\mathrm{coh},0}}\right)^2,
$$

and, under the thermal coherence identification used in the present forecast, as

$$
D_{\mathrm{pred}} \propto T\,n^2\,k_{\rm eff}^2\,w_{\mathrm{coh}}^2\,\Theta.
$$

This thermal form is the one implemented in the current plotting code and calculator. 

## Broader NDK Program Context

This forecast rests on the broader NDK program, including the directional transport framework, the reduced matter-wave dephasing law, and the primitive-cell closure linking the normalization of the emergent action scale to the same sector that governs the transport burden. For the upstream theoretical development, see:

- **The Core NDK Framework:** [10.5281/zenodo.18665370](https://doi.org/10.5281/zenodo.18665370)
- **The Transport Model & LMT Letter:** [10.5281/zenodo.19186680](https://doi.org/10.5281/zenodo.19186680)
- **Emergent Schrödinger Dynamics from Fisher Transport:** [10.5281/zenodo.19338222](https://doi.org/10.5281/zenodo.19338222)
- **Conditional Primitive-Cell Closure / Action-Scale Normalization:** [10.5281/zenodo.19375997](https://doi.org/10.5281/zenodo.19375997)
- **The NDK Master Action:** [10.5281/zenodo.19011014](https://doi.org/10.5281/zenodo.19011014)

## Compilation Instructions

The document is written in standard LaTeX. To compile the PDF locally:

```bash
pdflatex magis_forecast_note.tex
pdflatex magis_forecast_note.tex
