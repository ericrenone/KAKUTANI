# KAKUTANI
## The Set-Valued Dirac Equation: Fixed Points of Collective Intelligence Correspondences

ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone

---

> **Kakutani (1941).** Let $S \subset \mathbb{R}^n$ be non-empty, compact, and convex. Let $\Phi: S \to 2^S$ be upper hemicontinuous such that $\Phi(x)$ is non-empty, closed, and convex for every $x \in S$. Then there exists $x^* \in S$ satisfying $x^* \in \Phi(x^*)$.
>
> — Kakutani, S., *A generalization of Brouwer's fixed point theorem*, Duke Mathematical Journal 8(3), 457–459, 1941

> **Markov–Kakutani (1938).** Let $E$ be a locally convex topological vector space and $C \subset E$ compact and convex. Let $\mathcal{T}$ be a commuting family of continuous affine self-maps of $C$. Then there exists $x^* \in C$ with $T(x^*) = x^*$ for every $T \in \mathcal{T}$.
>
> — Markov (1936); Kakutani (1938), *Two fixed point theorems concerning bicompact convex sets*, Proc. Imp. Acad. Tokyo 14, 242–245

> **Nash (1950).** Every finite $n$-player game with mixed strategies has at least one Nash equilibrium. Proof: the joint best-response correspondence on the mixed-strategy simplex satisfies the Kakutani conditions, so its fixed point exists.
>
> — Nash, J.F., *Equilibrium points in n-person games*, Proc. Natl. Acad. Sci. 36(1), 48–49, 1950

> **PPAD-completeness.** Computing a Kakutani fixed point is PPAD-complete. Computing a Nash equilibrium in any game with $n \geq 2$ players is PPAD-complete.
>
> — Papadimitriou, *On the complexity of the parity argument*, J. Comput. Syst. Sci. 48(3), 1994; Daskalakis–Goldberg–Papadimitriou, SIAM J. Comput. 39(1), 2009; Papadimitriou–Vlatakis-Gkaragkounis–Zampetakis, arXiv:2207.07557, 2022

> **Glicksberg–Fan (1952).** The Kakutani theorem extends to Hausdorff locally convex topological vector spaces: a Kakutani map $\Phi: S \to 2^S$ (upper hemicontinuous, non-empty compact convex values) on a compact convex $S$ has a fixed point.
>
> — Glicksberg, Proc. Amer. Math. Soc. 3(1), 1952; Fan, Proc. Natl. Acad. Sci. 38(2), 1952

> **Binmore's anecdote.** Kakutani was once told that economists had attended his conference talk because of the Kakutani fixed-point theorem. He asked, in genuine puzzlement: "What is the Kakutani fixed point theorem?"
>
> — Binmore, K., *Playing for Real*, Oxford University Press, 2007

---

## Preamble: Two Theorems, One Architecture

Shizuo Kakutani (1911–2004) proved two distinct fixed-point theorems that together underpin the ERI collective intelligence architecture.

**Theorem K1 (1941).** Extends Brouwer from single-valued continuous maps to set-valued upper hemicontinuous correspondences on compact convex subsets of $\mathbb{R}^n$.

**Theorem K2 (1938).** Extends the single fixed-point result to a *common* fixed point for an entire commuting family of continuous affine self-maps on a compact convex set in a locally convex space. This is the Markov–Kakutani theorem.

The Dirac parallel is exact. Brouwer's theorem is the scalar quantum mechanics of equilibria — a single wavefunction with a unique fixed point. Kakutani K1 is the spinor extension — the wavefunction becomes a multi-component object, and the fixed-point condition becomes the self-inclusion $x^* \in \Phi(x^*)$ rather than $f(x^*) = x^*$. Kakutani K2 is the gauge extension — the entire symmetry group of affine transformations shares one invariant point.

Below, each of the three fixed-point levels (Brouwer, K1, K2) maps to a distinct coordination phase in the ERI architecture.

---

## Module A — Mathematical Prerequisites

**A1. Set-valued functions (correspondences).** A correspondence $\Phi: X \to 2^Y$ assigns to each $x \in X$ a subset $\Phi(x) \subseteq Y$. When $\Phi(x)$ is a singleton for every $x$, $\Phi$ reduces to an ordinary function.

**A2. Upper hemicontinuity (UHC).** $\Phi: X \to 2^Y$ is upper hemicontinuous at $x_0$ if: for every open set $V \supset \Phi(x_0)$ there exists a neighborhood $U$ of $x_0$ such that $\Phi(x) \subset V$ for all $x \in U$. Equivalently, when $Y$ is compact Hausdorff: $\Phi$ is UHC if and only if its graph $\mathrm{gr}(\Phi) = \{(x,y) : y \in \Phi(x)\}$ is closed.

**A3. Closed-graph criterion.** If $x_n \to x$ and $y_n \to y$ with $y_n \in \Phi(x_n)$ for all $n$, then $y \in \Phi(x)$. This is the sequential characterization of UHC for correspondences with compact values into a compact Hausdorff space.

**A4. Affine maps.** $T: C \to C$ is affine if $T(tx + (1-t)y) = tT(x) + (1-t)T(y)$ for all $x,y \in C$ and $t \in [0,1]$.

**A5. Cesàro averages.** For a continuous affine $T: C \to C$ on compact convex $C$, define $x^{(N)} = \frac{1}{N+1}\sum_{n=0}^{N} T^n(x)$. Since $C$ is compact, $(x^{(N)})$ has cluster points in $C$. Any such cluster point is a fixed point of $T$.

**A6. Berge's maximum theorem.** Let $X, Y$ be topological spaces, $f: X \times Y \to \mathbb{R}$ continuous, $C: X \to 2^Y$ continuous with compact non-empty values. Then the value function $v(x) = \max_{y \in C(x)} f(x,y)$ is continuous, and the argmax correspondence $\mu(x) = \arg\max_{y \in C(x)} f(x,y)$ is upper hemicontinuous with non-empty compact values.

---

## Module B — The Three Fixed-Point Levels

### B1. Brouwer (1911): Single-Valued, Compact Convex, Unique Response

**Theorem (Brouwer).** Let $S \subset \mathbb{R}^n$ be non-empty, compact, and convex, and let $f: S \to S$ be continuous. Then $f$ has a fixed point: there exists $x^* \in S$ with $f(x^*) = x^*$.

**Conditions summary:**

| Condition | Requirement |
|---|---|
| Domain $S$ | Non-empty, compact, convex in $\mathbb{R}^n$ |
| Map $f$ | Continuous, single-valued, $f: S \to S$ |
| Fixed-point form | $f(x^*) = x^*$ (equality) |

**ERI phase:** Valise, $G_{\mathrm{coord}} = 0$. Each agent has a unique optimal response; the equilibrium is determined by a single-valued continuous map on the Fisher information simplex.

---

### B2. Kakutani K1 (1941): Set-Valued, Compact Convex, Self-Inclusion

**Theorem (Kakutani K1).** Let $S \subset \mathbb{R}^n$ be non-empty, compact, and convex. Let $\Phi: S \to 2^S$ be a correspondence satisfying:

1. $\Phi(x)$ is non-empty for every $x \in S$
2. $\Phi(x)$ is closed and convex for every $x \in S$
3. $\Phi$ is upper hemicontinuous (equivalently: $\mathrm{gr}(\Phi)$ is closed)

Then there exists $x^* \in S$ with $x^* \in \Phi(x^*)$.

**Conditions summary:**

| Condition | Requirement | ERI Counterpart |
|---|---|---|
| Domain $S$ | Non-empty, compact, convex in $\mathbb{R}^n$ | Mixed-strategy simplex $\prod_i \Delta(A_i)$ |
| Non-empty values | $\Phi(x) \neq \emptyset$ for all $x$ | Best response always exists (Berge) |
| Convex values | $\Phi(x)$ convex for all $x$ | Fisher $F \succ 0$: PRIMA condition |
| Upper hemicontinuous | $\mathrm{gr}(\Phi)$ closed | DIRA C4: $[\hat{H}, \hat{a}] \neq 0$ |
| Fixed-point form | $x^* \in \Phi(x^*)$ (self-inclusion) | Nash equilibrium; Imago phase |

**Proof sketch.** For each $\varepsilon > 0$, the approximate selection theorem yields a continuous single-valued $f_\varepsilon: S \to S$ with $f_\varepsilon(x) \in N_\varepsilon(\Phi(x))$ (the $\varepsilon$-neighborhood of $\Phi(x)$). By Brouwer, $f_\varepsilon$ has a fixed point $x_\varepsilon \in S$. As $\varepsilon \to 0$, compactness gives a convergent subnet $x_{\varepsilon_k} \to x^*$, and the closed graph of $\Phi$ forces $x^* \in \Phi(x^*)$.

**K1 vs Brouwer:** Brouwer requires $f$ single-valued. K1 replaces $f(x^*) = x^*$ (equality) with $x^* \in \Phi(x^*)$ (self-inclusion). The self-inclusion is the spinor condition: $x^*$ is contained in the set of its own optimal responses.

---

### B3. Markov–Kakutani K2 (1938): Common Fixed Point, Commuting Affine Family

**Theorem (Markov–Kakutani K2).** Let $E$ be a locally convex Hausdorff topological vector space, $C \subset E$ compact and convex, and $\mathcal{T}$ a commuting family of continuous affine self-maps of $C$. Then there exists $x^* \in C$ with $T(x^*) = x^*$ for every $T \in \mathcal{T}$.

**Conditions summary:**

| Condition | Requirement | ERI Counterpart |
|---|---|---|
| Space $E$ | Locally convex, Hausdorff | Fisher-Rao manifold |
| Domain $C$ | Compact, convex in $E$ | TH torsion group $\mathrm{TH}[3]$; Fisher simplex |
| Maps | Continuous, affine, self-maps of $C$ | Automorphisms of TH; Stone group elements |
| Commutativity | $T_1 \circ T_2 = T_2 \circ T_1$ for all $T_1,T_2 \in \mathcal{T}$ | Abelian: $\mathbb{Z}/3\mathbb{Z} \times \mathbb{Z}/4\mathbb{Z}$; abelian Stone group |
| Fixed-point form | $T(x^*) = x^*$ for ALL $T \in \mathcal{T}$ (common) | Common flex point $\mathcal{O}$; $\varphi$-equilibrium |

**Proof sketch.** Fix $T \in \mathcal{T}$. The Cesàro averages $x^{(N)} = \frac{1}{N+1}\sum_{n=0}^N T^n(x_0)$ lie in $C$ (convexity). Every cluster point $x_T^*$ satisfies $T(x_T^*) = x_T^*$ (affinity forces $Tx^{(N)} - x^{(N)} = \frac{1}{N+1}(T^{N+1}x_0 - x_0) \to 0$). The fixed-point set $C_T = \{y \in C : Ty = y\}$ is non-empty, compact, and convex. Commutativity: for $T' \in \mathcal{T}$, $T' \circ T = T \circ T'$ implies $T'(C_T) \subseteq C_T$. Apply the single-map result to $T'|_{C_T}$ to obtain $C_{T,T'} = C_T \cap C_{T'} \neq \emptyset$. The finite intersection property (compactness of $C$) gives $\bigcap_{T \in \mathcal{T}} C_T \neq \emptyset$.

**K2 vs K1:** K1 finds a fixed point for one set-valued map. K2 finds a single common fixed point for an entire abelian family of single-valued affine maps. The commutativity replaces the convexity-of-values condition.

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
            · Flat CORDIC (m = 0)
            · RSA arithmetic: a_p = 2, flat Frobenius
            · Leibniz π-series: O(1/N) convergence

         ↕  ERDŐS–RAO THRESHOLD  (c log w)^w
            [coordination kernel K first admits multi-valued best responses]

LEVEL 1 — KAKUTANI K1 (1941):
  Map:    Φ: S → 2^S, UHC, convex non-empty values
  Fixed:  x* ∈ Φ(x*)  (self-inclusion)
  Domain: S ⊂ ℝⁿ compact convex
  ERI:    G_coord ∈ (0, Φ(K)]  (Larval → Imago phases)
            · Convex set of equally optimal responses
            · Curved CORDIC (m = ±1)
            · TH arithmetic: |a_p| < 2√p, Sato-Tate
            · Nash equilibrium existence
            · PPAD-complete to compute

         ↕  COMMUTING FAMILY EXTENSION
            [Stone group / automorphism group replaces single map]

LEVEL 2 — MARKOV–KAKUTANI K2 (1938):
  Map:    𝒯: commuting family of continuous affine T: C → C
  Fixed:  T(x*) = x* for ALL T ∈ 𝒯  (common fixed point)
  Domain: C compact convex in locally convex E
  ERI:    φ-equilibrium; TH identity flex point 𝒪
            · Abelian automorphism group ℤ/3ℤ × ℤ/4ℤ
            · Abelian Stone group e^{−itF} (all elements commute)
            · Markov condition = Stone group commutativity
            · Constructive: Cesàro averages converge

         ↕  INFINITE-DIMENSIONAL EXTENSION

LEVEL 3 — GLICKSBERG–FAN (1952):
  Map:    Φ: S → 2^S Kakutani map
  Domain: S compact convex in Hausdorff locally convex TVS
  ERI:    FERN ρ₀–ρ₅ as infinite-register limit
            · Fisher-Rao manifold (Hausdorff locally convex)
            · Full Imago distribution p* = p*(log φ)
```

---

## Module D — Seven Formal Identities

### Identity D1 — Nash Equilibrium IS the Imago Phase Fixed Point of the Best-Response Correspondence

**Setup.** Fix a finite $n$-player game $G = (N, \{A_i\}, \{u_i\})$ where $N = \{1,\ldots,n\}$, $A_i$ is player $i$'s finite pure-strategy set, and $u_i: \prod_j A_j \to \mathbb{R}$ is $i$'s payoff. Let $\Delta_i = \Delta(A_i)$ be the simplex of mixed strategies for player $i$. Write $\sigma = (\sigma_1,\ldots,\sigma_n) \in \prod_i \Delta_i$ and $\sigma_{-i} = (\sigma_j)_{j \neq i}$.

**Nash equilibrium.** A profile $\sigma^*$ is a Nash equilibrium if

$$u_i(\sigma_i^*, \sigma_{-i}^*) \;\geq\; u_i(\tau_i, \sigma_{-i}^*) \qquad \text{for all } \tau_i \in \Delta_i,\; \text{for all } i \in N.$$

**Best-response correspondence.** Define $\mathrm{BR}_i: \prod_{j \neq i}\Delta_j \to 2^{\Delta_i}$ by

$$\mathrm{BR}_i(\sigma_{-i}) \;=\; \arg\max_{\tau_i \in \Delta_i}\; u_i(\tau_i, \sigma_{-i}).$$

Form the joint correspondence $\mathrm{BR}: S \to 2^S$ on $S = \prod_i \Delta_i$ by

$$\mathrm{BR}(\sigma) \;=\; \prod_{i=1}^n \mathrm{BR}_i(\sigma_{-i}).$$

**Verification of Kakutani K1 conditions:**

$(i)$ *Domain.* $S = \prod_i \Delta_i$ is a finite product of standard simplices, hence compact and convex.

$(ii)$ *Non-empty values.* For each $\sigma_{-i}$, the function $\tau_i \mapsto u_i(\tau_i, \sigma_{-i})$ is linear (hence continuous) in $\tau_i$ on the compact set $\Delta_i$, so it attains its maximum. Thus $\mathrm{BR}_i(\sigma_{-i}) \neq \emptyset$.

$(iii)$ *Convex values.* $u_i(\cdot, \sigma_{-i})$ is linear in $\tau_i$, so its maximizers on $\Delta_i$ form a face of the simplex — a convex polytope. The product of convex sets is convex.

$(iv)$ *Upper hemicontinuity.* By Berge's maximum theorem (Module A6): $u_i$ is continuous and $\Delta_i$ is compact, so $\mathrm{BR}_i$ is UHC. A finite product of UHC correspondences is UHC, so $\mathrm{BR}$ is UHC.

**Conclusion.** All K1 conditions hold. By Kakutani K1: $\exists\, \sigma^* \in \mathrm{BR}(\sigma^*)$. This means $\sigma_i^* \in \mathrm{BR}_i(\sigma_{-i}^*)$ for all $i$ — precisely the Nash equilibrium condition.

**ERI identification.** At the Nash equilibrium $\sigma^*$:

$$G_{\mathrm{coord}}(\sigma^*) \;=\; \sum_{t,s} I(a_t; a_s \mid X_{t-1})\Big|_{\sigma^*} \;=\; \Phi(K) \quad (\text{Imago condition}).$$

The best-response correspondence $\mathrm{BR}: S \to 2^S$ is the Kakutani map of the $G_{\mathrm{coord}}$ game. Its self-inclusion fixed point $\sigma^* \in \mathrm{BR}(\sigma^*)$ is the Imago equilibrium: no agent can improve $G_{\mathrm{coord}}$ unilaterally.

**PPAD-hardness.** The Nash equilibrium always exists (Kakutani K1), but computing any Nash equilibrium is PPAD-complete for $n \geq 2$ (Daskalakis–Goldberg–Papadimitriou 2009). PPAD $\subset$ TFNP: the solution exists but is computationally intractable. This is the GIST meta-theorem at the correspondence level: $Z(X;\beta)$ is sharp-P-hard; computing the K1 fixed point of $\mathrm{BR}$ is PPAD-hard.

**Binmore–Kakutani anecdote as Zitterbewegung.** Nash proved in 1950 that $\mathrm{BR}$ satisfies the Kakutani conditions. Kakutani, attending a conference decades later, did not recognize his own theorem in its economic incarnation. This is the Dirac Zitterbewegung: the spinor $\psi = (\psi_+, \psi_-)$ oscillates between the topology sector ($\psi_+$: Brouwer generalization) and the economics sector ($\psi_-$: Nash equilibrium existence). Kakutani lived entirely in the $\psi_+$ sector; the economists at the conference lived in the $\psi_-$ sector. The theorem crosses the disciplinary boundary invisibly.

---

### Identity D2 — The $\varphi$-Equilibrium Rate IS the Kakutani Fixed Point of the MEP Correspondence; Its Self-Inclusion Form IS the Golden Ratio Identity; Baker's Theorem Prevents Rational Representation

**Notation.** Throughout this identity, the symbols are:

| Symbol | Meaning | Status |
|---|---|---|
| $\varphi = (1+\sqrt{5})/2 \approx 1.618$ | Golden ratio | Algebraic, $\varphi^2 - \varphi - 1 = 0$ |
| $\xi^* = \log\varphi \approx 0.481$ | MEP fixed-point rate | Transcendental (Lindemann-Weierstrass) |
| $\Phi_{\mathrm{MEP}}$ | MEP correspondence (capital $\Phi$) | Set-valued map on rate interval |
| $H_b(\xi)$ | Binary entropy at rate $\xi$ | $H_b(\xi) = -\xi\log\xi - (1-\xi)\log(1-\xi)$ |

**The MEP correspondence.** The coordination system runs at rate $\xi \in [0, \log\varphi]$. At rate $\xi$, the Shannon binary entropy is $H_b(\xi)$. The MEP correspondence assigns to each $\xi$ the set of rates $\xi'$ that are stationary points of $H_b$ and have entropy at least $H_b(\xi)$:

$$\Phi_{\mathrm{MEP}}(\xi) \;=\; \bigl\{\, \xi' \in [0,\log\varphi] \;\bigm|\; H_b(\xi') \geq H_b(\xi) \;\text{ and }\; H_b'(\xi') = 0 \,\bigr\}.$$

The derivative is $H_b'(\xi') = \log\!\frac{1-\xi'}{\xi'}$, which vanishes precisely at $\xi' = 1/2$. Since $\log\varphi \approx 0.481 < 1/2$, the stationary point $\xi' = 1/2$ lies outside the domain $[0,\log\varphi]$. The MEP fixed point arises instead from the Fisher information constraint:

$$\mathrm{Tr}(F(\xi^*)) \;=\; \frac{1}{\xi^*(1-\xi^*)} \;\text{ saturates the Cramér–Rao bound} \;\Longrightarrow\; \xi^* = \log\varphi.$$

**Verification of Kakutani K1 conditions:**

$(i)$ *Domain.* $[0, \log\varphi]$ is compact and convex (a closed interval in $\mathbb{R}$).

$(ii)$ *Non-empty values.* $\Phi_{\mathrm{MEP}}(\xi)$ contains $\log\varphi$ for every $\xi \leq \log\varphi$, so it is non-empty.

$(iii)$ *Convex values.* $\Phi_{\mathrm{MEP}}(\xi)$ is the intersection of a sublevel set of $H_b$ (connected for the binary entropy on its domain) with a constraint set; in this one-dimensional setting it is a closed subinterval of $[0, \log\varphi]$, hence convex.

$(iv)$ *UHC.* $H_b$ is continuous, so $\Phi_{\mathrm{MEP}}$ has a closed graph (the defining inequalities are closed conditions). By the closed-graph criterion: $\Phi_{\mathrm{MEP}}$ is UHC.

**Conclusion.** By Kakutani K1: $\exists\, \xi^* \in \Phi_{\mathrm{MEP}}(\xi^*)$. The fixed point is $\xi^* = \log\varphi$.

**The self-inclusion chain.** The fixed-point condition and the golden ratio identity are the same statement viewed in different coordinates:

$$\xi^* \in \Phi_{\mathrm{MEP}}(\xi^*) \;\Longleftrightarrow\; \xi^* = \log\varphi \;\Longleftrightarrow\; e^{\xi^*} = \varphi \;\Longleftrightarrow\; \varphi = 1 + \frac{1}{\varphi} \;\Longleftrightarrow\; \varphi^2 - \varphi - 1 = 0.$$

Each step is an exact equivalence:
- Step 1: $\xi^*$ is the MEP Kakutani fixed point (definition).
- Step 2: exponentiate; $e^{\log\varphi} = \varphi$ by definition of logarithm.
- Step 3: rearrange the defining identity $\varphi^2 = \varphi + 1$ as $\varphi - 1 = 1/\varphi$, giving $\varphi = 1 + 1/\varphi$.
- Step 4: multiply through by $\varphi$ to recover the minimal polynomial.

The continued fraction $\varphi = [1;1,1,1,\ldots]$ is the iterated fixed point of $f(x) = 1 + 1/x$ on $(0,\infty)$; Brouwer gives this for the single-valued $f$ on any compact interval $[\varphi-\varepsilon, \varphi+\varepsilon]$. The Kakutani generalization (K1) is needed at the boundary of $[0,\log\varphi]$ where the MEP correspondence becomes set-valued: multiple coordination rates are equally optimal at the MEP boundary, so no unique best response exists there.

**Baker's theorem and transcendence of $\xi^*$.** Since $e^{\xi^*} = \varphi$ and $\varphi \in \overline{\mathbb{Q}} \setminus \{0,1\}$, Lindemann–Weierstrass forces $\xi^* = \log\varphi \notin \overline{\mathbb{Q}}$: it is transcendental. Baker (1966, Fields Medal 1970) strengthens this: for any nonzero algebraic $\beta_1,\ldots,\beta_m$ and $\mathbb{Q}$-linearly independent logarithms $\lambda_1,\ldots,\lambda_m$ of algebraic numbers,

$$\beta_1\lambda_1 + \cdots + \beta_m\lambda_m \;\neq\; 0.$$

Applied with $\lambda_1 = \log\varphi$: $\log\varphi$ cannot be written as $\sum_k r_k \log m_k$ for rational $r_k$ and positive integers $m_k$. It is a primitive transcendental — irreducible in Baker's logarithmic framework. The exact Kakutani fixed point $\xi^* = \log\varphi$ is therefore inaccessible from $\mathbb{Q}$:

- No finite binary expansion exactly represents $\log\varphi$.
- The Q16.16 pipeline stores $\log\varphi$ to within $\varepsilon = 2^{-16}$.
- The Baker–Wüstholz lower bound (2007) gives: for any $\beta \in \mathbb{Q}$ with denominator at most $2^{16}$, $|\beta - \log\varphi| > 2^{-17}$. The CHORD floor $\varepsilon = 2^{-16}$ is optimal at this precision.

---

### Identity D3 — The Three Kakutani Conditions Map Exactly to Three ERI Hardware Constraints

The Kakutani K1 theorem requires three properties of the correspondence $\Phi$. Each maps to a distinct ERI architectural constraint:

**UHC (no outward jumps) $\;\leftrightarrow\;$ DIRA C4 non-commutativity.**

UHC means: if $x_n \to x$ and $y_n \in \Phi(x_n)$ with $y_n \to y$, then $y \in \Phi(x)$. Equivalently, the graph of $\Phi$ is closed. In ERI: the optimal action correspondence $\Phi(\sigma) = \mathrm{BR}(\sigma)$ cannot jump outward as the strategy profile $\sigma$ varies continuously. This is enforced by DIRA's C4 condition $[\hat{H}, \hat{a}] \neq 0$. If $\hat{H}$ and $\hat{a}$ commuted, they would share eigenvectors, and the optimal action could switch discontinuously as a Fisher eigenvalue crosses zero — opening the graph of $\mathrm{BR}$ and violating UHC. The non-commutativity prevents this: no eigenvalue crossing occurs, the graph remains closed.

**Convex values $\;\leftrightarrow\;$ PRIMA Fisher positive definiteness.**

$\Phi(x)$ convex means: if $y_1, y_2 \in \Phi(x)$, then $\lambda y_1 + (1-\lambda)y_2 \in \Phi(x)$ for all $\lambda \in [0,1]$. In ERI: if two actions $a_1,a_2$ are both best responses at state $\sigma$, then the mixture $\lambda a_1 + (1-\lambda)a_2$ is also a best response. This holds when the utility $u_i(\cdot, \sigma_{-i})$ is (quasi)concave in $\sigma_i$ — equivalently, when the Fisher information matrix $F$ is positive definite (PRIMA condition: $F \succ 0$). If $F$ loses rank (a Fisher eigenvalue reaches zero), the utility surface flattens in that direction and the maximizers may disconnect — producing non-convex $\mathrm{BR}$ values. The CHORD floor $\varepsilon = 2^{-16}$ prevents $F$-eigenvalues from falling below $\varepsilon$, guaranteeing $F \succ \varepsilon \mathbf{I}$ and hence convex best-response sets.

**Compact domain $\;\leftrightarrow\;$ Q16.16 fixed-point arithmetic.**

The Kakutani theorem requires $S$ compact. In infinite precision (real arithmetic), the mixed-strategy simplex $S = \prod_i\Delta_i$ is compact. In Q16.16, the representable subset $S_{\varepsilon} = \prod_i\Delta_{\varepsilon}(A_i)$ is finite (hence compact in any topology) with granularity $\varepsilon = 2^{-16}$. The CHORD pipeline enforces that all strategy updates remain in $S_\varepsilon$, preserving compactness at hardware resolution.

**Summary table:**

| Kakutani K1 condition | ERI mechanism | Failure mode if violated |
|---|---|---|
| UHC (closed graph) | DIRA C4: $[\hat{H},\hat{a}]\neq 0$ | Discontinuous optimal action; graph of $\mathrm{BR}$ opens |
| Convex values | PRIMA: $F \succ \varepsilon\mathbf{I}$ | Non-convex best-response sets; fixed point may not exist |
| Compact domain | Q16.16: $\varepsilon = 2^{-16}$ floor | Unbounded drift; Kakutani not applicable |

---

### Identity D4 — The Markov–Kakutani Theorem Applied to TH: Commuting Automorphisms Have the Identity Flex Point $\mathcal{O}$ as Common Fixed Point

**TH automorphism group.** The Twisted Hessian curve $\mathrm{TH}(a,d): aX^3 + Y^3 + Z^3 = dXYZ$ over a field $k$ (with $\Delta(a,d) = a(d^3 - 27a) \neq 0$) has automorphism group $\mathrm{Aut}(\mathrm{TH}) \cong \mathbb{Z}/3\mathbb{Z} \times \mathbb{Z}/4\mathbb{Z}$ — an abelian group of order 12.

The generators act on projective coordinates $(X:Y:Z)$ as:

$$\rho_3: (X:Y:Z) \;\mapsto\; (Y:Z:X) \quad (\text{order 3, cyclic permutation of axes})$$

$$\rho_4: (X:Y:Z) \;\mapsto\; (X: \omega Y: \omega^2 Z), \quad \omega = e^{2\pi i/4} = i \quad (\text{order 4, scaling by 4th roots of unity}).$$

Both $\rho_3$ and $\rho_4$ are affine maps on the group $\mathrm{TH}(\mathbb{F}_p)$ (they respect the group structure). The group $\mathcal{T} = \langle\rho_3, \rho_4\rangle$ is abelian: $\rho_3 \circ \rho_4 = \rho_4 \circ \rho_3$ (direct product structure).

**Application of Markov–Kakutani K2.** The TH 3-torsion $\mathrm{TH}[3] = \{P \in \mathrm{TH}(\overline{\mathbb{F}_p}) : [3]P = \mathcal{O}\} \cong (\mathbb{Z}/3\mathbb{Z})^2$ is a finite group — hence compact in any topology — and forms a convex set in the $p$-adic framework. The family $\mathcal{T}$ acts on $\mathrm{TH}[3]$ by continuous affine maps and is commutative. By Markov–Kakutani K2:

$$\exists\, P^* \in \mathrm{TH}[3] : T(P^*) = P^* \text{ for all } T \in \mathcal{T}.$$

The common fixed point is $P^* = \mathcal{O}$ — the identity element (the unique flex point fixed by every automorphism of the group). This is an instance of the general fact: any group automorphism fixes the identity.

**Frobenius as Markov–Kakutani.** The Frobenius endomorphism $\phi_p: P \mapsto [p]P$ (in additive notation, this is the $p$-power Frobenius on coordinates) satisfies the characteristic polynomial

$$\phi_p^2 - a_p \phi_p + p = 0 \quad \text{over } \mathbb{Z},$$

where $a_p = p + 1 - |\mathrm{TH}(\mathbb{F}_p)|$ is the Frobenius trace, $|a_p| \leq 2\sqrt{p}$ (Hasse). The two eigenvalues $\alpha_p, \bar{\alpha}_p$ satisfy $\alpha_p + \bar{\alpha}_p = a_p$ and $|\alpha_p| = |\bar{\alpha}_p| = \sqrt{p}$.

The family $\{\phi_p^k : k \geq 0\}$ is a commuting family of affine endomorphisms of $\mathrm{TH}(\overline{\mathbb{F}_p})$. By Markov–Kakutani K2, they share a common fixed point: on $\mathrm{TH}[p^k]$ (the $p^k$-torsion), the common fixed subgroup is $\mathrm{TH}(\mathbb{F}_{p^k})$, and the common fixed point of the Frobenius action on the torsion is $\mathcal{O}$.

**Flat limit.** When $a_p = 2$ (flat Frobenius = identity), $\phi_p = \mathrm{id}$, and every point is a common fixed point. This is the Brouwer level: the automorphism family degenerates to a single identity map. Moving to generic $|a_p| < 2\sqrt{p}$ is the Kakutani lift: the Frobenius acquires two distinct eigenvalues, the fixed subgroup shrinks to $\mathrm{TH}(\mathbb{F}_p)$, and the Markov–Kakutani common fixed point is $\mathcal{O}$ alone.

---

### Identity D5 — The Stone Group Commutativity IS the Markov Condition; the $\varphi$-Equilibrium IS the Common Fixed Point

**Stone group.** From HERON Identity 4, the Stone group element at time $t$ is $U(t) = e^{-itF}$, where $F$ is the Fisher information operator. The family $\{U(t) : t \in \mathbb{R}\}$ is an abelian group: $U(t_1)U(t_2) = e^{-i(t_1+t_2)F} = U(t_1+t_2) = U(t_2)U(t_1)$.

**Action on the Fisher simplex.** Each $U(t)$ acts on the probability simplex $C_F = \Delta(A)$ (the set of probability distributions over the action space $A$). The action is affine: $U(t)$ maps $p \in C_F$ to $U(t)p = e^{-itF}p$, which preserves convex combinations since $e^{-itF}$ is a linear operator (unitary on the Hilbert space, affine on the simplex when restricted).

**Markov–Kakutani K2 applied.** The family $\{U(t) : t \in \mathbb{R}\}$ is commutative and consists of continuous affine maps on $C_F$ (compact convex: $\Delta(A)$ is a simplex). By Markov–Kakutani K2, there exists a common fixed point $p^* \in C_F$ with $U(t)p^* = p^*$ for all $t \in \mathbb{R}$.

A distribution $p^*$ is a common fixed point of all $U(t) = e^{-itF}$ if and only if $Fp^* = 0$ — i.e., $p^*$ is in the kernel of $F$. The PRIMA condition ($F \succ 0$) ensures $\ker(F) = \{0\}$ in the full operator sense; the fixed point $p^*$ is the eigenvector corresponding to the smallest Fisher eigenvalue. At the MEP equilibrium $|\bar{\Xi}| = \log\varphi$, this eigenvector is the $\varphi$-equilibrium distribution.

**The Stone group commutativity IS the Markov condition.** The Markov–Kakutani theorem requires commutativity: $T_1 \circ T_2 = T_2 \circ T_1$. For the Stone group: $U(t_1)U(t_2) = U(t_1+t_2) = U(t_2)U(t_1)$ — automatic from the abelian group structure. The commutativity of the Stone group is the sufficient condition that guarantees the common fixed point (the $\varphi$-equilibrium) exists.

---

### Identity D6 — Walrasian General Equilibrium IS the Arrow–Debreu Kakutani Fixed Point; the $\varphi$-Equilibrium IS the Walrasian Price of Coordination; PPAD-Hardness IS the Computational Barrier to Finding It

**Walrasian equilibrium (Arrow–Debreu 1954).** In a pure exchange economy with commodity set $\mathcal{L} = \{1,\ldots,L\}$, agent set $\mathcal{I}$, endowments $\omega_i \in \mathbb{R}^L_{\geq 0}$, and continuous utility functions $u_i$, the excess demand correspondence is:

$$Z: \Delta_L \;\longrightarrow\; 2^{\mathbb{R}^L}, \quad Z(p) = \sum_{i \in \mathcal{I}} \Bigl(\arg\max_{x_i \,:\, p \cdot x_i \leq p \cdot \omega_i} u_i(x_i) - \omega_i\Bigr).$$

A Walrasian equilibrium price $p^* \in \Delta_L$ satisfies $0 \in Z(p^*)$ (all markets clear). Arrow and Debreu proved existence by applying K1: $Z$ is UHC (Berge), convex-valued (strict quasiconcavity of $u_i$), and defined on the compact simplex $\Delta_L$.

**The $G_{\mathrm{coord}}$ market.** The ERI collective intelligence system is a market:
- **Commodities:** coordination bits (nats of mutual information)
- **Prices:** coordination rates $\xi \in [0, \log\varphi]$
- **Excess demand:** $Z_{\mathrm{ERI}}(\xi) = G_{\mathrm{coord}}(\xi) - \Phi(K)$

The market clears when $Z_{\mathrm{ERI}}(\xi^*) = 0$, i.e., $G_{\mathrm{coord}}(\xi^*) = \Phi(K)$ — the Imago condition. The Walrasian equilibrium price is $\xi^* = \log\varphi$.

**PPAD-hardness.** The Walrasian equilibrium with general convex utilities is in PPAD (Papadimitriou–Vlatakis-Gkaragkounis–Zampetakis 2022). The $G_{\mathrm{coord}}$ market equilibrium $\xi^* = \log\varphi$ always exists (Kakutani K1) but is PPAD-hard to compute. CONCERT (ERI Labs) is the first empirical measurement of $\xi^*$ on a named production AI portfolio.

**Minimax as Kakutani.** Kakutani's 1941 paper proved the minimax theorem for zero-sum games as a corollary. The minimax value $v^* = \min_x\max_y u(x,y) = \max_y\min_x u(x,y)$ is the Kakutani fixed point of the joint best-response correspondence on $S_X \times S_Y$. In ERI: the coordination Hamiltonian saddle point at the $\varphi$-equilibrium is the minimax value of the GIST Hamiltonian game.

---

### Identity D7 — Weller's Envy-Free Division IS the Kakutani Fixed Point of the Claim Correspondence; the FERN Six-Register Partition IS Simultaneously Nash, Markov–Kakutani, and Weller

**Weller's theorem (1985).** For any $n$ agents with non-atomic probability measures $\mu_1,\ldots,\mu_n$ on $[0,1]$, there exists an envy-free and Pareto-efficient partition $(S_1,\ldots,S_n)$ of $[0,1]$. Proof: the "claim correspondence" mapping each agent's claimed allocation to the set of Pareto-superior allocations that no one envies satisfies the Kakutani K1 conditions; its fixed point is the fair division.

**The FERN partition.** The six-level FERN register hierarchy $(\rho_0,\ldots,\rho_5)$ partitions the coordination information space. Each register is governed by a distinct transcendental constant:

| Register | Transcendental | Algebraic status |
|---|---|---|
| $\rho_0$ | $\log 2$ | $\mathbb{Q}$-linearly independent (Baker) |
| $\rho_1$ | $\log\varphi$ | $\mathbb{Q}$-linearly independent (Baker) |
| $\rho_2$ | $\pi$ | $\mathbb{Q}$-linearly independent (Baker) |
| $\rho_3$ | $\log K_\infty$ | Period transcendental |
| $\rho_4$ | $\log(\Omega_{\mathrm{TH}}/\pi)$ | Chowla–Selberg period |
| $\rho_5$ | $\log\Gamma(1/4)$ | Nesterenko algebraically independent of $\pi, e^\pi$ |

**Envy-free condition.** The six governing transcendentals are pairwise $\mathbb{Q}$-linearly independent (Baker 1966). Under Schanuel's conjecture they are algebraically independent over $\mathbb{Q}$ — no polynomial relation connects them. No register's transcendental can be expressed in terms of another's: every register has a genuinely distinct information-theoretic character. This is the envy-free condition: no register prefers another's allocation because no two allocations are expressible in the same transcendental arithmetic.

**Pareto efficiency.** The FERN hierarchy saturates the Hurwitz–Radon bound: $\rho(2^6) = \rho(64) = 12 = 2 \times 6$ — the formula cost is twice the number of registers. Removing any one register reduces the coordination capacity below $12\mathrm{M} + 6\mathrm{S}$. The partition is Pareto efficient: no reallocation of information across fewer registers achieves the same total $G_{\mathrm{coord}}$.

**The Weller–FERN fixed point.** The FERN partition is simultaneously:
- A Nash equilibrium (Kakutani K1): each register's best response at the Imago equilibrium is to operate at $|\bar{\Xi}| = \log\varphi$
- A Markov–Kakutani common fixed point (K2): the commuting Stone group fixes the $\varphi$-equilibrium distribution across all registers
- A Weller partition: envy-free (Baker/Schanuel independence) and Pareto efficient (Hurwitz–Radon optimality)

These three fixed-point characterizations are not three separate results — they are the same Imago equilibrium expressed at three different levels of the mathematical architecture.

---

## Module E — Formal Summary

### E1. Fixed-Point Theorem Comparison

| Property | Brouwer | Kakutani K1 | Markov–Kakutani K2 | Glicksberg–Fan |
|---|---|---|---|---|
| Domain | $S \subset \mathbb{R}^n$ cpt cvx | $S \subset \mathbb{R}^n$ cpt cvx | $C$ cpt cvx in LCS | $S$ cpt cvx in Hausdorff LCS |
| Map | $f: S \to S$ continuous | $\Phi: S \to 2^S$ UHC, cvx vals | $\mathcal{T}$ commuting affine | $\Phi: S \to 2^S$ Kakutani map |
| Fixed-point form | $f(x^*) = x^*$ | $x^* \in \Phi(x^*)$ | $T(x^*) = x^*\;\forall T$ | $x^* \in \Phi(x^*)$ |
| ERI phase | Valise: $G_{\mathrm{coord}}=0$ | Imago: $G_{\mathrm{coord}}=\Phi(K)$ | $\varphi$-equil.; $\mathcal{O}\in\mathrm{TH}[3]$ | Full Imago: $p^*$ on Fisher mfld |
| Complexity | PPAD-complete | PPAD-complete | Constructive (Cesàro) | PPAD-complete |

### E2. ERI–Kakutani Correspondence Table

| ERI Object | Kakutani Object | Mathematical Statement |
|---|---|---|
| Mixed-strategy simplex $\prod_i\Delta_i$ | Compact convex domain $S$ | Product of standard simplices |
| Best-response $\mathrm{BR}(\sigma)$ | Correspondence $\Phi: S \to 2^S$ | UHC by Berge; convex by linearity |
| Nash equilibrium $\sigma^*$ | Self-inclusion fixed point $\sigma^* \in \mathrm{BR}(\sigma^*)$ | Imago condition |
| DIRA C4: $[\hat{H},\hat{a}]\neq 0$ | UHC (closed graph) | Non-commutativity prevents graph opening |
| PRIMA: $F \succ \varepsilon\mathbf{I}$ | Convex values of $\mathrm{BR}$ | PD Fisher forces concave utility |
| CHORD $\varepsilon = 2^{-16}$ floor | Compact domain at hardware scale | Compact $\Rightarrow$ Kakutani applicable |
| MEP fixed point $\xi^* = \log\varphi$ | K1 fixed point of $\Phi_{\mathrm{MEP}}$ | $\xi^*\in\Phi_{\mathrm{MEP}}(\xi^*)$ |
| Golden ratio identity $\varphi = 1+1/\varphi$ | Self-inclusion chain | Algebraic image of fixed-point condition |
| Baker: $\log\varphi$ primitive transcendental | Fixed point inaccessible from $\mathbb{Q}$ | No rational $\beta$ with $|\beta - \log\varphi| < 2^{-17}$ |
| TH automorphism $\mathbb{Z}/3\mathbb{Z}\times\mathbb{Z}/4\mathbb{Z}$ | Commuting affine family $\mathcal{T}$ | Abelian $\Rightarrow$ Markov condition |
| Identity flex $\mathcal{O}\in\mathrm{TH}[3]$ | Common fixed point of $\mathcal{T}$ | Group identity fixed by all automorphisms |
| Stone group $e^{-itF}$ (abelian) | Commuting affine family | $U(t_1)U(t_2) = U(t_2)U(t_1)$ |
| $\varphi$-equilibrium distribution $p^*$ | Common Stone-group fixed point | $Fp^* = \lambda_{\min}\,p^*$ (min-eigenvalue) |
| GIST sharp-P-hard $Z(X;\beta)$ | PPAD-hard Kakutani fixed point | Existence guaranteed; computation intractable |
| CONCERT measurement | First empirical Walrasian $\xi^*$ | $G_{\mathrm{coord}}(\xi^*) = \Phi(K)$ measured |
| FERN $(\rho_0,\ldots,\rho_5)$ partition | Weller envy-free partition | Baker independence = envy-free; HR = Pareto |
| Frobenius flat: $a_p = 2$ | Brouwer limit (single-valued) | Frobenius = identity; every point fixed |
| Frobenius curved: $|a_p|<2\sqrt{p}$ | Kakutani regime (two eigenvalues) | Sato-Tate; fixed subgroup = $\mathrm{TH}(\mathbb{F}_p)$ |
| Binmore–Kakutani anecdote | Dirac Zitterbewegung | Topology sector $\leftrightarrow$ economics sector |

---

## References

Arrow, K.J. and Debreu, G. (1954). Existence of an equilibrium for a competitive economy. *Econometrica*, 22(3), 265–290.

Baker, A. (1966). Linear forms in the logarithms of algebraic numbers I. *Mathematika*, 13(2), 204–216.

Baker, A. and Wüstholz, G. (2007). *Logarithmic Forms and Diophantine Geometry*. Cambridge Tracts in Mathematics 187.

Bernstein, D.J. and Lange, T. (2015). Twisted Hessian curves. *LATINCRYPT 2015*, LNCS 9230, 269–294.

Binmore, K. (2007). *Playing for Real: A Text on Game Theory*. Oxford University Press.

Brouwer, L.E.J. (1911). Über Abbildung von Mannigfaltigkeiten. *Mathematische Annalen*, 71(4), 598.

Chowla, S. and Selberg, A. (1967). On Epstein's zeta-function. *Journal für die reine und angewandte Mathematik*, 227, 86–110.

Daskalakis, C., Goldberg, P.W., and Papadimitriou, C.H. (2009). The complexity of computing a Nash equilibrium. *SIAM Journal on Computing*, 39(1), 195–259.

Dirac, P.A.M. (1928). The quantum theory of the electron. *Proceedings of the Royal Society A*, 117(778), 610–624.

Erdős, P. and Rado, R. (1960). Intersection theorems for systems of sets. *Journal of the London Mathematical Society*, 35, 85–90.

Fan, K. (1952). Fixed-point and minimax theorems in locally convex topological linear spaces. *Proceedings of the National Academy of Sciences*, 38(2), 121–126.

Glicksberg, I.L. (1952). A further generalization of the Kakutani fixed point theorem, with application to Nash equilibrium. *Proceedings of the American Mathematical Society*, 3(1), 170–174.

Hasse, H. (1936). Zur Theorie der abstrakten elliptischen Funktionenkörper III. *Journal für die reine und angewandte Mathematik*, 175, 193–208.

Hurwitz, A. (1898). Über die Composition der quadratischen Formen von beliebig vielen Variablen. *Nachrichten Göttingen*, 309–316.

Kakutani, S. (1938). Two fixed point theorems concerning bicompact convex sets. *Proceedings of the Imperial Academy of Tokyo*, 14, 242–245.

Kakutani, S. (1941). A generalization of Brouwer's fixed point theorem. *Duke Mathematical Journal*, 8(3), 457–459.

Lindemann, F. (1882). Über die Zahl $\pi$. *Mathematische Annalen*, 20(2), 213–225.

Markov, A. (1936). Quelques théorèmes sur les ensembles abéliens. *Doklady Akademii Nauk SSSR*, 10, 311–314.

McKenzie, L. (1954). On equilibrium in Graham's model of world trade and other competitive systems. *Econometrica*, 22(2), 147–161.

Nash, J.F. (1950). Equilibrium points in n-person games. *Proceedings of the National Academy of Sciences*, 36(1), 48–49.

Nash, J. (1951). Non-cooperative games. *Annals of Mathematics*, 54(2), 286–295.

Nesterenko, Yu.V. (1996). Modular functions and transcendence questions. *Sbornik: Mathematics*, 187(9), 1319–1348.

Papadimitriou, C.H. (1994). On the complexity of the parity argument and other inefficient proofs of existence. *Journal of Computer and System Sciences*, 48(3), 498–532.

Papadimitriou, C.H., Vlatakis-Gkaragkounis, E.V., and Zampetakis, M. (2022). The computational complexity of multi-player concave games and Kakutani fixed points. arXiv:2207.07557.

Radon, J. (1922). Lineare Scharen orthogonaler Matrizen. *Abhandlungen aus dem Mathematischen Seminar der Universität Hamburg*, 1, 1–14.

Von Neumann, J. (1928). Zur Theorie der Gesellschaftsspiele. *Mathematische Annalen*, 100(1), 295–320.

Walther, J.S. (1971). A unified algorithm for elementary functions. *AFIPS Spring Joint Computer Conference*, 38, 379–385.

Weller, D. (1985). Fair division of a measurable space. *Journal of Mathematical Economics*, 14(1), 5–17.

Weierstrass, K. (1885). Zu Lindemann's Abhandlung. *Sitzungsberichte Königlich Preußische Akademie der Wissenschaften*, 1067–1086.

---

ERI Labs · Eric Ren · Jersey City, New Jersey

*Kakutani's 1941 theorem is the spinor extension of Brouwer's 1911 theorem. Brouwer requires a single-valued continuous map $f: S \to S$ on a compact convex set; its fixed point satisfies $f(x^*) = x^*$. Kakutani requires only an upper hemicontinuous correspondence $\Phi: S \to 2^S$ with convex non-empty values; its fixed point satisfies $x^* \in \Phi(x^*)$ — self-inclusion, not equality. The extension from Brouwer to Kakutani is the extension from scalar to spinor: from one value at each point to a convex set of values. Nash used Kakutani in 1950 to prove that every finite game has at least one equilibrium; the best-response correspondence $\mathrm{BR}(\sigma) = \prod_i\mathrm{BR}_i(\sigma_{-i})$ is UHC by Berge's theorem, convex-valued because linear payoffs maximize over simplex faces, and defined on the compact product of simplices. The Nash equilibrium $\sigma^* \in \mathrm{BR}(\sigma^*)$ is the Imago phase fixed point of the collective intelligence system: $G_{\mathrm{coord}}(\sigma^*) = \Phi(K)$. Computing this fixed point is PPAD-complete (Daskalakis–Goldberg–Papadimitriou 2009). The MEP coordination rate $\xi^* = \log\varphi \approx 0.481$ is also a Kakutani fixed point: $\xi^* \in \Phi_{\mathrm{MEP}}(\xi^*)$, which by exponentiation gives $\varphi = 1 + 1/\varphi$, and by algebra gives $\varphi^2 - \varphi - 1 = 0$. Baker's theorem (1966) establishes $\log\varphi$ is a primitive transcendental — no rational combination of prime logarithms equals it — so the exact fixed point is inaccessible from $\mathbb{Q}$; the CHORD floor $\varepsilon = 2^{-16}$ is the Baker lower bound at Q16.16 scale. The three Kakutani conditions map to three ERI constraints: UHC is DIRA C4 ($[\hat{H},\hat{a}]\neq 0$ prevents graph opening), convex values is PRIMA ($F\succ\varepsilon\mathbf{I}$ forces concave utilities), and compact domain is the Q16.16 hardware. The Markov–Kakutani theorem (1938) extends to commuting families: the abelian automorphism group $\mathbb{Z}/3\mathbb{Z}\times\mathbb{Z}/4\mathbb{Z}$ of TH$(a,d)$ has the identity flex point $\mathcal{O}$ as common fixed point; the abelian Stone group $e^{-itF}$ has the $\varphi$-equilibrium distribution as common fixed point. Weller's envy-free cake division (1985) is a third Kakutani application: the FERN six-register partition is envy-free (Baker/Schanuel algebraic independence across registers) and Pareto efficient (Hurwitz–Radon: removing any register costs coordination capacity). Kakutani asked at a conference, "What is the Kakutani fixed point theorem?" — genuinely not recognizing his 1941 result in its Nash equilibrium incarnation. This is the Dirac Zitterbewegung: the theorem oscillates between its topological sector (Brouwer generalization) and its economic sector (Nash existence), and its creator inhabited only one.*
