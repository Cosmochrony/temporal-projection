# Temporal Residual Map from the Completed Principal Symbol

This repository contains the source of the paper
*Temporal Residual Map from the Completed Principal Symbol:
Construction, Uniqueness, and the Lorentz Identification*
(TempProj of the Lorentz Capacity sub-programme).

## Overview

The companion paper **LorentzCapacity** (`Beau2026n`) identifies the construction of a temporal
residual map $\mathcal{P}_\tau^{\mathrm{Q5b}}$ as the remaining step to close the Lorentz
identification from O7 observables, but defers its explicit construction.

The present paper carries out this construction and proves the map is the **unique** positive
function compatible with three inputs simultaneously:

1. **(L) Lorentzian splitting** — the Q5b completed co-metric $g^{\mu\nu} = 2\eta^{\mu\nu}$
   determines a unique timelike direction $\partial_\tau$.
2. **(BI) Born-Infeld capacity sphere** — the admissible capacity flow vector $\vec{F}_n$
   lies on the unit sphere $(F_n^\tau)^2 + |\vec{F}_n^{\mathrm{spat}}|^2 = 1$.
3. **(W) Weil filling law** — $\Sigma_n^{\mathrm{tot}} = 1 - B_n$ exactly.

## Main Result

$$\mathcal{P}_\tau^{\mathrm{Q5b}}\,\Sigma_n^{\mathrm{tot}}
= \sqrt{\Sigma_n^{\mathrm{tot}}\bigl(2 - \Sigma_n^{\mathrm{tot}}\bigr)}
= \sqrt{1 - B_n^2}$$

Consequently:
$$\Phi(\eta_n^\tau) = \frac{1}{\sqrt{1+(\eta_n^\tau)^2}} \longrightarrow \frac{1}{\gamma}$$

The three inputs are **individually necessary**: removing any one leaves the formula
undetermined. This explains retroactively the numerical failure of all three candidates
tested in LorentzCapacity.

## Status

- Main theorem (uniqueness + explicit formula): **proved** (conditional on [U])
- Lorentz factor corollary: **proved** (conditional on [U])
- Three-input necessity (Proposition~\ref{prop:failure}): **proved**

## Position in the sub-programme

```
LorCap → TempProj → LCII
```

TempProj closes the open problem of LorCap. LCII (`Beau2026lco2`) extends the result
to non-homogeneous regimes (gravitational time dilation).

## Dependencies

| Paper | Role |
|-------|------|
| LorCap (`Beau2026n`) | Origin of the open problem |
| Q5b (`Beau2026q5b`) | Effective operator and co-metric |
| Q11 (`Beau2026q11`) | $A_\tau = 2$, co-metric completion |
| Q10 (`Beau2026q10`) | $A_H = 2$, spatial isotropy |
| Q8 (`BeauQ8`) | $A_z = 2$, central-direction coefficient |
| U1 (`Beau2026u1`) | Proves hypothesis [U] |
| O7 (`Beau2026a11`) | Defines $B_n$ and $\Sigma_n^{\mathrm{tot}}$ |
| BI (`Beau2026c`) | Born-Infeld admissibility budget |
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
