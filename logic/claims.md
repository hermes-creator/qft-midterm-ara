# Claims Ledger (`ara/logic/claims.md`)

---

## 1.1 — Generate and read the one-loop diagrams
- **Question & Scope:** Generate all one-loop 1PI two- and four-point diagrams in real scalar $\phi^4$ theory using FeynArts and FeynCalc. Determine symmetry factors, identify the three four-point channels, and convert amplitudes to ToPaVe forms.
- **Assumptions & Conventions:** Euclidean signature, $m^2 > 0$, $d = 4-\epsilon$, $g = \frac{\lambda}{16\pi^2}$, one $\mu^\epsilon$ per loop in DR, sharp cutoff $d=4$, tree vertex $\Gamma^{(4)} = \lambda$ with overall $\mu^\epsilon$ stripped.
- **Derived Results / Claims:**
  - **Action & Propagator (Anchor A-01, A-02):** $S = \int d^d x \left[ \frac{1}{2}(\partial\phi)^2 + \frac{1}{2}m^2\phi^2 + \frac{\mu^\epsilon \lambda}{4!}\phi^4 \right]$, $G_0(k) = \frac{1}{k^2 + m^2}$, $\Gamma_{\text{tree}}^{(2)} = p^2 + m^2$, $\Gamma_{\text{tree}}^{(4)} = \lambda$.
  - **One-loop 1PI diagrams (Anchor A-03):** Tadpole graph giving $\Delta\Gamma_1^{(2)} = \frac{\lambda T}{2}$ (symmetry factor $1/2$), and three four-point channels giving $\Gamma_1^{(4)} = -\frac{\lambda^2}{2} \sum_{j} B(P_{1j})$ with $P_{1j} = p_i + p_j$ and symmetry factor $1/2$ per channel.
- **Status:** derived

## 1.2 — Cutoff and dimensional regularization
- **Question & Scope:** Evaluate the tadpole integral $T$ and zero-momentum bubble integral $B(0)$ using both a sharp momentum cutoff $\Lambda$ and dimensional regularization (DR). Isolate power divergences, logarithms, and poles, and verify the derivative identity $B(0) = -\partial T / \partial m^2$.
- **Assumptions & Conventions:** Euclidean signature, $m^2 > 0$, sharp cutoff domain $|k| < \Lambda$ in $d=4$, dimensional regularization in $d = 4-\epsilon$ with one $\mu^\epsilon$ per loop.
- **Derived Results / Claims:**
  - **Sharp Cutoff Exact & Expanded (Anchor A-05):**
    $16\pi^2 T_\Lambda = \Lambda^2 - m^2 \ln(1 + \frac{\Lambda^2}{m^2}) = \Lambda^2 - m^2 \ln\frac{\Lambda^2}{m^2} - \frac{m^4}{\Lambda^2} + \mathcal{O}(\Lambda^{-4})$
    $16\pi^2 B_\Lambda(0) = \ln(1 + \frac{\Lambda^2}{m^2}) - \frac{\Lambda^2}{\Lambda^2 + m^2} = \ln\frac{\Lambda^2}{m^2} - 1 + \frac{2m^2}{\Lambda^2} + \mathcal{O}(\Lambda^{-4})$
  - **Dimensional Regularization Master & Laurent Expansions (Anchor A-04):**
    $J_a(M^2) = \mu^\epsilon (M^2)^{d/2 - a} \frac{\Gamma(a - d/2)}{(4\pi)^{d/2} \Gamma(a)}$
    $16\pi^2 T_{\text{DR}} = m^2 \left( -\frac{2}{\epsilon} + \gamma_E - 1 - \ln\frac{4\pi\mu^2}{m^2} \right) + \mathcal{O}(\epsilon)$
    $16\pi^2 B_{\text{DR}}(0) = \frac{2}{\epsilon} - \gamma_E + \ln\frac{4\pi\mu^2}{m^2} + \mathcal{O}(\epsilon)$
  - **Derivative Identity:** $B(0) = -\frac{\partial T}{\partial m^2}$ holds identically in both schemes.
- **Status:** derived

## 1.3 — Counterterms and regulator independence
- **Question & Scope:** Impose the zero-momentum (SII) renormalization conditions $\Gamma^{(2)}(0) = m^2$, $\left.\partial_{p^2}\Gamma^{(2)}\right|_{p^2=0} = 1$, and $\Gamma^{(4)}(0) = \lambda$ in both the sharp-cutoff and dimensional-regularization schemes. Derive $\delta Z_\phi$, $\delta m^2$, and $\delta\lambda$, and prove that the subtracted bubble $B(P) - B(0)$ and its slope $B'(0)$ are finite and regulator-independent as the regulators are removed.
- **Assumptions & Conventions:** Euclidean signature, $m^2 > 0$, all external momenta $p_i$ incoming with $P_{ij} = p_i + p_j$. One-loop 1PI vertices with Euclidean signs:
  $$\Gamma^{(2)}(p^2) = p^2 + m^2 + \delta Z_\phi p^2 + \delta m^2 + \frac{\lambda}{2} T, \qquad \Gamma^{(4)}(p_1,p_2,p_3,p_4) = \lambda + \delta\lambda - \frac{\lambda^2}{2}\big[B(P_{12}) + B(P_{13}) + B(P_{14})\big].$$
- **Derived Results / Claims:**
  - **One-loop Counterterms under SII (Anchors A-06, A-07):** Expanding $\delta Z = z^{(1)}\lambda + \cdots$, $\delta m^2 = b^{(1)}\lambda + \cdots$, $\delta\lambda = a^{(1)}\lambda + \cdots$:
    1. Because the tadpole $T$ is independent of external momentum $p^2$, $\left.\partial_{p^2}\Gamma^{(2)}\right|_0 = 1 + \delta Z_\phi = 1 \implies \delta Z_\phi = 0 + \mathcal{O}(\lambda^2)$ in both regulators.
    2. From $\Gamma^{(2)}(0) = m^2 + \delta m^2 + \frac{\lambda}{2}T = m^2$, we obtain $\delta m^2 = -\frac{\lambda}{2}T$:
       - Sharp cutoff: $\delta m^2_\Lambda = -\frac{\lambda}{32\pi^2}\left[\Lambda^2 - m^2\ln\!\left(1+\frac{\Lambda^2}{m^2}\right)\right] = -\frac{\lambda}{32\pi^2}\left[\Lambda^2 - m^2\ln\frac{\Lambda^2}{m^2} - \frac{m^4}{\Lambda^2} + \mathcal{O}(\Lambda^{-4})\right]$.
       - DR: $\delta m^2_{\text{DR}} = -\frac{\lambda m^2}{32\pi^2}\left[-\frac{2}{\epsilon} + \gamma_E - 1 - \ln\frac{4\pi\mu^2}{m^2} + \mathcal{O}(\epsilon)\right]$.
    3. At $p_i = 0$ ($P_{12}=P_{13}=P_{14}=0$), $\Gamma^{(4)}(0) = \lambda + \delta\lambda - \frac{3\lambda^2}{2}B(0) = \lambda \implies \delta\lambda = \frac{3\lambda^2}{2}B(0)$:
       - Sharp cutoff: $\delta\lambda_\Lambda = \frac{3\lambda^2}{32\pi^2}\left[\ln\!\left(1+\frac{\Lambda^2}{m^2}\right) - \frac{\Lambda^2}{\Lambda^2+m^2}\right] = \frac{3\lambda^2}{32\pi^2}\left[\ln\frac{\Lambda^2}{m^2} - 1 + \frac{2m^2}{\Lambda^2} + \mathcal{O}(\Lambda^{-4})\right]$.
       - DR: $\delta\lambda_{\text{DR}} = \frac{3\lambda^2}{32\pi^2}\left[\frac{2}{\epsilon} - \gamma_E + \ln\frac{4\pi\mu^2}{m^2} + \mathcal{O}(\epsilon)\right]$.
  - **Subtracted Bubble $B(P) - B(0)$ and Regulator Independence (Anchors A-08, A-09):**
    - *In DR:* Using Feynman parametrization (Eq. 13.20) with $\alpha = \beta = 1$, completing the square $\ell = k + xP$, and integrating over $d = 4 - \epsilon$ dimensions gives
      $$B_{\text{DR}}(P) = \frac{\mu^\epsilon \Gamma(\epsilon/2)}{(4\pi)^{2-\epsilon/2}} \int_0^1 dx\,\big[m^2 + x(1-x)P^2\big]^{-\epsilon/2}.$$
      Subtracting $B_{\text{DR}}(0)$ cancels the $2/\epsilon$ pole and $\gamma_E$, leaving the finite $\epsilon \to 0$ limit:
      $$B(P) - B(0) = -\frac{1}{16\pi^2} \int_0^1 dx\,\ln\!\left(1 + x(1-x)\frac{P^2}{m^2}\right).$$
    - *In Sharp Cutoff:* Because shifting $k \to k - xP$ inside a logarithmically divergent integral with a sharp sphere $|k|<\Lambda$ would introduce a boundary surface term, we first form the difference
      $$B_\Lambda(P) - B_\Lambda(0) = \int_{|k|<\Lambda} \frac{d^4k}{(2\pi)^4}\left[\frac{1}{(k^2+m^2)((k+P)^2+m^2)} - \frac{1}{(k^2+m^2)^2}\right],$$
      which falls off as $1/k^5$ (and $1/k^6$ after angular averaging) and is absolutely convergent in $d=4$. Taking $\Lambda \to \infty$ first, we can safely apply Feynman parametrization and shift $k \to k - xP$. Evaluating the radial integral $\frac{1}{16\pi^2}\int_0^\infty u\,du\left[\frac{1}{(u+m^2+x(1-x)P^2)^2} - \frac{1}{(u+m^2)^2}\right]$ gives the exact same result:
      $$B(P) - B(0) = -\frac{1}{16\pi^2} \int_0^1 dx\,\ln\!\left(1 + x(1-x)\frac{P^2}{m^2}\right) = -\frac{1}{16\pi^2}\left[\sqrt{1+\frac{4m^2}{P^2}}\ln\frac{\sqrt{P^2+4m^2}+\sqrt{P^2}}{\sqrt{P^2+4m^2}-\sqrt{P^2}} - 2\right].$$
    - *Slope at $P^2 = 0$:* Differentiating under the integral sign at $P^2 = 0$:
      $$B'(0) = \left.\frac{d}{dP^2}[B(P)-B(0)]\right|_{P^2=0} = -\frac{1}{16\pi^2 m^2}\int_0^1 x(1-x)\,dx = -\frac{1}{16\pi^2 m^2}\cdot\frac{1}{6} = -\frac{1}{96\pi^2 m^2}.$$
      Both regulators agree identically once the regulators are removed.
- **Status:** derived

## 1.4 — The beta function and fixed point
- **Question & Scope:** Using the DR pole counterterms (Minimal Subtraction, MS), derive the one-loop beta function $\beta_g$ through $\mathcal{O}(g^2)$ and its nonzero Wilson–Fisher fixed point $g^*$ through $\mathcal{O}(\epsilon)$. Establish the one-loop field counterterm, explain why the tadpole cannot alter the momentum exponent, and distinguish MS from the finite SII conditions of Subsection 1.3.
- **Assumptions & Conventions:** Dimensional regularization in $d = 4 - \epsilon$, dimensionless renormalized coupling $g = \frac{\lambda}{16\pi^2}$, bare coupling $\lambda_0$ has mass dimension $[\lambda_0] = 4 - d = \epsilon$ (Anchor A-10) and is independent of the arbitrary RG scale $\mu$.
- **Derived Results / Claims:**
  - **One-loop Field Counterterm and Momentum Exponent (Anchor A-11):** Because the one-loop two-point tadpole $\frac{\lambda}{2}T$ has no $p^2$ dependence, the coefficient of $p^2$ in $\Gamma^{(2)}(p^2)$ receives no one-loop divergence. Therefore $\delta Z_{\phi,\text{MS}} = 0 + \mathcal{O}(g^2)$, $Z_\phi = 1 + \mathcal{O}(g^2)$, and the anomalous dimension $\gamma_\phi(g) = \frac{1}{2}\left.\mu\frac{d\ln Z_\phi}{d\mu}\right|_{\text{bare}} = \mathcal{O}(g^2)$ vanishes at one loop. Consequently, the tadpole only shifts the mass and cannot change the momentum exponent $\eta = 2\gamma_\phi(g^*)$ at one loop.
  - **MS Bare Coupling (Anchor A-11):** In MS, counterterms retain only the $1/\epsilon$ pole parts (dropping finite constants such as $-\gamma_E + \ln(4\pi\mu^2/m^2)$ that appear in the SII scheme of 1.3). From $B_{\text{DR}}(0)\big|_{\text{pole}} = \frac{2}{16\pi^2\epsilon}$, the MS coupling counterterm is $\delta\lambda_{\text{MS}} = \frac{3\lambda^2}{2}\cdot\frac{2}{16\pi^2\epsilon} = \frac{3\lambda^2}{16\pi^2\epsilon}$. With $Z_\phi = 1 + \mathcal{O}(g^2)$ and $\lambda_0 = \mu^\epsilon Z_\phi^{-2}(\lambda + \delta\lambda_{\text{MS}})$, substituting $\lambda = 16\pi^2 g$ yields:
    $$\lambda_0 = 16\pi^2 \mu^\epsilon \left(g + \frac{3g^2}{\epsilon} + \mathcal{O}(g^3)\right).$$
  - **Beta Function $\beta_g$ and Wilson–Fisher Fixed Point $g^*$ (Anchor A-12):** Differentiating $\lambda_0$ with respect to $\ln\mu$ at fixed bare parameters ($\mu\frac{d\lambda_0}{d\mu} = 0$):
    $$0 = \epsilon\left(g + \frac{3g^2}{\epsilon}\right) + \left(1 + \frac{6g}{\epsilon}\right)\beta_g + \mathcal{O}(g^3) \implies \beta_g = -\frac{\epsilon g + 3g^2}{1 + 6g/\epsilon} + \mathcal{O}(g^3).$$
    Expanding consistently through $\mathcal{O}(g^2)$ (writing $\beta_g = c_1 g + c_2 g^2$, where $c_1 = -\epsilon$ cancels the $6g/\epsilon \cdot (-\epsilon g) = -6g^2$ term to give $c_2 = +3$):
    $$\beta_g(g) = \left.\mu\frac{dg}{d\mu}\right|_{\text{bare}} = -\epsilon g + 3g^2 + \mathcal{O}(g^3).$$
    Setting $\beta_g(g^*) = 0$ yields the Gaussian fixed point $g^* = 0$ (IR-unstable for $\epsilon > 0$) and the nontrivial IR-stable Wilson–Fisher fixed point:
    $$g^* = \frac{\epsilon}{3} + \mathcal{O}(\epsilon^2) \quad \left(\lambda^* = \frac{(4\pi)^2}{3}\epsilon + \mathcal{O}(\epsilon^2)\right).$$
  - **Distinction between MS and SII:** In SII (1.3), counterterms are fixed by physical/zero-momentum normalization conditions at $p=0$ and therefore contain finite $m^2$-dependent terms ($\gamma_E$, $\ln(4\pi\mu^2/m^2)$, etc.). In MS (1.4), counterterms are defined to be pure $1/\epsilon$ poles, making $Z_\phi$, $Z_\lambda$, and $\beta_g$ mass-independent and cleanly isolating the UV RG flow.
- **Status:** derived
