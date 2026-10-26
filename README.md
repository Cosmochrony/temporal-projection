# Temporal Residual Map from the Completed Principal Symbol

This repository contains the source of the paper
*Temporal Residual Map from the Completed Principal Symbol:
Construction, Uniqueness, and the Lorentz Identification*
(TempProj of the Lorentz Capacity sub-programme).

## Overview

The companion paper **LorentzCapacity** (`Beau2026n`) identifies the construction of a temporal
residual map $\mathcal{P}_\tau^{\mathrm{Q5b}}$ as the remaining step to close the Lorentz
identification from O7 observables, but defers its explicit construction.

The present paper carries out this construction from three inputs, which play different roles:

1. **(L) Temporal splitting** — a supplied rank-four co-metric of the conditional form of Q11
   Corollary 6.1, $g^{\mu\nu} = \mathrm{diag}(-A_\tau, 2\lambda, 2\lambda, 2\lambda)$ with $A_\tau$ and
   $\lambda$ independent and fixed by no source, determines the direction $\partial_\tau$, orthogonal to the
   spatial directions. The projector uses only the decoupled temporal block, not the coefficient values and not
   the signature; the normalisation $g^{\mu\nu} = 2\eta^{\mu\nu}$ is a choice of units.
2. **(BI) Born-Infeld capacity sphere** — the admissible capacity flow vector $\vec{F}_n$
   lies on the unit sphere $(F_n^\tau)^2 + |\vec{F}_n^{\mathrm{spat}}|^2 = 1$.
3. **(W) Weil filling law** — $\Sigma_n^{\mathrm{tot}} = 1 - B_n$ exactly (proved in LorentzCapacity).

The spatial component of the capacity flow is identified with $B_n$; this identification (S) is a
hypothesis of the paper, not a consequence of the Q5b Carnot convergence.

## Main Result

$$\mathcal{P}_\tau^{\mathrm{Q5b}}\,\Sigma_n^{\mathrm{tot}}
= \sqrt{\Sigma_n^{\mathrm{tot}}\bigl(2 - \Sigma_n^{\mathrm{tot}}\bigr)}
= \sqrt{1 - B_n^2}$$

Consequently, exactly:
$$\Phi(\eta_n^\tau) = \frac{1}{\sqrt{1+(\eta_n^\tau)^2}} = \sqrt{1 - B_n^2}$$

Three statements are distinct:

- **Scalar uniqueness.** The quadratic law (BI) and the Weil filling law (W) alone force the values of any
  non-negative map at the values of $\Sigma_n^{\mathrm{tot}}$ actually attained, $0 \le n \le R = (q-1)/2$: a
  finite set of $R+1$ points in $[1/2 - 1/(2q^2),\, 1 - 1/q^2]$. Off that set the map is not constrained.
  (L) is not used and is not necessary for this uniqueness.
- **Identification of the component.** (L) identifies the value so fixed as the $\partial_\tau$-component of
  the capacity flow; it does not select the formula.
- **Lorentzian kinematic reading.** Reading $B_n$ as the velocity of an observer, and the value as time
  dilation, uses the Lorentzian signature of the co-metric and the hypothesis **[H-cone]**: the light-cone speed
  of the co-metric equals the Born-Infeld bound per ordering step. This is the coupling datum that Q11 leaves
  open (Q11-O1); it is not derived. In the domain of the theorem the load satisfies
  $B_n \le 1/2 + 1/(2q^2)$; the light cone $B = 1$ is reached only by the exact torus load of LC-O3.

The three candidates tested in LorentzCapacity all fail the quadratic law (BI); the square-root complement
obeys a linear budget, the depth proxy uses the normalised depth in place of $B_n$ (it violates (S)), and the
central coverage is not a function of $B_n$.

## Status

- Explicit formula on the attained values: **proved** under a supplied co-metric of the form of Q11
  Corollary 6.1, the identification (S) and the Born-Infeld lift
- Scalar uniqueness on the attained values from (BI) and (W): **proved**; it uses neither (L) nor the co-metric
- Identification of the value as the temporal component: under (L), (S) and the Born-Infeld lift; the
  signature is not used
- Necessity: the quadratic law and (W) are necessary for the uniqueness, (L) is not (**proved**)
- Lorentz factor corollary: formula **proved** under the same hypotheses; kinematic reading conditional on
  [H-cone] and the Lorentzian signature
- Failure modes of the LorentzCapacity candidates: all fail (BI) (**proved** for the square-root complement and
  the depth proxy; numerical for the central coverage)
- Hypothesis [U] enters no step; it is open (U1 records that no proof is available)

## Position in the sub-programme

```
LorCap → TempProj → LCII
```

TempProj constructs the temporal residual map left open by LorCap. LCII (`Beau2026lco2`) extends the result
to non-homogeneous regimes (gravitational time dilation, under the declared postulate of LCII Remark 3.2).

## Dependencies

| Paper | Role |
|-------|------|
| LorCap (`Beau2026n`) | Origin of the open problem |
| Q5b (`Beau2026q5b`) | Effective operator and rank-three co-metric, under [H-L] and [H-lift] |
| Q11 (`Beau2026q11`) | Conditional rank-four form $\mathrm{diag}(-A_\tau, 2\lambda, 2\lambda, 2\lambda)$; $A_\tau$ free; coupling datum open |
| Q10 (`Beau2026q10`) | No coefficient value derived |
| Q8 (`BeauQ8`) | $A_H = A_Z = 2\lambda$ with $\lambda$ free, for a supplied invariant form |
| U1 (`Beau2026u1`) | Hypothesis [U] open; not used |
| O7 (`Beau2026a11`) | Defines $B_n$ and $\Sigma_n^{\mathrm{tot}}$ |
| BI (`Beau2026c`) | Capacity bound [A-cap], expressed by the quadratic budget hypothesis |
| PTO (`Beau2026pto`) | Projective temporal ordering (structural context) |

## Repository Contents

```
temporal-projection/
├── out/              # Compiled PDF
├── tex/
│   ├── temporal-projection.tex
│   └── cosmochrony-bibliography.bib
├── compile.sh
├── zenodo.json
└── README.md
```

## Citation

> J. Beau, *Temporal Residual Map from the Completed Principal Symbol:
> Construction, Uniqueness, and the Lorentz Identification*, Preprint, 2026.

## Acknowledgements

Portions of the editorial refinement benefited from iterative interactions with
large language models used as analytical assistants.
All claims, interpretations, and final formulations remain the sole
responsibility of the author.
