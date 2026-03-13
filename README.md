# numerical-fracture-datasets

A curated collection of numerical datasets from fracture mechanics experiments,
covering multiple approaches, models, and sources.

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
<!-- A Zenodo DOI badge will appear here after the first tagged release is deposited. -->

---

## Overview

This repository stores datasets produced by numerical simulations of fracture
mechanics problems. Experiments may originate from different models, software
frameworks, or research groups. Each dataset series lives in its own
subdirectory of [`datasets/`](datasets/) and is documented by a local
`README.md`.

Supported approaches include (but are not limited to):

| Approach | Directory |
|---|---|
| Phase-field fracture | [`datasets/phase-field/`](datasets/phase-field/) |
| Cohesive zone models | [`datasets/cohesive-zone/`](datasets/cohesive-zone/) |
| Extended FEM (XFEM) | [`datasets/xfem/`](datasets/xfem/) |

---

## Repository layout

```
numerical-fracture-datasets/
├── .gitattributes        # Git-LFS tracking rules for binary/large data files
├── .gitignore
├── .zenodo.json          # Zenodo deposit metadata
├── CITATION.cff          # Machine-readable citation metadata
├── LICENSE               # CC BY 4.0
├── README.md             # This file
├── CONTRIBUTING.md       # How to contribute a new dataset
├── datasets/
│   ├── phase-field/      # Phase-field fracture datasets
│   │   └── README.md
│   ├── cohesive-zone/    # Cohesive zone model datasets
│   │   └── README.md
│   └── xfem/             # XFEM datasets
│       └── README.md
├── docs/                 # Extended documentation and references
└── scripts/              # Utility scripts for loading / validating data
```

---

## Getting started

### Prerequisites

- [Git](https://git-scm.com/) ≥ 2.x
- [Git-LFS](https://git-lfs.github.com/) ≥ 3.x  
  Install once with:
  ```bash
  git lfs install
  ```

### Clone the repository (with LFS data)

```bash
git clone https://github.com/kumiori/numerical-fracture-datasets.git
cd numerical-fracture-datasets
```

Git-LFS pointers are resolved automatically on clone if Git-LFS is installed.
To download only the LFS objects you actually need:

```bash
git lfs pull --include="datasets/phase-field/**"
```

### Clone without LFS data (metadata / code only)

```bash
GIT_LFS_SKIP_SMUDGE=1 git clone https://github.com/kumiori/numerical-fracture-datasets.git
```

---

## Data organisation

Each experiment series is stored under `datasets/<approach>/<series-name>/`
and must contain at minimum:

- `README.md` – description, provenance, parameter table, and citation
- The actual data files (tracked by Git-LFS)

Suggested additional files per series:

- `params.json` / `params.yaml` – machine-readable simulation parameters
- `load_data.py` – minimal Python snippet to load and plot the data

See [CONTRIBUTING.md](CONTRIBUTING.md) for the full checklist.

---

## Data formats

All binary and large files are tracked with **Git-LFS** (see
[`.gitattributes`](.gitattributes)). Supported formats include:

| Format | Extension(s) | Typical source |
|---|---|---|
| HDF5 | `.h5`, `.hdf5` | FEniCS, h5py |
| NetCDF | `.nc`, `.nc4` | generic |
| XDMF + HDF5 | `.xdmf`, `.h5` | FEniCS/DOLFINx |
| VTK / ParaView | `.vtu`, `.vtk`, `.pvd` | OpenFOAM, FEniCS |
| NumPy | `.npy`, `.npz` | NumPy |
| MATLAB | `.mat` | MATLAB / SciPy |
| CSV / TSV | `.csv`, `.tsv` | generic |

---

## Zenodo archiving

Every tagged release is automatically deposited on **Zenodo** via the
`.zenodo.json` metadata file. After the first deposit the Zenodo DOI badge
can be added to the top of this README.

To create a new citable release:

1. Update `.zenodo.json` if metadata has changed.
2. Create an annotated tag and push it:
   ```bash
   git tag -a v0.1.0 -m "Initial dataset release"
   git push origin v0.1.0
   ```
3. The Zenodo webhook (configured in the repository settings) will create the
   deposit automatically.

---

## Citation

If you use these datasets in your research, please cite them using the
information in [`CITATION.cff`](CITATION.cff) or the Zenodo DOI above.

---

## Contributing

Contributions of new datasets, corrections, and documentation improvements are
welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull
request.

---

## License

Data and documentation are released under the
[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE) license.