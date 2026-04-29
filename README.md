# 🌍 Agrofood CO₂ Emissions — Analysis Notebook

Exploratory data analysis and machine learning on global agrifood CO₂ emissions (1990–2020).

---

## Requirements

- Python 3.8+
- Jupyter Notebook or JupyterLab

---

## Setup

**1. Install dependencies**
```bash
pip install pandas numpy matplotlib seaborn plotly scipy scikit-learn xgboost lightgbm tqdm jupyter
```

**2. Add the dataset**

Place `Agrofood_co2_emission.csv` in the same folder as the notebook.  
If it is saved elsewhere, update the path in **Cell 3**:
```python
df = load_raw_data("your/path/to/Agrofood_co2_emission.csv")
```

**3. Launch the notebook**
```bash
jupyter notebook ITS68404_0362477_Code.ipynb
```

**4. Run all cells**

Go to `Kernel → Restart & Run All` to execute the full pipeline from top to bottom.

---

## What the notebook does

| Step | Description |
|------|-------------|
| 1–2  | Load and inspect the raw dataset |
| 3    | Clean data — remove duplicates, impute missing values, map continents |
| 4    | Engineer features — per-capita emission, urban ratio, rolling averages |
| 5    | Reshape and aggregate data for analysis |
| 6    | EDA — 10 interactive Plotly charts (trends, heatmaps, 3D scatter, KDE, etc.) |
| 7    | Advanced visualizations — choropleth maps, animations, Sankey diagram |
| 8    | Machine learning — train/evaluate 8 regression models to predict temperature |

---

## Notes

- All charts are interactive (hover, zoom, filter) — best viewed inside Jupyter.
- The train/test split is **temporal**: data before 2016 is used for training, 2016 onward for testing.
- Countries not matched to a continent are labelled `"Other"` and excluded from continent-level plots.
