# Phase-field fracture datasets

This directory contains datasets produced by **phase-field (damage) fracture**
simulations. The phase-field approach regularises the sharp crack into a
diffuse damage zone controlled by a length-scale parameter ℓ.

## Contents

| Series | Description |
|---|---|
| *(empty – add your first dataset)* | |

## Common parameters

| Parameter | Symbol | Typical units |
|---|---|---|
| Elastic modulus | E | Pa |
| Poisson's ratio | ν | – |
| Critical energy release rate | G_c | J/m² |
| Length-scale | ℓ | m |

## Adding a dataset

Follow the instructions in [CONTRIBUTING.md](../../CONTRIBUTING.md) and create
a subdirectory here, e.g.:

```
datasets/phase-field/at2-single-edge-notch/
├── README.md
├── params.yaml
└── results.h5          # tracked by Git-LFS
```
