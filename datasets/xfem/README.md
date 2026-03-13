# XFEM fracture datasets

This directory contains datasets produced by **Extended Finite Element Method
(XFEM)** fracture simulations. XFEM enriches the standard FEM basis to
represent discontinuities without re-meshing.

## Contents

| Series | Description |
|---|---|
| *(empty – add your first dataset)* | |

## Common parameters

| Parameter | Symbol | Typical units |
|---|---|---|
| Elastic modulus | E | Pa |
| Poisson's ratio | ν | – |
| Fracture toughness | K_Ic | Pa·√m |
| Enrichment radius | r_e | m |

## Adding a dataset

Follow the instructions in [CONTRIBUTING.md](../../CONTRIBUTING.md) and create
a subdirectory here, e.g.:

```
datasets/xfem/penny-shaped-crack-mode-i/
├── README.md
├── params.yaml
└── results.h5          # tracked by Git-LFS
```
