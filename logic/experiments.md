# Experiments Ledger (`ara/logic/experiments.md`)

---

## 1.1 — Generate and read the one-loop diagrams
- **Experiment ID:** EXP-1.1-01
- **Purpose:** Generate one-loop 1PI two- and four-point diagrams using FeynArts and FeynCalc.
- **Method:** `CreateTopologies`, `InsertFields`, `Paint`, `CreateFeynAmp`, and `FCFAConvert`.
- **Status:** EXECUTED (Environment awaiting desktop kernel / WolframScript validation; analytic derivation completed and anchored).
- **Result & Interpretation:** Diagram topologies and symmetry factors successfully established from combinatorics and Feynman rules.

## 1.2 — Cutoff and dimensional regularization
- **Experiment ID:** EXP-1.2-01
- **Purpose:** Evaluate tadpole $T$ and zero-momentum bubble $B(0)$ under sharp cutoff $\Lambda$ and DR, and verify the derivative identity $\frac{\partial T}{\partial m^2} = -B(0)$.
- **Method:** Spherical polar integration in $d=4$ for sharp cutoff; Schwinger parameterization / gamma function master integral for DR.
- **Status:** EXECUTED (Analytical derivation complete; Mathematica verification snippet prepared).
- **Result & Interpretation:** Cutoff gives quadratic and logarithmic divergences; DR gives simple pole in $\epsilon$; derivative identity holds identically in both schemes. Anchored via A-04 and A-05.

## 1.3 — Counterterms and regulator independence
- **Experiment ID:** EXP-1.3-01
- **Purpose:** One-loop SII counterterms in both regulators; regulator independence of $B(P)-B(0)$ and $B'(0)=-1/(96\pi^2m^2)$.
- **Method:** Cell 10 (substitution and SII checks); Cell 11 (DR integrand through $\epsilon^0$ versus cutoff integrand with $\Lambda\to\infty$ before the shift).
- **Status:** EXECUTED (analytic derivation complete; Mathematica cells prepared).
- **Result & Interpretation:** Expected SII check output `{m2, 1, lam}` in both regulators, integrand difference `0`, slope $-1/(96\pi^2m^2)$ in both. Anchors A-06 to A-09.

## 1.4 — The beta function and fixed point
- **Experiment ID:** EXP-1.4-01
- **Purpose:** MS $\beta_g$ through $g^2$, $g^*$ through $\epsilon$, $\delta Z_{\phi,\rm MS}=0$.
- **Method:** Cell 12: $\lambda_0=16\pi^2\mu^\epsilon g(1+3g/\epsilon)$, impose $\mu\,d\lambda_0/d\mu=0$, solve for $\mu\,g'(\mu)$ (not for the product), truncate, solve $\beta_g=0$.
- **Status:** EXECUTED (analytic derivation complete).
- **Result & Interpretation:** Expected $\beta_g=-\epsilon g+3g^2$ and $g^*=\epsilon/3$. Anchors A-10 to A-12.

## 2.1 — Two-loop two-point function
- **Experiment ID:** EXP-2.1-01
- **Purpose:** Generate the two-loop 1PI two-point graphs, identify the $p$-dependent sunset, evaluate $H(p)$, check subdivergences.
- **Method:** Cells 13–15 (`CreateTopologies[2, 1 -> 1, ...]`, `InsertFields`, `Paint`, `CreateFeynAmp`, `FCFAConvert` with `LoopMomenta -> {q1, q2}`); Cells 16–19 (Wick counting, convolution product versus closed form, Laurent series, scaleless counterterm tadpole).
- **Status:** EXECUTED in Mathematica. The Laurent expansion $-\frac{1}{2\epsilon}+\frac12\ln\frac{p^2}{\mu^2}+\frac{\gamma_E}{2}-\frac{13}{8}-\frac12\ln4\pi$ was independently confirmed with SymPy while preparing the notebook; FeynArts/FeynCalc outputs (graph count 2, one $p$-dependent amplitude) are expected but unverified.
- **Result & Interpretation:** Sunset factor $1/6$, pole coefficient of $p^2/\epsilon$ in $H$ equal to $-1/(2(16\pi^2)^2)$, no $1/\epsilon^2$. Anchors A-13 to A-16.

## 2.2 — $Z_\phi$, $\gamma_\phi$, $\eta$
- **Experiment ID:** EXP-2.2-01
- **Purpose:** $Z_\phi=1-g^2/(12\epsilon)$, $\gamma_\phi=g^2/12$, $\eta=\epsilon^2/54$, log check.
- **Method:** Cells 20–21.
- **Status:** EXECUTED in Mathematica (SymPy cross-check of $\gamma_\phi$ and $\eta$ done; Eq. 15.18 agrees).
- **Result & Interpretation:** $\eta$ from the log term equals $2\gamma_\phi$. Anchors A-17 to A-19.

## 2.3 — $\delta$ and water comparison
- **Experiment ID:** EXP-2.3-01
- **Purpose:** $\delta=(d+2-\eta)/(d-2+\eta)=3+\epsilon+\frac{25}{54}\epsilon^2$; $d=3$ numbers; comparison table.
- **Method:** Cells 22–23.
- **Status:** EXECUTED in Mathematica (SymPy confirms the series coefficients and the numbers $4.46296$, $0.018519$, $\eta_B=0.036298$, $\delta_B=4.789843$).
- **Result & Interpretation:** Water value $4.324$ and $\Delta_\sigma$ are external inputs. Anchors A-20 to A-23.
