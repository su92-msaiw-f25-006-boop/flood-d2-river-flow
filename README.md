# Pakistan River Flow and Reservoir Forecasting (2021–2025)

This repository provides daily hydrological records and machine learning forecasting models for Pakistan's major river inflow points and dam reservoirs (2021–2025). The data tracks daily inflows and storage levels across the Indus River (Tarbela Dam), Kabul River (Nowshera), Jhelum River (Mangla Dam), and Chenab River (Marala Barrage) to predict next-day and multi-day ahead streamflow using Linear Regression, Random Forest, XGBoost, and LSTM neural architectures.

## Folder Structure

```
flood-d2-river-flow/
├── 1_code/
│   └── River_Flow_Forecast_Pakistan.ipynb  # Notebook: date reconstruction, EDA, and models
├── 2_kaggle_input/
│   ├── Pakistans-Rivers_data.csv           # Raw daily river flow monitoring dataset
│   └── Pakistans_Rivers_Flow_data.csv      # Complementary hydrological flow log
├── 3_kaggle_output/
│   └── Dataset_2_River_Flow_OUTPUT.ipynb   # Executed notebook with model outputs and plots
├── 4_doc/
│   └── Dataset 2 - Pakistan River Flow Forecasting - Results.docx # Experimental summary report
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## How to Run

1. **Prerequisites:** Python 3.10 or higher.
2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Notebook:**
   ```bash
   jupyter notebook 1_code/River_Flow_Forecast_Pakistan.ipynb
   ```

The pipeline handles calendar year reconstruction from day-month strings (aligning 1,731 observation days across 2021–2025), fits scalers on the training period (2021–2023), and benchmarks models out-of-time on 2024–2025 test records.

## Data Source and Licence

- **Primary Source:** Kaggle dataset *"Pakistan's Rivers Flow Data at different Dams"* uploaded by Syed Asim Ali Shah.
  - Dataset link: [https://www.kaggle.com/datasets/syedasimalishah/pakistans-rivers-flow-data-at-different-dams](https://www.kaggle.com/datasets/syedasimalishah/pakistans-rivers-flow-data-at-different-dams)
  - Underlying monitoring bodies: Indus River System Authority (IRSA) and Pakistan Flood Forecasting Division (FFD).
- **Data Licence:** Creative Commons CC0 1.0 Universal (Public Domain Dedication).
- **Code Licence:** The code in this repository is released under the [MIT License](LICENSE).

## Citation

```bibtex
@misc{anwar2026_river_flow,
  author = {Shahan Anwar},
  title = {Pakistan River Flow and Reservoir Forecasting (2021--2025)},
  year = {2026},
  publisher = {GitHub},
  howpublished = {\url{https://github.com/su92-msaiw-f25-006-boop/flood-d2-river-flow}}
}
```
