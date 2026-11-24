# Experiments Ledger (`ara/logic/experiments.md`)

---

## 1.1 — Generate and read the one-loop diagrams
- **Experiment ID:** EXP-1.1-01
- **Purpose:** Generate one-loop 1PI two- and four-point diagrams using FeynArts and FeynCalc.
- **Method:** `CreateTopologies`, `InsertFields`, `Paint`, `CreateFeynAmp`, and `FCFAConvert`.
- **Status:** NOT EXECUTED (Environment awaiting desktop kernel / WolframScript validation; analytic derivation completed and anchored).
- **Result & Interpretation:** Diagram topologies and symmetry factors successfully established from combinatorics and Feynman rules.

## 1.2 — Cutoff and dimensional regularization
- **Experiment ID:** EXP-1.2-01
- **Purpose:** Evaluate tadpole $T$ and zero-momentum bubble $B(0)$ under sharp cutoff $\Lambda$ and DR, and verify the derivative identity $\frac{\partial T}{\partial m^2} = -B(0)$.
- **Method:** Spherical polar integration in $d=4$ for sharp cutoff; Schwinger parameterization / gamma function master integral for DR.
- **Status:** NOT EXECUTED (Analytical derivation complete; Mathematica verification snippet prepared).
- **Result & Interpretation:** Cutoff gives quadratic and logarithmic divergences; DR gives simple pole in $\epsilon$; derivative identity holds identically in both schemes. Anchored via A-04 and A-05.

## 1.3 — Counterterms and regulator independence
- **Experiment ID:** EXP-1.3-01
- **Purpose:** Compute the one-loop SII counterterms ($\delta Z_\phi$, $\delta m^2$, $\delta\lambda$) in sharp-cutoff and DR schemes, verify the three SII normalization conditions, and confirm regulator independence of $B(P) - B(0)$ and its slope $B'(0) = -1/(96\pi^2 m^2)$.
- **Method:** Symbolic counterterm substitution in Cell 10; Feynman parametrization (Eq. 13.20) in DR ($\epsilon \to 0$) vs. convergent difference ($\Lambda \to \infty$ before shifting loop momentum) in Cell 11.
- **Status:** NOT EXECUTED (Analytical derivation complete; Mathematica verification cells 10–11 prepared in `QFT_Midterm_Final_v6.nb`).
- **Result & Interpretation:** Both regulators satisfy the SII conditions identically, yield the same finite integrand $-\frac{1}{16\pi^2}\ln(1 + x(1-x)P^2/m^2)$ for $B(P)-B(0)$, and reproduce $B'(0) = -1/(96\pi^2 m^2)$. Anchored via A-06 through A-09.

## 1.4 — The beta function and fixed point
- **Experiment ID:** EXP-1.4-01
- **Purpose:** Derive the one-loop MS beta function $\beta_g = -\epsilon g + 3g^2 + \mathcal{O}(g^3)$ and the Wilson–Fisher fixed point $g^* = \epsilon/3 + \mathcal{O}(\epsilon^2)$ from the DR pole counterterms, and verify $\delta Z_{\phi,\text{MS}} = 0$.
- **Method:** Construct $\lambda_0 = 16\pi^2\mu^\epsilon(g + 3g^2/\epsilon)$, solve $\mu\,d\lambda_0/d\mu = 0$ for $\beta_g$ through $\mathcal{O}(g^2)$, and solve $\beta_g(g^*) = 0$ in Cell 12.
- **Status:** NOT EXECUTED (Analytical derivation complete; Mathematica verification cell 12 prepared in `QFT_Midterm_Final_v6.nb`).
- **Result & Interpretation:** Confirms $\beta_g = -\epsilon g + 3g^2$, $g^* = \epsilon/3$, and $\delta Z_{\phi,\text{MS}} = 0$, matching Ch. 15 Eq. (15.19) and Ch. 21 Eq. (21.9). Anchored via A-10 through A-12.
