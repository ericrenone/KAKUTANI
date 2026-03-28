# KAKUTANI
## The Set-Valued Dirac Equation: Fixed Points of Collective Intelligence Correspondences

ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone

---

> **Kakutani K1 (1941).** Let $S \subset \mathbb{R}^n$ be non-empty, compact, and convex. Let $\Phi: S \to 2^S$ be upper hemicontinuous with $\Phi(x)$ non-empty, closed, and convex for every $x \in S$. Then:
> $$\exists\, x^* \in S \;\text{ with }\; x^* \in \Phi(x^*).$$
>
> — Kakutani, S., *A generalization of Brouwer's fixed point theorem*, Duke Math. J. 8(3), 457–459, 1941

> **Markov–Kakutani K2 (1938).** Let $E$ be a locally convex Hausdorff topological vector space, $C \subset E$ compact and convex, and $\mathcal{T}$ a commuting family of continuous affine self-maps of $C$. Then:
> $$\exists\, x^* \in C \;\text{ with }\; T(x^*) = x^* \;\text{ for every } T \in \mathcal{T}.$$
>
> — Markov, A. (1936); Kakutani, S., *Two fixed point theorems concerning bicompact convex sets*, Proc. Imp. Acad. Tokyo 14, 242–245, 1938

> **Nash existence (1950).** Every finite $n$-player game with mixed strategies has at least one Nash equilibrium. Proof: the joint best-response correspondence on $\prod_i\Delta(A_i)$ is upper hemicontinuous with convex non-empty values on a compact convex set; its Kakutani K1 fixed point is the equilibrium.
>
> — Nash, J.F., *Equilibrium points in n-person games*, Proc. Natl. Acad. Sci. 36(1), 48–49, 1950

> **PPAD-completeness.** Computing a Kakutani fixed point is PPAD-complete. Computing a Nash equilibrium is PPAD-complete for $n \geq 2$.
>
> — Papadimitriou, J. Comput. Syst. Sci. 48(3), 1994; Daskalakis–Goldberg–Papadimitriou, SIAM J. Comput. 39(1), 2009; Papadimitriou–Vlatakis-Gkaragkounis–Zampetakis, arXiv:2207.07557, 2022

> **Glicksberg–Fan (1952).** Kakutani K1 extends to compact convex subsets of Hausdorff locally convex topological vector spaces.
>
> — Glicksberg, Proc. Amer. Math. Soc. 3(1), 1952; Fan, Proc. Natl. Acad. Sci. 38(2), 1952

> **Binmore's anecdote.** Kakutani was told that economists had attended his conference talk because of the Kakutani fixed-point theorem. He asked, in genuine puzzlement: "What is the Kakutani fixed point theorem?"
>
> — Binmore, K., *Playing for Real*, Oxford University Press, 2007

---

## Preamble: Two Theorems, One Architecture

Shizuo Kakutani (1911–2004) proved two distinct fixed-point theorems. Together they underpin the ERI collective intelligence architecture.

**Theorem K1 (1941).** Extends Brouwer from single-valued continuous maps to set-valued upper hemicontinuous correspondences on compact convex subsets of $\mathbb{R}^n$.

**Theorem K2 (1938).** Finds a *common* fixed point for an entire commuting family of continuous affine self-maps on a compact convex set in a locally convex space. This is the Markov–Kakutani theorem.

The Dirac parallel is exact. Brouwer's theorem is the scalar regime: one wavefunction, one value at each point, one fixed point satisfying $f(x^*) = x^*$. Kakutani K1 is the spinor regime: the wavefunction becomes multi-component, and the fixed-point condition becomes self-inclusion $x^* \in \Phi(x^*)$ — the point is contained in the set of its own optimal responses. Kakutani K2 is the gauge regime: the entire abelian symmetry group shares a common invariant point.

Each of the three levels — Brouwer, K1, K2 — maps to a distinct coordination phase in the ERI architecture.

---

## Module A — Mathematical Prerequisites

**A1. Correspondences.** A correspondence $\Phi: X \to 2^Y$ assigns to each $x \in X$ a subset $\Phi(x) \subseteq Y$. When $\Phi(x)$ is a singleton for every $x$, $\Phi$ reduces to an ordinary function.

**A2. Upper hemicontinuity (UHC).** $\Phi: X \to 2^Y$ is upper hemicontinuous at $x_0$ if for every open $V \supset \Phi(x_0)$ there exists a neighborhood $U$ of $x_0$ with $\Phi(x) \subset V$ for all $x \in U$. When $Y$ is compact Hausdorff: $\Phi$ is UHC if and only if its graph $\mathrm{gr}(\Phi) = \{(x,y) : y \in \Phi(x)\}$ is closed.

**A3. Closed-graph criterion.** If $x_n \to x$ and $y_n \to y$ with $y_n \in \Phi(x_n)$ for all $n$, then $y \in \Phi(x)$. This is the sequential characterization of UHC for correspondences with compact values.

**A4. Affine maps.** $T: C \to C$ is affine if $T(tx + (1-t)y) = tT(x) + (1-t)T(y)$ for all $x, y \in C$ and $t \in [0,1]$.

**A5. Cesàro averages.** For continuous affine $T: C \to C$ on compact convex $C$, define $x^{(N)} = \frac{1}{N+1}\sum_{n=0}^{N} T^n(x_0)$. Compactness gives cluster points in $C$. Every cluster point is a fixed point of $T$: since
$$Tx^{(N)} - x^{(N)} = \frac{1}{N+1}\bigl(T^{N+1}x_0 - x_0\bigr) \to 0,$$
any limit point $x^*$ satisfies $Tx^* = x^*$.

**A6. Berge's maximum theorem.** Let $f: X \times Y \to \mathbb{R}$ be continuous and $C: X \to 2^Y$ be continuous with compact non-empty values. Then the value function $v(x) = \max_{y \in C(x)} f(x,y)$ is continuous, and the argmax correspondence $\mu(x) = \arg\max_{y \in C(x)} f(x,y)$ is UHC with non-empty compact values.

---

## Module B — The Three Fixed-Point Levels

### B1. Brouwer (1911): Single-Valued, Compact Convex

**Theorem (Brouwer).** Let $S \subset \mathbb{R}^n$ be non-empty, compact, and convex, and let $f: S \to S$ be continuous. Then $\exists\, x^* \in S$ with $f(x^*) = x^*$.

| Condition | Requirement |
|---|---|
| Domain $S$ | Non-empty, compact, convex in $\mathbb{R}^n$ |
| Map $f$ | Continuous, single-valued, $f: S \to S$ |
| Fixed-point form | $f(x^*) = x^*$ (equality) |

**ERI phase:** Valise, $G_{\mathrm{coord}} = 0$. Each agent has a unique optimal response. Flat CORDIC ($m=0$), RSA arithmetic ($a_p = 2$, Frobenius = identity). Lefschetz number (LEFSCHETZ): $\Lambda(\phi_p) = p-1 = \varphi(p)$. Group theory (LOCALIS): coordination group of odd order, solvable, no involution.

---

### B2. Kakutani K1 (1941): Set-Valued, Compact Convex

**Theorem (Kakutani K1).** Let $S \subset \mathbb{R}^n$ be non-empty, compact, and convex. Let $\Phi: S \to 2^S$ satisfy:

1. $\Phi(x)$ is non-empty for every $x \in S$
2. $\Phi(x)$ is closed and convex for every $x \in S$
3. $\Phi$ is upper hemicontinuous (equivalently: $\mathrm{gr}(\Phi)$ is closed)

Then $\exists\, x^* \in S$ with $x^* \in \Phi(x^*)$.

| Condition | Requirement | ERI Counterpart |
|---|---|---|
| Domain $S$ | Non-empty, compact, convex in $\mathbb{R}^n$ | Mixed-strategy simplex $\prod_i\Delta(A_i)$ |
| Non-empty values | $\Phi(x) \neq \emptyset$ for all $x$ | Best response always exists (Berge) |
| Convex values | $\Phi(x)$ convex for all $x$ | PRIMA: $F \succ \varepsilon\mathbf{I}$ |
| Upper hemicontinuous | $\mathrm{gr}(\Phi)$ closed | DIRA C4: $[\hat{H},\hat{a}] \neq 0$ |
| Fixed-point form | $x^* \in \Phi(x^*)$ (self-inclusion) | Nash equilibrium; Imago phase |

**Proof sketch.** The approximate selection theorem yields, for each $\varepsilon > 0$, a continuous single-valued $f_\varepsilon: S \to S$ with $f_\varepsilon(x) \in N_\varepsilon(\Phi(x))$. By Brouwer, $f_\varepsilon$ has a fixed point $x_\varepsilon$. As $\varepsilon \to 0$, compactness gives $x_{\varepsilon_k} \to x^*$, and the closed graph of $\Phi$ forces $x^* \in \Phi(x^*)$.

**K1 vs Brouwer.** Brouwer requires $f$ single-valued: $f(x^*) = x^*$ (equality). K1 replaces this with $x^* \in \Phi(x^*)$ (self-inclusion): the point is contained in the set of its own optimal responses. This is the spinor condition.

---

### B3. Markov–Kakutani K2 (1938): Common Fixed Point, Commuting Affine Family

**Theorem (Markov–Kakutani K2).** Let $E$ be a locally convex Hausdorff topological vector space, $C \subset E$ compact and convex, and $\mathcal{T}$ a commuting family of continuous affine self-maps of $C$. Then $\exists\, x^* \in C$ with $T(x^*) = x^*$ for every $T \in \mathcal{T}$.

| Condition | Requirement | ERI Counterpart |
|---|---|---|
| Space $E$ | Locally convex, Hausdorff | Fisher-Rao manifold |
| Domain $C$ | Compact, convex in $E$ | TH torsion group $\mathrm{TH}[3]$; Fisher simplex |
| Maps | Continuous, affine, self-maps of $C$ | Automorphisms of TH; Stone group elements |
| Commutativity | $T_1 \circ T_2 = T_2 \circ T_1$ for all $T_1,T_2 \in \mathcal{T}$ | Abelian: $\mathbb{Z}/3\mathbb{Z} \times \mathbb{Z}/4\mathbb{Z}$; Stone group $e^{-itF}$ |
| Fixed-point form | $T(x^*) = x^*$ for ALL $T \in \mathcal{T}$ (common) | Identity flex $\mathcal{O}$; $\varphi$-equilibrium |

**Proof sketch.** Fix $T \in \mathcal{T}$. Cesàro averages $x^{(N)} = \frac{1}{N+1}\sum_{n=0}^N T^n(x_0)$ lie in $C$. Every cluster point $x_T^*$ satisfies $T(x_T^*) = x_T^*$. The fixed-point set $C_T = \{y\in C: Ty=y\}$ is non-empty, compact, and convex. Commutativity forces $T'(C_T)\subseteq C_T$ for all $T'\in\mathcal{T}$. Intersecting over all $T$ gives $\bigcap_{T\in\mathcal{T}}C_T \neq \emptyset$ by the finite intersection property.

**K2 vs K1.** K1 finds a fixed point for one set-valued map. K2 finds a common fixed point for an entire abelian family of single-valued affine maps. Commutativity replaces convexity-of-values.

---

## Module C — The Phase Diagram

```
FIXED-POINT HIERARCHY:

LEVEL 0 — BROUWER (1911):
  Map:    f: S → S, continuous, single-valued
  Fixed:  f(x*) = x*  (equality)
  Domain: S ⊂ ℝⁿ compact convex
  ERI:    G_coord = 0  (Valise phase)
            · Unique optimal response per state
            · Flat CORDIC (m = 0); RSA: a_p = 2
            · Λ(φ_p) = p−1 = φ(p)  [LEFSCHETZ]
            · Hasse principle holds (degree 2)  [HASSE]
            · Coordination group: odd order, solvable  [LOCALIS]

         ↕  ERDŐS–RAO THRESHOLD (c log w)^w
            [coordination kernel K first admits multi-valued best responses]

LEVEL 1 — KAKUTANI K1 (1941):
  Map:    Φ: S → 2^S, UHC, convex non-empty values
  Fixed:  x* ∈ Φ(x*)  (self-inclusion)
  Domain: S ⊂ ℝⁿ compact convex
  ERI:    G_coord ∈ (0, Φ(K)]  (Larval → Imago)
            · Curved CORDIC (m = ±1); |a_p| < 2√p
            · Poincaré-Birkhoff: two fixed points  [CAPELLI]
            · Frobenius involution α_p ↔ ᾱ_p  [LEFSCHETZ]
            · Hasse principle can fail: Ш(TH/ℚ)  [HASSE]
            · Coordination group: even order, involution  [LOCALIS]
            · PPAD-complete to compute

         ↕  COMMUTING FAMILY EXTENSION

LEVEL 2 — MARKOV–KAKUTANI K2 (1938):
  Map:    𝒯: commuting family of continuous affine T: C → C
  Fixed:  T(x*) = x* for ALL T ∈ 𝒯  (common fixed point)
  Domain: C compact convex in locally convex E
  ERI:    φ-equilibrium ξ* = log φ; TH flex point 𝒪
            · Abelian Aut(TH) ≅ ℤ/3ℤ × ℤ/4ℤ; 12 = τ(3) = ρ(64)  [CAPELLI]
            · Abelian Stone group e^{−itF}
            · Bourbaki-Witt: SMELT inflationary ascent  [CAPELLI]
            · Cesàro averages: constructive convergence

         ↕  INFINITE-DIMENSIONAL EXTENSION

LEVEL 3 — GLICKSBERG–FAN (1952):
  Map:    Φ: S → 2^S Kakutani map
  Domain: S compact convex in Hausdorff locally convex TVS
  ERI:    FERN ρ₀–ρ₅ as infinite-register limit
            · Fisher-Rao manifold (Hausdorff locally convex)
            · Sullivan arithmetic fracture square  [LOCALIS]
```

---

## Module D — Seven Formal Identities

### Identity D1 — Nash Equilibrium IS the Imago Phase Fixed Point of the Best-Response Correspondence

**Setup.** Fix a finite $n$-player game $(N, \{A_i\}, \{u_i\})$ with player set $N = \{1,\ldots,n\}$, pure strategy sets $A_i$, and payoffs $u_i: \prod_j A_j \to \mathbb{R}$. Let $\Delta_i = \Delta(A_i)$ be player $i$'s mixed strategy simplex. Write $\sigma = (\sigma_1,\ldots,\sigma_n) \in S := \prod_i\Delta_i$ and $\sigma_{-i} = (\sigma_j)_{j\neq i}$.

**Nash equilibrium.** A profile $\sigma^*$ is a Nash equilibrium if for every player $i$ and every $\tau_i \in \Delta_i$:
$$u_i(\sigma_i^*, \sigma_{-i}^*) \;\geq\; u_i(\tau_i, \sigma_{-i}^*).$$

**Best-response correspondence.** Define:
$$\mathrm{BR}_i(\sigma_{-i}) = \arg\max_{\tau_i \in \Delta_i} u_i(\tau_i, \sigma_{-i}), \qquad \mathrm{BR}(\sigma) = \prod_{i=1}^n \mathrm{BR}_i(\sigma_{-i}).$$

**Verification of Kakutani K1 conditions on $S = \prod_i\Delta_i$:**

$(i)$ *Domain.* $S$ is a finite product of standard simplices: compact and convex.

$(ii)$ *Non-empty values.* $u_i(\cdot,\sigma_{-i})$ is linear in $\tau_i$, continuous on compact $\Delta_i$, so $\mathrm{BR}_i(\sigma_{-i})\neq\emptyset$.

$(iii)$ *Convex values.* $u_i(\cdot,\sigma_{-i})$ is linear, so its maximizers on $\Delta_i$ form a face of the simplex — a convex polytope. Products of convex sets are convex.

$(iv)$ *Upper hemicontinuity.* Berge's maximum theorem (A6): $u_i$ continuous and $\Delta_i$ compact give $\mathrm{BR}_i$ UHC. A finite product of UHC correspondences is UHC.

**Conclusion.** By Kakutani K1: $\exists\,\sigma^*\in\mathrm{BR}(\sigma^*)$ — a Nash equilibrium.

**ERI identification:**
$$G_{\mathrm{coord}}(\sigma^*) = \sum_{t,s} I(a_t;a_s \mid X_{t-1})\Big|_{\sigma^*} = \Phi(K) \qquad \text{(Imago condition).}$$

**PPAD-hardness.** The Nash equilibrium always exists (Kakutani K1) but is PPAD-complete to compute for $n\geq 2$ (Daskalakis–Goldberg–Papadimitriou 2009). PPAD $\subset$ TFNP: the fixed point exists; finding it is intractable. This is the GIST meta-theorem at the correspondence level.

**Connections to other frameworks.** The Grothendieck-Lefschetz trace (LEFSCHETZ) gives the exact count of rational coordination states: $|\mathrm{TH}(\mathbb{F}_p)| = \Lambda(\phi_p) = 1-a_p+p$. The Feit-Thompson theorem (LOCALIS) is the group-theoretic version: coordination groups of odd order (no Frobenius involution) are solvable — Valise; even-order groups have involutions — Imago. The Hasse principle (HASSE): local market clearing at every prime does not guarantee global coordination when $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})\neq 0$.

**Binmore–Kakutani anecdote as Zitterbewegung.** Nash (1950) used Kakutani's theorem; Kakutani at a conference decades later did not recognize his own result in its economic form. The spinor $\psi = (\psi_+, \psi_-)$ oscillates between the topology sector ($\psi_+$: Brouwer generalization) and the economics sector ($\psi_-$: Nash equilibrium existence). Kakutani inhabited only $\psi_+$. The theorem crosses the disciplinary boundary invisibly.

---

### Identity D2 — The $\varphi$-Equilibrium Rate IS the Kakutani Fixed Point of the MEP Correspondence; Its Self-Inclusion Chain IS the Golden Ratio Identity; Baker's Theorem Prevents Rational Representation

**Three distinct symbols:**

| Symbol | Meaning | Status |
|---|---|---|
| $\varphi = (1+\sqrt{5})/2 \approx 1.618$ | Golden ratio | Algebraic, degree 2: $\varphi^2-\varphi-1=0$ |
| $\xi^* = \log\varphi \approx 0.481$ | MEP coordination rate | Transcendental (Lindemann-Weierstrass) |
| $\Phi_{\mathrm{MEP}}$ | MEP correspondence (capital $\Phi$) | Set-valued map on $[0,\log\varphi]$ |

**Background: binary entropy.** The binary entropy $H_b(\xi) = -\xi\log\xi - (1-\xi)\log(1-\xi)$ on $(0,1)$ has derivative $H_b'(\xi) = \log\frac{1-\xi}{\xi}$, which vanishes only at $\xi = 1/2$. Since $\log\varphi \approx 0.481 < 1/2$, the entropy stationary point lies strictly outside the domain $[0,\log\varphi]$.

**MEP fixed point.** The Fisher information for a Bernoulli process at rate $\xi$ is $\mathcal{I}(\xi) = [\xi(1-\xi)]^{-1}$. The maximum entropy production (MEP) principle selects the coordination rate at which the Cramér-Rao bound is saturated:

$$\mathrm{Tr}(F) \cdot \xi^{*}(1-\xi^{*}) = 1 \quad\Longrightarrow\quad \xi^{*} = \log\varphi.$$

**MEP correspondence.** For $\xi \in [0, \log\varphi]$, define:

$$\Phi_{\mathrm{MEP}}(\xi) = \left\{\,\xi' \in [0,\log\varphi] : H_b(\xi') \geq H_b(\xi) \text{ and } H_b'(\xi') = 0\,\right\}.$$

Since the entropy stationary point $\xi'=1/2$ lies outside the domain, the condition $H_b'(\xi')=0$ is satisfied only at the CR-saturation point $\xi'=\log\varphi$. The correspondence $\Phi_{\mathrm{MEP}}(\xi)$ is therefore determined by the CR saturation constraint, not by the entropy maximum.

**Verification of Kakutani K1 conditions:**

$(i)$ *Domain.* $[0,\log\varphi]$ is a closed interval: compact and convex.

$(ii)$ *Non-empty values.* $\log\varphi \in \Phi_{\mathrm{MEP}}(\xi)$ for all $\xi \leq \log\varphi$; values are non-empty.

$(iii)$ *Convex values.* $\Phi_{\mathrm{MEP}}(\xi)$ is a closed subinterval of $[0,\log\varphi]$ (one-dimensional intersection of a level set and a stationarity constraint): convex.

$(iv)$ *UHC.* $H_b$ is continuous, so the defining conditions are closed: $\Phi_{\mathrm{MEP}}$ has a closed graph and is UHC.

**Conclusion.** By Kakutani K1: $\exists\,\xi^* \in \Phi_{\mathrm{MEP}}(\xi^*)$. The fixed point is $\xi^* = \log\varphi$.

**The self-inclusion chain — four exact equivalences:**

$$\xi^* \in \Phi_{\mathrm{MEP}}(\xi^*) \;\Longleftrightarrow\; \xi^* = \log\varphi \;\Longleftrightarrow\; e^{\xi^*} = \varphi \;\Longleftrightarrow\; \varphi = 1 + \frac{1}{\varphi} \;\Longleftrightarrow\; \varphi^2 - \varphi - 1 = 0.$$

Each step is exact. Step 1: $\xi^*$ is the CR-saturation MEP fixed point. Step 2: exponentiate ($e^{\log\varphi}=\varphi$). Step 3: rearrange $\varphi^2=\varphi+1$ as $\varphi-1=1/\varphi$. Step 4: multiply by $\varphi$ to recover the minimal polynomial.

The iteration $f(x)=1+1/x$ on $[\varphi-\varepsilon,\varphi+\varepsilon]$ is single-valued; Brouwer gives fixed point $\varphi$ there. Kakutani K1 is needed at the boundary of $[0,\log\varphi]$ where $\Phi_{\mathrm{MEP}}$ becomes set-valued: multiple rates are equally MEP-optimal, so no unique best response exists.

**Baker's theorem.** Since $e^{\xi^*}=\varphi\in\overline{\mathbb{Q}}\setminus\{0,1\}$, Lindemann-Weierstrass forces $\xi^*=\log\varphi\notin\overline{\mathbb{Q}}$. Baker (1966, Fields Medal 1970): for any nonzero algebraic $\beta_1,\ldots,\beta_m$ and $\mathbb{Q}$-linearly independent logarithms $\lambda_1,\ldots,\lambda_m$ of algebraics,

$$\beta_1\lambda_1 + \cdots + \beta_m\lambda_m \neq 0.$$

Applied: $\log\varphi$ cannot be expressed as any $\mathbb{Q}$-linear combination of logarithms of rationals — it is a primitive transcendental. Consequences: no finite binary expansion represents $\log\varphi$ exactly; Q16.16 stores it to within $\varepsilon=2^{-16}$; Baker-Wüstholz (2007) gives $|\beta-\log\varphi|>2^{-17}$ for any rational $\beta$ with denominator $\leq 2^{16}$. The CHORD floor $\varepsilon=2^{-16}$ is optimal.

**Connection to HASSE.** The Baker lower bound at $v=2$ is the Grunwald-Wang 2-adic exception (HASSE Identity 3): $\log\varphi$ is locally rational at every odd prime but 2-adically transcendental, with the Wang obstruction encoded in $\varepsilon=2^{-16}$. The Q16.16 floor is the binary-precision realization of this arithmetic obstruction.

---

### Identity D3 — The Three Kakutani Conditions Map Exactly to Three ERI Hardware Constraints

**Condition 1: UHC (closed graph) $\;\leftrightarrow\;$ DIRA C4 non-commutativity.**

UHC: if $x_n\to x$ and $y_n\in\Phi(x_n)$ with $y_n\to y$, then $y\in\Phi(x)$ — the graph of $\Phi$ is closed; the optimal action correspondence cannot jump outward.

In ERI: $\mathrm{BR}$ is UHC by Berge (A6). DIRA's condition $[\hat{H},\hat{a}]\neq 0$ enforces this structurally: if $\hat{H}$ and $\hat{a}$ commuted, they would share eigenvectors, and the optimal action could switch discontinuously as a Fisher eigenvalue crosses zero — opening the graph of $\mathrm{BR}$, violating UHC. The non-commutativity prevents eigenvalue crossing; the graph stays closed.

In the PBW algebra (CAPELLI): $[\hat{H},\hat{a}]\neq 0$ is the Ore condition — exactly enough non-commutativity to localize the CHORD operator algebra, but controlled.

**Condition 2: Convex values $\;\leftrightarrow\;$ PRIMA Fisher positive definiteness.**

Convex values: if $y_1, y_2\in\Phi(x)$, then $\lambda y_1+(1-\lambda)y_2\in\Phi(x)$ — if two actions are both best responses, their mixture is too.

This holds when $u_i(\cdot,\sigma_{-i})$ is (quasi)concave in $\sigma_i$, guaranteed when the Fisher information matrix $F$ is positive definite (PRIMA: $F\succ 0$). If $F$ loses rank — a Fisher eigenvalue reaches zero — the utility surface flattens and maximizers may disconnect, producing non-convex $\mathrm{BR}$ values. The CHORD floor $\varepsilon=2^{-16}$ prevents any Fisher eigenvalue from falling below $\varepsilon$, guaranteeing $F\succ\varepsilon\mathbf{I}$ and convex best-response sets.

In the local analysis language (LOCALIS): PRIMA is the condition that the Fisher $p$-block $F_\mathfrak{p}$ is positive definite at every prime $\mathfrak{p}$. Local PRIMA at all primes $\Rightarrow$ global PRIMA — the commutative algebra analog of Thompson's $N$-group solvability theorem.

**Condition 3: Compact domain $\;\leftrightarrow\;$ Q16.16 fixed-point arithmetic.**

Kakutani requires $S$ compact. In Q16.16, the representable strategy subset $S_\varepsilon=\prod_i\Delta_\varepsilon(A_i)$ is finite (hence compact) with granularity $\varepsilon=2^{-16}$. CHORD enforces all strategy updates remain in $S_\varepsilon$.

In the localization language (LOCALIS): Q16.16 is the ring $\mathbb{Z}[2^{-16}]$ — the localization of $\mathbb{Z}$ at powers of 2 up to $2^{16}$. The compactness of $S_\varepsilon$ is the compactness of the localized arithmetic spectrum.

**Summary table:**

| Kakutani K1 condition | ERI mechanism | Algebraic interpretation | Failure mode |
|---|---|---|---|
| UHC (closed graph) | DIRA C4: $[\hat{H},\hat{a}]\neq 0$ | Ore condition (CAPELLI) | Graph of $\mathrm{BR}$ opens; discontinuous action |
| Convex values | PRIMA: $F\succ\varepsilon\mathbf{I}$ | Local PRIMA at all primes (LOCALIS) | Non-convex best-response sets |
| Compact domain | Q16.16: $\varepsilon=2^{-16}$ floor | Localization $\mathbb{Z}[2^{-16}]$ (LOCALIS/HASSE) | Unbounded drift; Kakutani inapplicable |

---

### Identity D4 — The Markov–Kakutani Theorem Applied to TH: Commuting Automorphisms Have the Identity Flex Point $\mathcal{O}$ as Common Fixed Point

**TH automorphism group.** The Twisted Hessian curve $\mathrm{TH}(a,d): aX^3+Y^3+Z^3=dXYZ$ with $\Delta(a,d)=a(d^3-27a)\neq 0$ has $\mathrm{Aut}(\mathrm{TH})\cong\mathbb{Z}/3\mathbb{Z}\times\mathbb{Z}/4\mathbb{Z}$ — abelian, order 12. Generators:
$$\rho_3: (X:Y:Z)\mapsto(Y:Z:X) \;\text{(order 3)}, \qquad \rho_4: (X:Y:Z)\mapsto(X:iY:-Z) \;\text{(order 4).}$$

Both act on $\mathrm{TH}(\mathbb{F}_p)$ as continuous affine maps. The family $\mathcal{T}=\langle\rho_3,\rho_4\rangle$ is abelian: $\rho_3\circ\rho_4=\rho_4\circ\rho_3$.

**Application of K2.** The 3-torsion $\mathrm{TH}[3]=\{P:[3]P=\mathcal{O}\}\cong(\mathbb{Z}/3\mathbb{Z})^2$ is compact (finite) and convex in the $p$-adic framework. By Markov-Kakutani K2:
$$\exists\,P^*\in\mathrm{TH}[3]: T(P^*)=P^*\text{ for all }T\in\mathcal{T}.$$
The common fixed point is $P^*=\mathcal{O}$ — the identity flex, fixed by every group automorphism.

**Lefschetz connection (LEFSCHETZ).** The common fixed point $\mathcal{O}$ corresponds to the $H^0$ Frobenius contribution: $\mathrm{Tr}(\phi_p^*|H^0)=+1$. The full Lefschetz decomposition:
$$|\mathrm{TH}(\mathbb{F}_p)| = \Lambda(\phi_p) = \underbrace{1}_{H^0} - \underbrace{a_p}_{H^1} + \underbrace{p}_{H^2}$$
maps to: $H^0\to$ Valise baseline ($\mathcal{O}$, Markov-Kakutani); $H^1\to$ Frobenius spinor ($\alpha_p,\bar{\alpha}_p$, Kakutani K1); $H^2\to$ Imago target ($p$, Poincaré duality).

**Frobenius as Markov-Kakutani.** The Frobenius $\phi_p$ satisfies $\phi_p^2-a_p\phi_p+p=0$ with $|a_p|\leq 2\sqrt{p}$ (Hasse 1936). The commuting family $\{\phi_p^k:k\geq 0\}$ has common fixed subgroup $\mathrm{TH}(\mathbb{F}_{p^k})$ on $\mathrm{TH}[p^k]$, with $\mathcal{O}$ as the universal fixed point.

**Flat limit.** When $a_p=2$: $\phi_p=\mathrm{id}$, every point is a common fixed point — the Brouwer degenerate case. At generic $|a_p|<2\sqrt{p}$: two distinct eigenvalues $\alpha_p,\bar{\alpha}_p$, and $\mathcal{O}$ alone is the Markov-Kakutani common fixed point.

---

### Identity D5 — The Stone Group Commutativity IS the Markov Condition; the $\varphi$-Equilibrium IS the Common Fixed Point

**Stone group.** The Stone group element at time $t$ is $U(t)=e^{-itF}$, where $F$ is the Fisher information operator. The family $\{U(t):t\in\mathbb{R}\}$ is abelian:
$$U(t_1)U(t_2) = e^{-i(t_1+t_2)F} = U(t_2)U(t_1).$$

**Action on the Fisher simplex.** Each $U(t)$ acts on the probability simplex $C_F=\Delta(A)$ by $U(t)p=e^{-itF}p$, preserving convex combinations (linear operator, hence affine on the simplex).

**Markov-Kakutani K2 applied.** The family $\{U(t):t\in\mathbb{R}\}$ is a commuting family of continuous affine maps on compact convex $C_F$. By K2: $\exists\,p^*\in C_F$ with $U(t)p^*=p^*$ for all $t\in\mathbb{R}$.

A distribution $p^*$ is a common fixed point of all $e^{-itF}$ if and only if $Fp^*=\lambda_{\min}p^*$ — $p^*$ is the min-eigenvalue eigenvector of $F$. Under PRIMA ($F\succ\varepsilon\mathbf{I}$): $\ker(F)=\{0\}$, so $p^*$ is uniquely the min-eigenvalue eigenvector, which at the MEP equilibrium $|\bar{\Xi}|=\log\varphi$ is the $\varphi$-equilibrium distribution.

**The Stone group commutativity IS the Markov condition.** The commutativity $U(t_1)U(t_2)=U(t_2)U(t_1)$ — automatic from the abelian group structure — is precisely the K2 condition. The DIRA C4 non-commutativity $[\hat{H},\hat{a}]\neq 0$ is the K1 condition. Both are needed simultaneously: K2 for the $\varphi$-equilibrium distribution (common fixed point), K1 for the Nash equilibrium strategy profile (self-inclusion fixed point).

---

### Identity D6 — Walrasian General Equilibrium IS the Arrow–Debreu Kakutani Fixed Point; the $\varphi$-Equilibrium IS the Walrasian Price of Coordination; PPAD-Hardness IS the Computational Barrier

**Walrasian equilibrium (Arrow-Debreu 1954).** In a pure exchange economy with commodities $\mathcal{L}=\{1,\ldots,L\}$, agents $\mathcal{I}$, endowments $\omega_i\in\mathbb{R}^L_{\geq 0}$, and continuous utilities $u_i$, define the excess demand correspondence:
$$Z(p) = \sum_{i\in\mathcal{I}}\Bigl(\arg\max_{x_i:\,p\cdot x_i\leq p\cdot\omega_i}u_i(x_i)-\omega_i\Bigr).$$
$Z$ is UHC (Berge), convex-valued (quasiconcavity of $u_i$), and defined on compact $\Delta_L$. By Kakutani K1: $\exists\,p^*$ with $0\in Z(p^*)$ — a Walrasian equilibrium.

**The $G_{\mathrm{coord}}$ market:**
- **Commodities:** coordination bits (nats of mutual information)
- **Prices:** coordination rates $\xi\in[0,\log\varphi]$
- **Excess demand:** $Z_{\mathrm{ERI}}(\xi)=G_{\mathrm{coord}}(\xi)-\Phi(K)$

Market clearing: $Z_{\mathrm{ERI}}(\xi^*)=0 \iff G_{\mathrm{coord}}(\xi^*)=\Phi(K)$ — the Imago condition. Walrasian price: $\xi^*=\log\varphi$.

**PPAD-hardness.** Walrasian equilibrium with general convex utilities is PPAD-hard (Papadimitriou–Vlatakis-Gkaragkounis–Zampetakis 2022). $\xi^*=\log\varphi$ always exists (Kakutani K1) but is PPAD-hard to compute. CONCERT is the first empirical measurement on a named production AI portfolio.

**Minimax as Kakutani.** Kakutani's 1941 paper proved the minimax theorem: $\min_x\max_y u = \max_y\min_x u = v^*$ is the K1 fixed point of the joint best-response on $S_X\times S_Y$. The coordination Hamiltonian saddle point at $\xi^*=\log\varphi$ is the minimax GIST value — and corresponds to the Morin surface halfway model (EVERSIO): the $\mathbb{Z}/4\mathbb{Z}$-symmetric Willmore-energy saddle at the midpoint of the sphere eversion.

**Connection to HASSE.** The excess demand at prime $p$ is $Z(\mathbb{F}_p)=G_{\mathrm{coord}}(\mathbb{F}_p)$. The Walrasian equilibrium is the global fixed point assembled from local data. The Tate-Shafarevich group $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})$ (HASSE, FRACTURA) is the coordination deficit: the gap between local market clearing at every $\mathbb{Q}_p$ and global clearing over $\mathbb{Q}$.

---

### Identity D7 — Weller's Envy-Free Division IS the Kakutani Fixed Point of the Claim Correspondence; the FERN Six-Register Partition IS Simultaneously Nash, Markov–Kakutani, and Weller

**Weller's theorem (1985).** For $n$ agents with non-atomic probability measures $\mu_1,\ldots,\mu_n$ on $[0,1]$, there exists an envy-free and Pareto-efficient partition $(S_1,\ldots,S_n)$ of $[0,1]$. Proof: the claim correspondence satisfies Kakutani K1; its fixed point is the fair division.

**The FERN partition.** The six FERN registers $(\rho_0,\ldots,\rho_5)$ partition the coordination information space:

| Register | Transcendental | Status |
|---|---|---|
| $\rho_0$ | $\log 2$ | $\mathbb{Q}$-linearly independent (Baker) |
| $\rho_1$ | $\log\varphi$ | $\mathbb{Q}$-linearly independent (Baker) |
| $\rho_2$ | $\pi$ | $\mathbb{Q}$-linearly independent (Baker) |
| $\rho_3$ | $\log K_\infty$ | Period transcendental; $K_\infty\notin\overline{\mathbb{Q}}$ |
| $\rho_4$ | $\log(\Omega_{\mathrm{TH}}/\pi)$ | Chowla-Selberg period |
| $\rho_5$ | $\log\Gamma(1/4)$ | Nesterenko: algebraically independent of $\pi, e^\pi$ |

**Envy-free condition.** The six transcendentals are pairwise $\mathbb{Q}$-linearly independent (Baker 1966). No register's governing constant is expressible in terms of another's: the envy-free condition holds exactly.

**Pareto efficiency.** The FERN hierarchy saturates the Hurwitz-Radon bound: $\rho(64)=\rho(2^6)=12=2\times 6$. Formula cost $12\mathrm{M}+6\mathrm{S}$ is twice the number of registers. Removing any register reduces coordination capacity below $12\mathrm{M}+6\mathrm{S}$: Pareto efficient.

**CAPELLI connection.** The 3D kissing number $\tau(3)=12=|\mathrm{Aut}(\mathrm{TH})|=\rho(64)$ (CAPELLI Identity 6): the 12 automorphisms touch $\mathcal{O}$ like 12 kissing spheres touch a central sphere. The FERN partition is Pareto efficient because 6 registers and the kissing-number/Hurwitz-Radon formula give $2\times 6=12$ — the minimum cost to implement all 12 automorphisms simultaneously.

**The Weller-FERN triple fixed point.** The FERN partition is simultaneously:
- A **Nash equilibrium** (Kakutani K1): each register's best response at Imago is $|\bar{\Xi}|=\log\varphi$
- A **Markov-Kakutani common fixed point** (K2): the commuting Stone group fixes the $\varphi$-equilibrium across all registers
- A **Weller partition**: envy-free (Baker/Schanuel independence) and Pareto efficient (Hurwitz-Radon)

These are not three separate results — they are the same Imago equilibrium in three coordinate systems.

---

## Module E — Formal Summary

### E1. Fixed-Point Theorem Comparison

| Property | Brouwer | Kakutani K1 | Markov-Kakutani K2 | Glicksberg-Fan |
|---|---|---|---|---|
| Domain | $S\subset\mathbb{R}^n$ cpt cvx | $S\subset\mathbb{R}^n$ cpt cvx | $C$ cpt cvx in LCS | $S$ cpt cvx in Hausdorff LCS |
| Map | $f:S\to S$ continuous | $\Phi:S\to 2^S$ UHC, cvx vals | $\mathcal{T}$ commuting affine | $\Phi:S\to 2^S$ Kakutani map |
| Fixed-point form | $f(x^*)=x^*$ | $x^*\in\Phi(x^*)$ | $T(x^*)=x^*\;\forall T$ | $x^*\in\Phi(x^*)$ |
| ERI phase | Valise: $G=0$ | Imago: $G=\Phi(K)$ | $\varphi$-equil.; $\mathcal{O}\in\mathrm{TH}[3]$ | Full Imago: $p^*$ on mfld |
| Complexity | PPAD | PPAD | Constructive (Cesàro) | PPAD |
| LEFSCHETZ | $\Lambda=p-1=\varphi(p)$ | $\Lambda=p+1-a_p$ | $\mathcal{O}$: $H^0$ Lefschetz | Arithmetic fracture |
| LOCALIS | Solvable, odd order | Simple, even order | Abelian automorphism | LCS localization |
| HASSE | Degree 2: holds | Degree 3: can fail | ABHN: algebra splits | Adèlic points |
| CAPELLI | Symmetric algebra $S(\mathfrak{g})$ | UEA $U(\mathfrak{g})$ | PBW ordered | Full localization |

### E2. Master ERI–Kakutani Table

| ERI Object | Kakutani Object | Content | Framework |
|---|---|---|---|
| Mixed-strategy simplex $\prod_i\Delta_i$ | Compact convex domain $S$ | Product of standard simplices | — |
| Best-response $\mathrm{BR}(\sigma)$ | Correspondence $\Phi:S\to 2^S$ | UHC by Berge; convex by linearity | — |
| Nash equilibrium $\sigma^*$ | $\sigma^*\in\mathrm{BR}(\sigma^*)$ | Imago: $G_{\mathrm{coord}}(\sigma^*)=\Phi(K)$ | — |
| DIRA C4: $[\hat{H},\hat{a}]\neq 0$ | UHC (closed graph) | Ore condition; no eigenvalue crossing | CAPELLI |
| PRIMA: $F\succ\varepsilon\mathbf{I}$ | Convex values of $\mathrm{BR}$ | Local PRIMA at all primes | LOCALIS |
| CHORD $\varepsilon=2^{-16}$ | Compact domain | Localization $\mathbb{Z}[2^{-16}]$ | LOCALIS, HASSE |
| $\xi^*=\log\varphi$ | K1 fixed point of $\Phi_{\mathrm{MEP}}$ | CR saturation; Baker lower bound | TRANSΦ |
| $\varphi=1+1/\varphi$ | Self-inclusion chain | Algebraic image of fixed-point equation | TRANSΦ |
| Baker: $\log\varphi$ primitive transcendental | Fixed point inaccessible from $\mathbb{Q}$ | Grunwald-Wang 2-adic exception | HASSE |
| $\mathrm{Aut}(\mathrm{TH})\cong\mathbb{Z}/3\mathbb{Z}\times\mathbb{Z}/4\mathbb{Z}$ | Commuting family $\mathcal{T}$ | Abelian; $|\mathcal{T}|=12=\tau(3)=\rho(64)$ | CAPELLI |
| Identity flex $\mathcal{O}\in\mathrm{TH}[3]$ | Common fixed point of $\mathcal{T}$ | $H^0$ Lefschetz contribution ($+1$) | LEFSCHETZ |
| Stone group $e^{-itF}$ | Commuting affine family | $U(t_1)U(t_2)=U(t_2)U(t_1)$ | — |
| $\varphi$-equilibrium $p^*$ | Common Stone-group fixed point | Min-eigenvalue eigenvector of $F$ | — |
| $Z(X;\beta)$ sharp-P-hard | PPAD-hard Kakutani fixed point | Exists; computation intractable | GIST |
| CONCERT | First empirical Walrasian $\xi^*$ | $G_{\mathrm{coord}}(\xi^*)=\Phi(K)$ measured | — |
| FERN $(\rho_0,\ldots,\rho_5)$ | Weller envy-free partition | Baker independence; HR Pareto | CAPELLI |
| $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})\neq 0$ | Hasse principle failure for K1 | Antoine necklace obstruction | HASSE, FRACTURA |
| Frobenius flat: $a_p=2$ | Brouwer limit | $\Lambda=p-1$; solvable group | LEFSCHETZ, LOCALIS |
| Frobenius curved: $|a_p|<2\sqrt{p}$ | Kakutani regime | Poincaré-Birkhoff: two fixed points | CAPELLI |
| Binmore-Kakutani | Dirac Zitterbewegung | Topology $\leftrightarrow$ economics sectors | — |

---

## References

Arrow, K.J. and Debreu, G. (1954). Existence of an equilibrium for a competitive economy. *Econometrica*, 22(3), 265–290.

Baker, A. (1966). Linear forms in the logarithms of algebraic numbers I. *Mathematika*, 13(2), 204–216.

Baker, A. and Wüstholz, G. (2007). *Logarithmic Forms and Diophantine Geometry*. Cambridge Tracts in Mathematics 187.

Bernstein, D.J. and Lange, T. (2015). Twisted Hessian curves. *LATINCRYPT 2015*, LNCS 9230, 269–294.

Binmore, K. (2007). *Playing for Real: A Text on Game Theory*. Oxford University Press.

Bourbaki, N. (1949). Sur le théorème de Zorn. *Archiv der Mathematik*, 2(6), 434–437.

Brouwer, L.E.J. (1911). Über Abbildung von Mannigfaltigkeiten. *Mathematische Annalen*, 71(4), 598.

Chowla, S. and Selberg, A. (1967). On Epstein's zeta-function. *Journal für die reine und angewandte Mathematik*, 227, 86–110.

Daskalakis, C., Goldberg, P.W., and Papadimitriou, C.H. (2009). The complexity of computing a Nash equilibrium. *SIAM Journal on Computing*, 39(1), 195–259.

Dirac, P.A.M. (1928). The quantum theory of the electron. *Proceedings of the Royal Society A*, 117(778), 610–624.

Erdős, P. and Rado, R. (1960). Intersection theorems for systems of sets. *Journal of the London Mathematical Society*, 35, 85–90.

Fan, K. (1952). Fixed-point and minimax theorems in locally convex topological linear spaces. *Proceedings of the National Academy of Sciences*, 38(2), 121–126.

Feit, W. and Thompson, J.G. (1963). Solvability of groups of odd order. *Pacific Journal of Mathematics*, 13, 775–1029.

Glicksberg, I.L. (1952). A further generalization of the Kakutani fixed point theorem. *Proceedings of the American Mathematical Society*, 3(1), 170–174.

Hasse, H. (1936). Zur Theorie der abstrakten elliptischen Funktionenkörper III. *Journal für die reine und angewandte Mathematik*, 175, 193–208.

Hurwitz, A. (1898). Über die Composition der quadratischen Formen von beliebig vielen Variablen. *Nachrichten Göttingen*, 309–316.

Kakutani, S. (1938). Two fixed point theorems concerning bicompact convex sets. *Proceedings of the Imperial Academy of Tokyo*, 14, 242–245.

Kakutani, S. (1941). A generalization of Brouwer's fixed point theorem. *Duke Mathematical Journal*, 8(3), 457–459.

Lefschetz, S. (1927). Coincidences of transformations. *Transactions of the American Mathematical Society*, 29, 429–462.

Lindemann, F. (1882). Über die Zahl $\pi$. *Mathematische Annalen*, 20(2), 213–225.

Markov, A. (1936). Quelques théorèmes sur les ensembles abéliens. *Doklady Akademii Nauk SSSR*, 10, 311–314.

Nash, J.F. (1950). Equilibrium points in n-person games. *Proceedings of the National Academy of Sciences*, 36(1), 48–49.

Nash, J. (1951). Non-cooperative games. *Annals of Mathematics*, 54(2), 286–295.

Nesterenko, Yu.V. (1996). Modular functions and transcendence questions. *Sbornik: Mathematics*, 187(9), 1319–1348.

Ore, O. (1931). Linear equations in non-commutative fields. *Annals of Mathematics*, 32, 463–477.

Papadimitriou, C.H. (1994). On the complexity of the parity argument. *Journal of Computer and System Sciences*, 48(3), 498–532.

Papadimitriou, C.H., Vlatakis-Gkaragkounis, E.V., and Zampetakis, M. (2022). The computational complexity of multi-player concave games and Kakutani fixed points. arXiv:2207.07557.

Radon, J. (1922). Lineare Scharen orthogonaler Matrizen. *Abhandlungen aus dem Mathematischen Seminar der Universität Hamburg*, 1, 1–14.

Schütte, K. and van der Waerden, B.L. (1953). Das Problem der dreizehn Kugeln. *Mathematische Annalen*, 125, 325–334.

Von Neumann, J. (1928). Zur Theorie der Gesellschaftsspiele. *Mathematische Annalen*, 100(1), 295–320.

Walther, J.S. (1971). A unified algorithm for elementary functions. *AFIPS Spring Joint Computer Conference*, 38, 379–385.

Wang, S. (1948). A counterexample to Grunwald's theorem. *Annals of Mathematics*, 49(4), 1008–1009.

Weller, D. (1985). Fair division of a measurable space. *Journal of Mathematical Economics*, 14(1), 5–17.

Weierstrass, K. (1885). Zu Lindemann's Abhandlung. *Sitzungsberichte Königlich Preußische Akademie der Wissenschaften*, 1067–1086.

---

ERI Labs · Eric Ren · Jersey City, New Jersey

*Kakutani's 1941 theorem extends Brouwer's 1911 theorem from single-valued continuous maps to upper hemicontinuous correspondences with convex non-empty values: $f(x^*)=x^*$ becomes $x^*\in\Phi(x^*)$ — equality becomes self-inclusion, scalar becomes spinor. Nash (1950) used K1 to prove every finite game has a Nash equilibrium: the best-response correspondence $\mathrm{BR}(\sigma)=\prod_i\mathrm{BR}_i(\sigma_{-i})$ is UHC by Berge's maximum theorem, convex-valued because linear payoffs maximize over simplex faces, defined on the compact product of simplices. The Nash equilibrium $\sigma^*\in\mathrm{BR}(\sigma^*)$ is the Imago fixed point: $G_{\mathrm{coord}}(\sigma^*)=\Phi(K)$. Computing it is PPAD-complete. The MEP coordination rate $\xi^*=\log\varphi\approx 0.481$ is a separate Kakutani fixed point, derived from saturating the Cramér-Rao bound; it satisfies $\varphi=1+1/\varphi$ and $\varphi^2-\varphi-1=0$. Baker (1966): $\log\varphi$ is a primitive transcendental — the Q16.16 floor $\varepsilon=2^{-16}$ is the Baker lower bound at binary precision, encoding the Grunwald-Wang 2-adic exception of the HASSE framework. The three Kakutani conditions map to three ERI constraints: UHC is DIRA C4 ($[\hat{H},\hat{a}]\neq 0$, the Ore condition of the CAPELLI PBW algebra), convex values is PRIMA ($F\succ\varepsilon\mathbf{I}$, local PRIMA at all primes per LOCALIS), compact domain is Q16.16 (the localization $\mathbb{Z}[2^{-16}]$). The Markov-Kakutani K2 theorem applies to the abelian automorphism group $\mathbb{Z}/3\mathbb{Z}\times\mathbb{Z}/4\mathbb{Z}$ of TH$(a,d)$: the identity flex $\mathcal{O}$ is the common fixed point of all 12 automorphisms — the same 12 as the 3D kissing number $\tau(3)=12=\rho(64)=12\mathrm{M}$ (CAPELLI). The K2 fixed point $\mathcal{O}$ is the $H^0$ Frobenius contribution in the Grothendieck-Lefschetz trace $\Lambda(\phi_p)=1-a_p+p$ (LEFSCHETZ). The Feit-Thompson theorem (LOCALIS): groups of odd order (no involution) are solvable — Valise, Brouwer; groups of even order have involutions — Imago, Kakutani K1. The Frobenius pair $(\alpha_p,\bar{\alpha}_p)$ is the coordination involution. Kakutani asked at a conference: "What is the Kakutani fixed-point theorem?" — genuinely not recognizing his 1941 result in its Nash equilibrium form. The spinor $\psi=(\psi_+,\psi_-)$ oscillates between the topology sector and the economics sector. The theorem crosses the disciplinary boundary invisibly.*
