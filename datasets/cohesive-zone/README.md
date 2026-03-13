# Cohesive zone model datasets

This directory contains datasets produced by **cohesive zone model (CZM)**
simulations. CZMs represent fracture through traction-separation laws along
potential crack surfaces.

## Contents

| Series | Description |
|---|---|
| *(empty – add your first dataset)* | |

## Common parameters

| Parameter | Symbol | Typical units |
|---|---|---|
| Peak traction | t_max | Pa |
| Critical separation | δ_c | m |
| Fracture energy | G_f | J/m² |
| Cohesive law shape | – | – |

## Adding a dataset

Follow the instructions in [CONTRIBUTING.md](../../CONTRIBUTING.md) and create
a subdirectory here, e.g.:

```
datasets/cohesive-zone/exponential-law-mode-i/
├── README.md
├── params.yaml
└── results.h5          # tracked by Git-LFS
```
