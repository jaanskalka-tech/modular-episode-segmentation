# Modular Framework for Episode Segmentation

Reproducibility repository for the manuscript **A Modular Framework for Episode Segmentation and Temporal Pattern Discovery in Multidimensional Time Series**.

## Repository structure

```text
.
├── notebooks/          # Main Jupyter notebooks
├── data/
│   ├── raw/            # Input data (not for public sharing if sensitive)
│   └── processed/      # Derived datasets
├── outputs/            # Figures, tables, exported results
├── src/                # Optional helper scripts
├── docs/               # Supplementary documentation
├── requirements.txt    # Python dependencies
├── environment.yml     # Conda environment (optional)
├── .gitignore
└── LICENSE
```

## Quick start

### Option 1: pip

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab
```

### Option 2: conda

```bash
conda env create -f environment.yml
conda activate modular-episode-segmentation
jupyter lab
```

## Suggested workflow

1. Put the main notebook into `notebooks/`.
2. Put small, shareable example inputs into `data/raw/`.
3. Put generated intermediate datasets into `data/processed/`.
4. Save figures and tables into `outputs/`.
5. If some data are large or restricted, do **not** store them directly in Git. Use Git LFS or keep them outside the repository and describe access in `docs/data_access.md`.

## Data sharing note

If your input files contain large binaries or sensitive data, use one of these options:
- keep only a small demo sample in the repository,
- publish full data elsewhere and link them here,
- or use Git LFS for large files.

## Minimal reproduction checklist

- [ ] notebook runs from top to bottom
- [ ] dependencies are listed
- [ ] input data locations are documented
- [ ] outputs can be regenerated
- [ ] random seeds are fixed where relevant
- [ ] private data are excluded

## Citation

If you use this repository, cite the related manuscript and link the repository version used for the analysis.
