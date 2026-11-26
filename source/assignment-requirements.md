# Assignment Requirements Ledger (`ara/source/assignment-requirements.md`)

Source Document: `FeynCalc_Midterm_Project.pdf` (Detailed Mathematical Brief)
Scope: Real scalar $\phi^4$ theory renormalization from one loop to the critical isotherm of water (Parts 1 & 2).

---

## 1.1 — Generate and read the one-loop diagrams
- **Source PDF Page:** Page 1.
- **Source Question / Requirement:** "Use FeynArts and FeynCalc with the real-scalar $\Phi^4$ model $[S]$ to generate all one-loop 1PI two- and four-point diagrams and their amplitudes. Include your `CreateTopologies`, `InsertFields`, `Paint`, `CreateFeynAmp`, and `FCFAConvert` code. Label momenta, determine symmetry factors, and identify the three four-point channels. Give the converted integrands and their ToPaVe forms, stating the Wick-rotation and loop-measure conventions."
- **Mapped Skill Task ID:** 1.1.a through 1.1.f.
- **Mapped Notebook Section/Cell Group:** Section 1.1.
- **Status:** `verified`
- **Notes / Verification:** Action normalization: Euclidean signature, $m^2 > 0$, $S = \int d^d x \left[ \frac{1}{2}(\partial\phi)^2 + \frac{1}{2}m^2\phi^2 + \frac{\mu^\epsilon \lambda}{4!}\phi^4 \right]$, $d=4-\epsilon$, $g=\frac{\lambda}{16\pi^2}$. Tree vertices: $\Gamma^{(2)} = p^2 + m^2$, $\Gamma^{(4)} = \lambda$ (with overall $\mu^\epsilon$ stripped).

## 1.2 — Cutoff and dimensional regularization
- **Source PDF Page:** Page 1.
- **Source Question / Requirement:** Define tadpole $T$ and zero-momentum bubble $B(P)$. For $|k| < \Lambda$, evaluate $T$ and $B(0)$ exactly and expand through $\Lambda^{-2}$. Independently obtain their DR Laurent expansions through the finite $\epsilon^0$ terms. Identify power divergences, logarithms, and poles. Verify $B(0) = -\partial T / \partial m^2$ in both schemes.
- **Mapped Skill Task ID:** 1.2.a through 1.2.f.
- **Mapped Notebook Section/Cell Group:** Section 1.2.
- **Status:** `verified`

## 1.3 — Counterterms and regulator independence
- **Source PDF Page:** Page 1.
- **Source Question / Requirement:** Use Euclidean vertex formulas with counterterms. Impose renormalization conditions $\Gamma^{(2)}(0) = m^2$, $\partial_{p^2}\Gamma^{(2)}|_{0} = 1$, and $\Gamma^{(4)}(0) = \lambda$ in each regulator. Derive counterterms, show $B(P)-B(0)$ and its slope agree across regulators, take $\Lambda \to \infty$ before shifting loop momentum for cutoff, and distinguish MS from finite subtraction.
- **Mapped Skill Task ID:** 1.3.a through 1.3.f.
- **Mapped Notebook Section/Cell Group:** Section 1.3.
- **Status:** `verified`

## 1.4 — The beta function and fixed point
- **Source PDF Page:** Page 1.
- **Source Question / Requirement:** Derive MS beta function $\beta_g$ through $g^2$ and nonzero fixed point $g^*$ through $\epsilon$. Establish one-loop field counterterm and explain tadpole momentum independence. Distinguish MS from finite conditions.
- **Mapped Skill Task ID:** 1.4.a through 1.4.f.
- **Mapped Notebook Section/Cell Group:** Section 1.4.
- **Status:** `verified`

## 2.1 — The two-loop two-point function
- **Source PDF Page:** Page 2.
- **Source Question / Requirement:** Tune mass to criticality. Generate all two-loop 1PI two-point diagrams with FeynArts/FeynCalc. Identify $p$-dependent graphs, derive sunset symmetry factor, evaluate $H(p)$ by two successive massless convolutions, give gamma-function expression, Laurent expansion, and coefficient of $p^2/\epsilon$. Analyze subdivergences and counterterm insertions.
- **Mapped Skill Task ID:** 2.1.a through 2.1.f.
- **Mapped Notebook Section/Cell Group:** Section 2.1.
- **Status:** `verified`

## 2.2 — Field renormalization and the anomalous dimension
- **Source PDF Page:** Page 2.
- **Source Question / Requirement:** Determine sunset contribution and sign, extract $Z_\phi$, derive $\gamma_\phi(g)$ and $\eta = 2\gamma_\phi(g^*)$, check using finite $\log(p^2/\mu^2)$, and justify one-loop $g^*$ sufficiency for $\eta$ through $\epsilon^2$.
- **Mapped Skill Task ID:** 2.2.a through 2.2.e.
- **Mapped Notebook Section/Cell Group:** Section 2.2.
- **Status:** `verified`

## 2.3 — Scaling and comparison with water
- **Source PDF Page:** Page 2.
- **Source Question / Requirement:** Add external field $h$, derive scaling relation $\delta = \frac{d+2-\eta}{d-2+\eta}$, expand through $\epsilon^2$ before setting $\epsilon=1$, justify water critical-isotherm mapping, derive scattering slope $-2+\eta$, and present comparison table with 3D Ising bootstrap and Straub water fit.
- **Mapped Skill Task ID:** 2.3.a through 2.3.g.
- **Mapped Notebook Section/Cell Group:** Section 2.3.
- **Status:** `verified`
