# ResNet Practice

A hands-on machine learning project for learning and experimenting with Residual Networks (ResNet) on the CIFAR-10 dataset. The repository is organized as a lightweight data-science template and includes notebook-based training workflows for multiple ResNet configurations.

<p align="center">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.12-3776AB?logo=python&logoColor=white" />
  <img alt="TensorFlow" src="https://img.shields.io/badge/TensorFlow-2.x-FF6F00?logo=tensorflow&logoColor=white" />
  <img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-2.x-EE4C2C?logo=pytorch&logoColor=white" />
  <img alt="CIFAR-10" src="https://img.shields.io/badge/Dataset-CIFAR--10-5A67D8" />
</p>

## Overview

This project is designed as a practice repository for:

- building and evaluating ResNet architectures,
- exploring transfer learning and fine-tuning,
- working with CIFAR-10 image data,
- following a clean project structure for reproducible ML work.

The codebase includes notebook experiments and a template layout meant to make it easy to extend with custom data pipelines, model training logic, and reporting.

## Repository contents

- `notebooks/` — Jupyter notebooks for model experimentation and training
- `src/` — project code scaffolding for dataset, training, plotting, and model utilities
- `data/` — raw, interim, processed, and external datasets
- `models/` — trained model artifacts and checkpoints
- `reports/` — generated analysis outputs and figures
- `references/` — attribution and licensing notes for third-party sources
- `.env.example` — example environment configuration
- `requirements.txt` / `pyproject.toml` — project dependencies

## Notebooks

This repository currently includes:

- `notebooks/resnet-20.ipynb`
- `notebooks/resnet-50.ipynb`
- `notebooks/resnet-50-cifar10-finetune.ipynb`

These notebooks are intended as experimentation endpoints for training and comparing ResNet models and fine-tuned variants.

## Project structure

```text
.
├── .env.example
├── .gitignore
├── .python-version
├── LICENCE
├── README.md
├── pyproject.toml
├── requirements.txt
├── uv.lock
├── data/
│   ├── external/
│   ├── interim/
│   ├── processed/
│   └── raw/
├── models/
├── notebooks/
│   ├── resnet-20.ipynb
│   ├── resnet-50.ipynb
│   └── resnet-50-cifar10-finetune.ipynb
├── references/
│   └── third_party_attributions.md
├── reports/
│   └── figures/
└── src/
    ├── __init__.py
    ├── config.py
    ├── dataset.py
    ├── features.py
    ├── modeling/
    │   ├── __init__.py
    │   ├── predict.py
    │   └── train.py
    ├── plots.py
    └── services/
        └── __init__.py
```

## Getting started

### 1. Clone the repository

```bash
git clone https://github.com/Antaun/resnet-practice.git
cd resnet-practice
```

### 2. Create a virtual environment

Using Python 3.12:

```bash
python -m venv .venv
source .venv/bin/activate
```

On Windows PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

Or with `uv`:

```bash
uv sync
```

### 4. Configure environment variables

Copy the example env file and update it as needed:

```bash
cp .env.example .env
```

## Data setup

This repository expects image data such as CIFAR-10 to be placed in the `data/` folder, typically under `data/raw/` or according to your preferred preprocessing workflow. The repo is structured for a standard data science pipeline, but the actual dataset files are not committed by default.

## Training and experimentation

Open the notebooks in `notebooks/` to run experiments, inspect model behavior, and evaluate training outcomes.

Typical workflow:

1. Prepare or download the dataset.
2. Run a notebook to train a ResNet model.
3. Save artifacts to `models/`.
4. Review plots and reports in `reports/`.

## Notes on provenance and licensing

This project includes a residual-network implementation inspired by public examples from the Keras and deep-learning ecosystem. The repository is intended for education and experimentation, and any third-party sources, dataset references, and licensing information are documented in:

- `references/third_party_attributions.md`
- `LICENCE`

## Recommended next steps

- add a reproducible training script under `src/modeling/train.py`,
- implement dataset loading in `src/dataset.py`,
- add evaluation metrics and visualizations in `src/plots.py`,
- log experiment results and model artifacts in `models/`.

## License

This project is distributed under the repository's license file (`LICENCE`), with additional attribution details recorded in the references folder.

## Contributing

This repository is intended as a learning and experimentation space. If you extend the notebooks or add reusable training pipelines, keep the project structure organized and document any external data or third-party code used.
