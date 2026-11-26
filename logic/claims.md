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
- **Question & Scope:** In both regulators impose $\Gamma^{(2)}(0)=m^2$, $\partial_{p^2}\Gamma^{(2)}|_0=1$, $\Gamma^{(4)}(0)=\lambda$; derive $\delta Z_\phi,\delta m^2,\delta\lambda$; show that $B(P)-B(0)$ and its slope at $P^2=0$ agree once the regulators are removed.
- **Assumptions & Conventions:** Euclidean, $m^2>0$, incoming $p_i$, $P_{ij}=p_i+p_j$. Brief's vertices: $\Gamma^{(2)}=p^2+m^2+\delta Z_\phi p^2+\delta m^2+\frac{\lambda}{2}T$ and $\Gamma^{(4)}=\lambda+\delta\lambda-\frac{\lambda^2}{2}[B(P_{12})+B(P_{13})+B(P_{14})]$. Counterterms are power series $\delta Z=z^{(1)}\lambda+z^{(2)}\lambda^2+\cdots$, $\delta m^2=b^{(1)}\lambda+\cdots$, $\delta\lambda=a^{(1)}\lambda+\cdots$ (A-07).
- **Derivation (A-06, A-07):**
  1. $\partial_{p^2}\Gamma^{(2)}|_0=1+\delta Z_\phi=1$ because $T$ does not depend on $p$, so $z^{(1)}=0$ and $\delta Z_\phi=\mathcal O(\lambda^2)$ in both regulators.
  2. $\Gamma^{(2)}(0)=m^2+\delta m^2+\frac\lambda2T=m^2$ gives $\delta m^2=-\frac\lambda2T$, i.e. $b^{(1)}=-\frac12T$.
     - Cutoff: $\delta m^2=-\frac{\lambda}{32\pi^2}\big[\Lambda^2-m^2\ln\frac{\Lambda^2}{m^2}-\frac{m^4}{\Lambda^2}+\mathcal O(\Lambda^{-4})\big]$.
     - DR: $\delta m^2=-\frac{\lambda m^2}{32\pi^2}\big[-\frac2\epsilon+\gamma_E-1-\ln\frac{4\pi\mu^2}{m^2}+\mathcal O(\epsilon)\big]$.
  3. At $p_i=0$ all $P_{1j}=0$, so $\Gamma^{(4)}(0)=\lambda+\delta\lambda-\frac{3\lambda^2}{2}B(0)=\lambda$ gives $\delta\lambda=\frac{3\lambda^2}{2}B(0)$ ($a^{(1)}=0$, $a^{(2)}=\frac32B(0)$, matching Eq. 13.22).
     - Cutoff: $\delta\lambda=\frac{3\lambda^2}{32\pi^2}\big[\ln\frac{\Lambda^2}{m^2}-1+\frac{2m^2}{\Lambda^2}+\mathcal O(\Lambda^{-4})\big]$.
     - DR: $\delta\lambda=\frac{3\lambda^2}{32\pi^2}\big[\frac2\epsilon-\gamma_E+\ln\frac{4\pi\mu^2}{m^2}+\mathcal O(\epsilon)\big]$.
- **Subtracted bubble (A-08, A-09):**
  - *DR.* Feynman parametrization (13.20, $\alpha=\beta=1$) gives $\frac{1}{(k^2+m^2)((k+P)^2+m^2)}=\int_0^1\frac{dx}{[(k+xP)^2+\Delta]^2}$, $\Delta=m^2+x(1-x)P^2$. The Feynman parameter $x$ is a convex-combination weight, so it ranges over $[0,1]$; the momentum integral already ran over all $k$. After the shift $\ell=k+xP$ and Eq. 13.7 with $\alpha=2$: $B_{\rm DR}(P)=\frac{\mu^\epsilon\Gamma(\epsilon/2)}{(4\pi)^{2-\epsilon/2}}\int_0^1dx\,\Delta^{-\epsilon/2}$. Then $B(P)-B(0)=\frac{\mu^\epsilon\Gamma(\epsilon/2)}{(4\pi)^{2-\epsilon/2}}\int_0^1dx[\Delta^{-\epsilon/2}-m^{-\epsilon}]$. Since $\Delta^{-\epsilon/2}-m^{-\epsilon}=-\frac\epsilon2\ln\frac{\Delta}{m^2}+\mathcal O(\epsilon^2)$ and $\Gamma(\epsilon/2)=\frac2\epsilon+\cdots$, the pole cancels and the $\epsilon^0$ term is exact in the limit $\epsilon\to0$ (higher orders vanish, lower orders are absent): $-\frac{1}{16\pi^2}\int_0^1dx\ln\big(1+x(1-x)\frac{P^2}{m^2}\big)$.
  - *Cutoff.* Form $B_\Lambda(P)-B_\Lambda(0)$ first. The integrand falls as $|k|^{-5}$ (and the odd $1/k^5$ term averages to zero), so it is absolutely convergent in $d=4$ and $\Lambda\to\infty$ can be taken before shifting $k\to k-xP$. The radial integral is $\frac{1}{16\pi^2}\int_0^\infty u\,du\,[(u+\Delta)^{-2}-(u+m^2)^{-2}]=-\frac{1}{16\pi^2}\ln\frac{\Delta}{m^2}$, because the antiderivative $F_\Delta(u)=\ln(u+\Delta)+\frac{\Delta}{u+\Delta}$ gives $F_\Delta(\infty)-F_{m^2}(\infty)=0$ and $F_\Delta(0)-F_{m^2}(0)=\ln\frac{\Delta}{m^2}$, so the integral is $0-\ln\frac{\Delta}{m^2}$.
  - *Comparison.* The two $x$-integrands are identical for every $x\in(0,1)$, hence their integrals over $x$ are identical; both give $-\frac{1}{16\pi^2}\big[\sqrt{1+\frac{4m^2}{P^2}}\ln\frac{\sqrt{P^2+4m^2}+\sqrt{P^2}}{\sqrt{P^2+4m^2}-\sqrt{P^2}}-2\big]$. Comparing the integrands is stronger than comparing only the integrals, and the closed-form integral is computed too (Cell 11).
  - *Slope.* $B'(0)=-\frac{1}{16\pi^2m^2}\int_0^1x(1-x)dx=-\frac{1}{96\pi^2m^2}$ in both regulators.
- **Status:** derived

## 1.4 — The beta function and fixed point
- **Question & Scope:** From the DR pole counterterms (MS) derive $\beta_g$ through $g^2$ and the nonzero fixed point through $\epsilon$; show the one-loop field counterterm; explain why the tadpole cannot change the momentum exponent; separate MS from the finite SII conditions.
- **Assumptions & Conventions:** $d=4-\epsilon$, $g=\lambda/(16\pi^2)$, $[\lambda_0]=\epsilon$ (A-10), $\lambda_0$ independent of the scale $\mu$.
- **Derivation (A-10, A-11, A-12):**
  1. Field counterterm: the one-loop two-point correction is the tadpole, independent of $p$, so $\delta Z_{\phi,\rm MS}=0+\mathcal O(g^2)$ and $Z_\phi=1+\mathcal O(g^2)$. Since $\gamma_\phi\propto\mu\,\partial_\mu\ln Z_\phi=\mathcal O(g^2)$, the tadpole shifts only the mass and cannot change the momentum exponent at one loop.
  2. MS keeps only poles. $B_{\rm DR}(0)|_{\rm pole}=\frac{2}{16\pi^2\epsilon}$, so $\delta\lambda_{\rm MS}=\frac{3\lambda^2}{2}\cdot\frac{2}{16\pi^2\epsilon}=\frac{3\lambda^2}{16\pi^2\epsilon}$. From $\delta\lambda=\lambda_0Z^2-\lambda$ (p. 149) with the $\mu^\epsilon$ convention, $\lambda_0=\mu^\epsilon(\lambda+\delta\lambda)/Z^2$, so $\lambda_0=16\pi^2\mu^\epsilon\big(g+\frac{3g^2}{\epsilon}+\mathcal O(g^3)\big)$.
  3. $\mu\,\frac{d\lambda_0}{d\mu}=0$: the bare action was written without reference to the auxiliary scale $\mu$, so changing $\mu$ must not change $\lambda_0$. Then $0=\epsilon g+3g^2+(1+\frac{6g}{\epsilon})\beta_g$, $\beta_g=-\frac{\epsilon g+3g^2}{1+6g/\epsilon}=-\epsilon g+3g^2+\mathcal O(g^3)$, since $-(\epsilon g+3g^2)(1-\frac{6g}{\epsilon})=-\epsilon g-3g^2+6g^2$. The $1/\epsilon$ terms cancel, as they must.
  4. $\beta_g(g^*)=0$: $g^*=0$ (Gaussian) or $g^*=\frac\epsilon3+\mathcal O(\epsilon^2)$ (Wilson–Fisher), i.e. $\lambda^*=\frac{(4\pi)^2}{3}\epsilon$ (Eq. 21.9). This matches $\beta(\lambda)=-\epsilon\lambda+\frac{3\lambda^2}{(4\pi)^2}$ (printed p. 219) and Eq. 15.19.
  5. MS vs. SII: SII (1.3) fixes counterterms at $p=0$ and keeps finite pieces such as $\gamma_E$ and $\ln(4\pi\mu^2/m^2)$; MS (1.4) keeps only poles, so the counterterms are mass independent.
- **Status:** derived

## 2.1 — Two-loop two-point function (massless DR, $p^2>0$)
- **Question & Scope:** Generate all two-loop 1PI two-point graphs, find the $p$-dependent one, derive its symmetry factor, evaluate $H(p)$ by two massless convolutions (gamma form, Laurent expansion, $p^2/\epsilon$ coefficient), and show that four-point subdivergence counterterms do not affect the $p^2$ pole.
- **Assumptions & Conventions:** Criticality means $m^2=0$ (the mass counterterm vanishes in massless DR, since $T_{m=0}=0$). $d=4-\epsilon$, $\mu^\epsilon$ per loop so $\mu^{2\epsilon}$ here, $g=\lambda/(16\pi^2)$, $\epsilon=2\epsilon_{\rm FC}$, $\lambda^2/(16\pi^2)^2=g^2$.
- **Diagrams (A-13):** Two quartic vertices, two external legs, three internal propagators. The 1PI possibilities are (i) the sunset (one external leg on each vertex, three lines between them) and (ii) the double scoop (both external legs on one vertex, two lines to the other vertex, a self-loop on the other vertex). Putting one external leg on a vertex that carries a self-loop and a single line to the second vertex gives a reducible graph and is excluded.
- **$p$ dependence:** In the sunset the momentum $p$ flows through the loops, so $p$ appears in a denominator. In the double scoop $p$ enters and leaves at the same vertex and never flows through a loop; it is $p$-independent and, with $m=0$, a product of scaleless integrals, hence $0$ in DR.
- **Sunset symmetry factor:** The term is $\frac{1}{2!}\big(\frac{-\lambda}{4!}\big)^2$. Choose which vertex takes external leg 1 (2 ways), its leg (4), the leg of the other vertex for external leg 2 (4), then pair the remaining three legs of each vertex (3! ways): $2\cdot4\cdot4\cdot6=192$. Factor: $\frac{192}{2!\,(4!)^2}=\frac{192}{1152}=\frac16$. (Double scoop for comparison: $2\cdot12\cdot12=288$, $\frac{288}{1152}=\frac14$.) The two vertices give $(-\lambda)^2=+\lambda^2$, so the amputated sunset is $+\frac{\lambda^2}{6}H(p)$; the 1PI function is minus the amputated self-energy graph, consistent with the notes' $\Sigma_a=-\frac{\lambda^2}{3!}\int\!\!\int\cdots$ (p. 132). Hence $\Gamma^{(2)}\ni-\frac{\lambda^2}{6}H(p)$.
- **Massless convolution (A-14):** With Feynman parameter $w$ (Eq. 13.20), $\frac{1}{(k^2)^a((k+P)^2)^b}=\frac{\Gamma(a+b)}{\Gamma(a)\Gamma(b)}\int_0^1dw\frac{w^{b-1}(1-w)^{a-1}}{[(k+wP)^2+w(1-w)P^2]^{a+b}}$. Shifting $k$ and applying Eq. 13.7 gives $\frac{\Gamma(a+b-\frac d2)}{(4\pi)^{d/2}\Gamma(a)\Gamma(b)}(P^2)^{\frac d2-a-b}\int_0^1dw\,w^{\frac d2-a-1}(1-w)^{\frac d2-b-1}$, and the Euler beta integral is $\frac{\Gamma(\frac d2-a)\Gamma(\frac d2-b)}{\Gamma(d-a-b)}$. Hence $G(a,b)=\frac{\Gamma(\frac d2-a)\Gamma(\frac d2-b)\Gamma(a+b-\frac d2)}{(4\pi)^{d/2}\Gamma(a)\Gamma(b)\Gamma(d-a-b)}$.
- **Evaluation of $H$ (A-15, A-16):**
  1. Inner loop: $\int\frac{d^d\ell}{(2\pi)^d}\frac{1}{\ell^2(r-\ell)^2}=G(1,1)(r^2)^{\frac d2-2}$ with $r=p-k$ and $G(1,1)=\frac{\Gamma(\frac d2-1)^2\Gamma(2-\frac d2)}{(4\pi)^{d/2}\Gamma(d-2)}$.
  2. Outer loop: $\int\frac{d^dk}{(2\pi)^d}\frac{1}{k^2((p-k)^2)^{2-d/2}}=G(1,2-\tfrac d2)(p^2)^{d-3}$ with $G(1,2-\tfrac d2)=\frac{\Gamma(\frac d2-1)\Gamma(d-2)\Gamma(3-d)}{(4\pi)^{d/2}\Gamma(2-\frac d2)\Gamma(\frac{3d}{2}-3)}$.
  3. The factors $\Gamma(2-\frac d2)$ and $\Gamma(d-2)$ cancel: $H(p)=\frac{\mu^{2\epsilon}(p^2)^{d-3}}{(4\pi)^d}\frac{\Gamma(3-d)\Gamma(\frac d2-1)^3}{\Gamma(\frac{3d}{2}-3)}=\frac{\mu^{2\epsilon}(p^2)^{1-\epsilon}}{(4\pi)^{4-\epsilon}}\frac{\Gamma(-1+\epsilon)\Gamma(1-\frac\epsilon2)^3}{\Gamma(3-\frac{3\epsilon}{2})}$.
  4. Expansion with $\Gamma(z+1)=z\Gamma(z)$ (A-15): $\Gamma(-1+\epsilon)=-\frac1\epsilon+\gamma_E-1+\mathcal O(\epsilon)$; $\Gamma(1-\frac\epsilon2)^3=1+\frac{3\gamma_E}{2}\epsilon+\cdots$; $\frac{1}{\Gamma(3-\frac{3\epsilon}{2})}=\frac12\big[1+\frac{3\epsilon}{2}\psi(3)\big]$ with $\psi(3)=\frac32-\gamma_E$. The product is $\frac12\big[-\frac1\epsilon+\gamma_E-\frac{13}{4}\big]$. The prefactor $(4\pi)^{\epsilon}\big(\frac{p^2}{\mu^2}\big)^{-\epsilon}=1+\epsilon\ln4\pi-\epsilon\ln\frac{p^2}{\mu^2}$ adds $\frac12\ln\frac{p^2}{\mu^2}-\frac12\ln4\pi$.
  5. Result: $H(p)=\frac{p^2}{(16\pi^2)^2}\Big[-\frac{1}{2\epsilon}+\frac12\ln\frac{p^2}{\mu^2}+\frac{\gamma_E}{2}-\frac{13}{8}-\frac12\ln4\pi+\mathcal O(\epsilon)\Big]$. The coefficient of $p^2/\epsilon$ is $-\frac{1}{2(16\pi^2)^2}=-\frac{1}{512\pi^4}$. There is no $1/\epsilon^2$ term.
- **Subdivergences (A-07, A-11):** The two-loop counterterm graphs obtained by shrinking a divergent subgraph are: (a) the bubble of the sunset (or of the scoop) shrunk to a point, which leaves a one-loop tadpole with a $\delta\lambda$ vertex; (b) the tadpole subgraph of the scoop shrunk to a point, which is a $\delta m^2$ insertion (zero, because $m=0$ in massless DR); (c) $\delta Z_\phi$ insertions (zero, because $\delta Z_\phi^{(1)}=0$). Case (a) equals $-\frac{\delta\lambda}{2}\int\frac{d^dk}{(2\pi)^d}\frac{1}{k^2}$, which has no scale and vanishes in DR; in any case it contains no $p$, so it could only change the $p^0$ part and never the $p^2$ pole. The absence of $1/\epsilon^2$ in $H$ confirms that the sunset has no nested divergence requiring such a cancellation.
- **Status:** derived

## 2.2 — $Z_\phi$, $\gamma_\phi$, and $\eta$
- **Question & Scope:** Find the sunset contribution including sign, extract $Z_\phi$, derive $\gamma_\phi$ and $\eta=2\gamma_\phi(g^*)$, check against the $\ln(p^2/\mu^2)$ term, and explain why one-loop $g^*$ suffices through $\epsilon^2$.
- **Derivation (A-17, A-18, A-19):**
  1. $\Gamma^{(2)}=p^2(1+\delta Z)-\frac{\lambda^2}{6}H(p)+\cdots$. With $\frac{\lambda^2}{(16\pi^2)^2}=g^2$: $-\frac{\lambda^2}{6}\frac{H}{p^2}=g^2\Big[\frac{1}{12\epsilon}-\frac{1}{12}\ln\frac{p^2}{\mu^2}-\frac{1}{6}\Big(\frac{\gamma_E}{2}-\frac{13}{8}-\frac12\ln4\pi\Big)\Big]$. The pole is positive.
  2. MS cancels the pole: $\delta Z=-\frac{g^2}{12\epsilon}$, so $Z_\phi=1-\frac{g^2}{12\epsilon}+\mathcal O(g^3)$ with $\phi_0=Z_\phi^{1/2}\phi$ (A-17).
  3. $\gamma_\phi=\frac12\mu\frac{d\ln Z_\phi}{d\mu}\big|_{\rm bare}=\frac12\frac{d\ln Z_\phi}{dg}\beta_g=\frac12\Big(-\frac{g}{6\epsilon}\Big)\beta_g$. Only the $-\epsilon g$ part of $\beta_g$ produces a finite term, $\frac{g^2}{12}$; the $3g^2$ part gives $-\frac{g^3}{4\epsilon}$, which cancels against the $g^3$ pole of $Z_\phi$ at the next order (A-18 defines $\gamma$ in this way). Hence $\gamma_\phi(g)=\frac{g^2}{12}+\mathcal O(g^3)$, equal to the textbook Eq. 15.18, $\gamma=\frac{\lambda^2}{12(4\pi)^4}$.
  4. At the fixed point $g^*=\frac\epsilon3$: $\eta=2\gamma_\phi(g^*)=\frac{g^{*2}}{6}=\frac{\epsilon^2}{54}$.
  5. Log check: the renormalized function is $\Gamma_R^{(2)}/p^2=1-\frac{g^2}{12}\ln\frac{p^2}{\mu^2}+\text{const}\cdot g^2$. Matching $G\propto(p^2)^{-1+\eta/2}$, i.e. $\Gamma^{(2)}\propto(p^2)^{1-\eta/2}$, gives $\frac{\eta}{2}=\frac{g^2}{12}$, i.e. $\eta=\frac{g^2}{6}=2\gamma_\phi$, in agreement.
  6. Why one-loop $g^*$ suffices: $\gamma_\phi=\frac{g^2}{12}+\mathcal O(g^3)$ and $g^*=\frac\epsilon3+c\,\epsilon^2$. Then $g^{*2}=\frac{\epsilon^2}{9}+\frac{2c}{3}\epsilon^3$, so the unknown two-loop correction to $g^*$ and the $\mathcal O(g^3)$ part of $\gamma_\phi$ both start at $\epsilon^3$.
- **Status:** derived

## 2.3 — $\delta$, the critical isotherm, and the water comparison
- **Question & Scope:** Add a uniform source, derive $\delta=\frac{d+2-\eta}{d-2+\eta}$, expand to $\epsilon^2$ before setting $\epsilon=1$, relate $M$ and $h$ to $\rho$ and $P$, give the scattering slope, and compare with the water fit and bootstrap benchmark.
- **Derivation (A-20, A-21):**
  1. $S_h=S-\int d^dx\,h\phi$, $M=\langle\phi\rangle_h$.
  2. At the fixed point the scaling dimension of $\phi$ is the canonical $\frac{d-2}{2}$ (p. 216) plus the anomalous part, $\Delta_\phi=\frac{d-2}{2}+\gamma_\phi=\frac{d-2+\eta}{2}$ (p. 217, $D(\lambda)$).
  3. Since $\int d^dx\,h\phi$ is dimensionless, $[h]=y_h=d-\Delta_\phi=\frac{d+2-\eta}{2}$.
  4. Dimensional analysis at $T=T_c$ gives $M\propto{\rm sgn}(h)|h|^{\Delta_\phi/y_h}$, and by definition this exponent is $1/\delta$, so $\delta=\frac{y_h}{\Delta_\phi}=\frac{d+2-\eta}{d-2+\eta}$.
  5. With $d=4-\epsilon$, $\eta=\frac{\epsilon^2}{54}$: $\delta=\frac{6-\epsilon-\eta}{2-\epsilon+\eta}=3+\epsilon+\frac{25}{54}\epsilon^2+\mathcal O(\epsilon^3)$. At $\epsilon=1$ the expanded result is $\delta=4+\frac{25}{54}=4.46296$ and $\eta=\frac{1}{54}=0.018519$. (Inserting $\eta=\frac{1}{54}$ directly into the unexpanded formula gives $4.8909$; this is a different truncation and is shown only for contrast.)
- **Water mapping (A-22, application):** Ising/liquid–gas universality identifies the order parameter with $\rho-\rho_c$. On the critical isotherm the field conjugate to $\rho$ is $\mu_{\rm chem}-\mu_c$, and Gibbs–Duhem at fixed $T$ gives $dP=\rho\,d\mu_{\rm chem}$ with $\rho\to\rho_c\neq0$, so $h\propto\mu_{\rm chem}-\mu_c\propto P-P_c$ to leading order. Hence $\frac{P-P_c}{P_c}\sim A\,{\rm sgn}(\Delta\rho)\,|\Delta\rho/\rho_c|^{\delta}$ with a nonuniversal amplitude $A$. The propagator $G(p)\propto(p^2)^{-1+\eta/2}$ gives $S(q)\propto q^{-2+\eta}$ for $\xi^{-1}\ll q\ll a^{-1}$; predicted slope $-2+\eta=-1.98148$.
- **Comparison (A-23, external inputs):**

| Quantity | Your result ($d=3$) | Reference |
|---|---|---|
| $\eta$ | $0.018519$ | $\eta_B=2\Delta_\sigma-1=0.036298$ |
| $\delta$ | $4.462963$ | $\delta_B=3/\Delta_\sigma-1=4.789843$ |
| Water $\delta$ | – | $4.324$ (Straub fit) |
| Bootstrap input | – | $\Delta_\sigma=0.518148806(24)$ |

  The expanded $\delta$ is $6.8\%$ below the bootstrap value and $3.2\%$ above the water fit; $\eta$ is about half the bootstrap value, as expected from a truncated $\epsilon^2$ series evaluated at $\epsilon=1$.
- **Status:** derived (benchmarks external)
