# Subpart 1.1 Summary Report

## 1. Derived or Tested Content
- **Model Action & Feynman Rules (Anchor A-01, A-02):** Established the Euclidean real scalar $\phi^4$ action with $m^2 > 0$, $d = 4-\epsilon$, $g = \frac{\lambda}{16\pi^2}$, propagator $G_0(k) = \frac{1}{k^2+m^2}$, tree two-point vertex $\Gamma^{(2)} = p^2 + m^2$, and tree four-point vertex $\Gamma^{(4)} = \lambda$ (with overall $\mu^\epsilon$ stripped).
- **One-Loop Topologies & Amplitudes (Anchor A-03):** Generated 1PI two-point tadpole graph yielding $\Delta\Gamma_1^{(2)} = \frac{\lambda T}{2}$ and three four-point Mandelstam channels yielding $\Gamma_1^{(4)} = -\frac{\lambda^2}{2} \sum_j B(P_{1j})$ with symmetry factor $1/2$ justified from combinatorics.
- **Conventions:** Tracked loop measure $\int \frac{d^d k}{(2\pi)^d}$, Wick rotation, $\mu^\epsilon$ per loop, and FeynCalc D convention conversion $\epsilon = 2\epsilon_{\text{FC}}$.

## 2. Decision Made
- Adopted strict Euclidean signature, standard $\phi^4$ combinatorics, and explicit $\mu^\epsilon$ tracking as mandated by the detailed project brief (`FeynCalc_Midterm_Project.pdf`).
- Structured ARA records (`ara/source/assignment-requirements.md`, `ara/logic/claims.md`, `ara/logic/experiments.md`, `ara/src/environment.md`, `ara/trace/exploration_tree.yaml`, `ara/anchor/equation-map.md`) and linked all key equations to Anchor IDs A-01 through A-03.

## 3. Failed Approach / Dead End
- None encountered in subpart 1.1; diagrammatic expansion and tree vertex normalization matched project specifications cleanly.

## 4. Result Status
- **Status:** **derived** (Analytically derived, checked against Feynman rules and equation map; Mathematica kernel execution status recorded as pending kernel verification).
