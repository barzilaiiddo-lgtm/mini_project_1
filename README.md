# Mini-Project 1 | From Data Generation to Scientific Analysis

Q1 simulates and compares neural spike patterns. Q2 explores laptop listings and their prices in euros.

## Run the notebooks

From the project folder, create a Python environment, install the dependencies, and launch JupyterLab.

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m jupyterlab
```

Open either notebook in JupyterLab. Run the selected cell with **Shift+Enter** or use **Run → Run All Cells** to execute the notebook in order.

- `Q1_neural_spikes.ipynb` covers regular, irregular, and bursting neural spike patterns.
- `Q2_laptop_analysis.ipynb` reads `laptop_price_dataset .csv` from the project folder. The filename includes a space before `.csv`.
- `figures/` holds exported plots.
- `AI_USAGE.md` records AI assistance and verification.
