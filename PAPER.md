# PAPER.md: Scalar Field Renormalization

## Overview
This project investigates renormalization in real scalar $\phi^4$ theory and its application to critical phenomena, bridging quantum field theory calculations (using FeynArts and FeynCalc) with statistical mechanics critical exponents of water.

## Part 1: Warm up with one loop and two regulators
- **1.1 One-loop diagrams:** Generate 1PI two-point and four-point diagrams using real-scalar $\Phi_4$ model.
- **1.2 Cutoff and dimensional regularization:** Evaluate tadpole $T$ and bubble $B(0)$ integrals, expanding through $\Lambda^{-2}$ and $\varepsilon$ poles.
- **1.3 Counterterms and regulator independence:** Derive $\delta Z_\phi$, $\delta m^2$, and $\delta \lambda$; verify $B(P) - B(0)$ agreement across regulators.
- **1.4 The beta function and fixed point:** Derive minimal-subtraction $\beta_g$, field counterterm, and fixed point $\varepsilon$.

## Part 2: Critical exponents and water
- **2.1 The two-loop two-point function:** Generate two-loop 1PI diagrams, evaluate sunset integral $H(p)$, and analyze subdivergences.
- **2.2 Field renormalization and anomalous dimension:** Extract $Z_\phi$, $\gamma_\phi(g)$, and $\eta = 2\gamma_\phi(g_*)$.
- **2.3 Scaling and comparison with water:** Introduce external field $h$, derive scaling relation $\delta = \frac{d+2-\eta}{d-2+\eta}$, and compare $d=3$ predictions with water critical isotherm data and 3D Ising bootstrap benchmarks.
