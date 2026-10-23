# RMT-IoT

Jupyter notebook for IoT network-traffic classification using CICIoT23 data.
Compares Logistic Regression, K-Nearest Neighbors, Random Forest and XGBoost
using stratified cross-validation and held-out validation/test evaluation.

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab RMT_IoT.ipynb
```

On macOS, XGBoost may require OpenMP: `brew install libomp`.

## Data and execution

Place `CICIOT23.zip` in the repository root, or set `DATA_PATH` in the notebook
to your archive or extracted dataset directory. The dataset must contain
`train.csv`, `validation.csv` and `test.csv` with the schema expected by the notebook.
The dataset is not included in this repository.

Run the notebook cells in order. Metrics, figures, predictions and the fitted
model are written to a timestamped directory under `assignment3_results/`.
The notebook includes saved outputs from the existing local run. Dependencies
are not pinned; results may vary with package versions.

The virtual environment, dataset archives and generated result folders are
excluded from Git.
