# Claims Ledger (`ara/logic/claims.md`)

---

## 1.1 — Generate and read the one-loop diagrams
- **Question & Scope:** Generate all one-loop 1PI two- and four-point diagrams in real scalar $\phi^4$ theory using FeynArts and FeynCalc. Determine symmetry factors, identify the three four-point channels, and convert amplitudes to ToPaVe forms.
- **Assumptions & Conventions:** Euclidean signature, $m^2 > 0$, $d = 4-\epsilon$, $g = \frac{\lambda}{16\pi^2}$, one $\mu^\epsilon$ per loop in DR, sharp cutoff $d=4$, tree vertex $\Gamma^{(4)} = \lambda$ with overall $\mu^\epsilon$ stripped.
- **Derived Results / Claims:**
  - **Action & Propagator (Anchor A-01, A-02):** $S = \int d^d x \left[ \frac{1}{2}(\partial\phi)^2 + \frac{1}{2}m^2\phi^2 + \frac{\mu^\epsilon \lambda}{4!}\phi^4 \right]$, $G_0(k) = \frac{1}{k^2 + m^2}$, $\Gamma_{\text{tree}}^{(2)} = p^2 + m^2$, $\Gamma_{\text{tree}}^{(4)} = \lambda$.
  - **One-loop 1PI diagrams (Anchor A-03):** Tadpole graph giving $\Delta\Gamma_1^{(2)} = \frac{\lambda T}{2}$ (symmetry factor $1/2$), and three four-point channels giving $\Gamma_1^{(4)} = -\frac{\lambda^2}{2} \sum_{j} B(P_{1j})$ with $P_{1j} = p_i + p_j$ and symmetry factor $1/2$ per channel.
- **Status:** derived
