# Temporal Residual Projection from the Completed Principal Symbol

This repository contains the source of the paper
*Temporal Residual Projection from the Completed Principal Symbol:
Explicit Construction of $\mathcal{P}_\tau^{\mathrm{Q5b}}$ and the Lorentz Identification*
(Cosmochrony / spectral admissibility programme).

## Overview

The companion paper **LorCap** (Spectral Mobility and the Lorentz Factor, `Beau2026n`)
establishes, conditionally, that the relativistic Lorentz factor emerges from the O7
saturation parameter via a temporally projected residual
$\Sigma_n^\tau := \mathcal{P}_\tau^{\mathrm{Q5b}}\,\Sigma_n^{\mathrm{tot}}$,
provided $B_n^2 + (\Sigma_n^\tau)^2 \to 1$.
The temporal projection operator $\mathcal{P}_\tau^{\mathrm{Q5b}}$ was defined
abstractly there, and its explicit construction was left as the remaining open task.

The present paper closes this gap.

## Main Result

Starting from the Q5b completed Lorentzian co-metric
$g^{\mu\nu} = 2\eta^{\mu\nu}$ (derived without free parameters from Q8, Q10, Q11),
the paper establishes:

$$\mathcal{P}_\tau^{\mathrm{Q5b}}\,\Sigma_n^{\mathrm{tot}} = \sqrt{1 - B_n^2}$$

equivalently $\sqrt{\Sigma_n^{\mathrm{tot}} (2 - \Sigma_n^{\mathrm{tot}})}$,
and consequently:

$$\Phi(\eta_n^\tau) = \frac{1}{\sqrt{1 + (\eta_n^\tau)^2}} \longrightarrow \frac{1}{\gamma}$$

## Conceptual steps

1. **Capacity flow vector** — the O7 observable $B_n$ is identified as the magnitude
   of the spatial component of the normalised Born-Infeld capacity flow vector $\vec{F}_n$
   on $\mathbb{R}_\tau \times \mathrm{Heis}_3(\mathbb{R})$.

2. **BI sphere constraint** — the Born-Infeld admissibility budget forces $\vec{F}_n$
   onto the unit sphere: $|\vec{F}_n^{\mathrm{spat}}|^2 + (F_n^\tau)^2 = 1$.

3. **Temporal projection** — $\mathcal{P}_\tau^{\mathrm{Q5b}}$ is the Lorentzian
   orthogonal projection onto the temporal direction $\partial_\tau$, lifted from vectors
   to the scalar observable $\Sigma_n^{\mathrm{tot}}$ via the above identification.

4. **Explicit formula** — combining the linear filling law
   $\Sigma_n^{\mathrm{tot}} = 1 - B_n$ (Weil factorization, exact) with the BI sphere
   gives $F_n^\tau = \sqrt{1 - B_n^2}$.

## Key features

- The construction is **non-linear** in $\Sigma_n^{\mathrm{tot}}$: this follows from the
  quadratic BI budget, not from a modified projector.
- The temporal direction is **not** the central direction $\tilde{Z}$ of $\mathrm{Heis}_3$
  directly: it emerges from the co-metric completion chain
  CC structure $\to$ sub-principal corrections (Q8) $\to$ Q11 co-metric closure.
- The result is **exact** for all $n < q/2$, not merely asymptotic.

## Status

- Main theorem (formula for $\mathcal{P}_\tau^{\mathrm{Q5b}}$): **proved** (conditional on [U])
- Lorentz factor corollary: **proved** (conditional on [U])
- Sole conditional input: hypothesis [U], proved in U1

## Dependencies

| Paper | Role |
|-------|------|
| Q5b (`Beau2026q5b`) | Effective operator $L_{\mathrm{eff}}$ and co-metric extraction |
| Q11 (`Beau2026q11`) | $A_\tau = 2$, co-metric completion |
| Q10 (`Beau2026q10`) | $A_H = 2$, spatial isotropy |
| Q8 (`BeauQ8`) | $A_z = 2$, central-direction coefficient |
| U1 (`Beau2026u1`) | Proves hypothesis [U] |
| O7 (`Beau2026a11`) | Defines $B_n$ and $\Sigma_n^{\mathrm{tot}}$ |
| BI (`Beau2026c`) | Born-Infeld admissibility budget |
| LorCap (`Beau2026n`) | The conditional mechanism this paper closes |
| PTO (`Beau2026pto`) | Projective temporal ordering (structural context) |

## Repository Contents

```
temporal-projection/
├── out/              # Compiled PDF
├── tex/              # LaTeX source
│   ├── temporal-projection.tex
│   └── cosmochrony-bibliography.bib
├── compile.sh        # Compilation script
├── zenodo.json       # Zenodo metadata
└── README.md
```

## Citation

> J. Beau, *Temporal Residual Projection from the Completed Principal Symbol:
> Explicit Construction of the Temporal Projection Operator and the Lorentz Identification*,
> Preprint, 2026.

## Acknowledgements

Portions of the editorial refinement benefited from iterative interactions with
large language models used as analytical assistants.
All claims, interpretations, and final formulations remain the sole
responsibility of the author.
