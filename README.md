# Gaussian Processes – Notebooks

This repository contains notebooks for learning, visualizing, and experimenting with Gaussian Processes (GPs) and common kernels (e.g., RBF).

## Repository Structure

- Notebooks
  - `Gaussian_process.ipynb`: Main report-style notebook with theory, methodology, and experiments.
  - `code_visualization.ipynb`: Visualization playground (RBF effects, prior vs posterior intuition, polynomial priors, kernel comparisons, etc.).

- Presentation
  - `Gaussian Process.pptx`: Slides summarizing concepts, visuals, and results.

## Setup

1) Create/activate a Python 3.9+ environment.

2) Install dependencies:

```
pip install -r requirements.txt
```

`requirements.txt` includes: numpy, matplotlib, scikit-learn, scipy. For running notebooks, you may also need:

```
pip install jupyterlab
```

## How to Use

- Open `Gaussian_process.ipynb` or `code_visualization.ipynb` in Jupyter Lab/Notebook and run cells top-to-bottom.
- Use the presentation `Gaussian Process.pptx` for a high-level summary of results and visuals.

## Tips (scikit-learn)

- Composite kernel parts are accessible as `k1`/`k2` (e.g., `C * RBF`).
- Print kernel before/after fitting to see optimized values:

```
print("Initial kernel:", gp.kernel_)
gp.fit(X_train, y_train)
print("Optimized kernel:", gp.kernel_)
```

## Notes

- Start with `Gaussian_process.ipynb` for the full narrative.
- Ensure the working directory is the repo root when running notebooks.
