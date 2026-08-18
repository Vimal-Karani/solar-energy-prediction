# Solar Energy Production Prediction

Machine learning internship project that predicts estimated annual PV energy production (kWh).

## Files

- `Solar_Energy_Production_Prediction_Polished.ipynb` — Google Colab notebook
- `app.py` — Streamlit application
- `solar_energy_model.pkl` — trained Random Forest pipeline
- `model_metadata.json` — model metrics and settings
- `feature_importance.csv` — feature importance results
- `model_comparison.csv` — comparison with and without PV system size
- `requirements.txt` — Streamlit dependencies

## Run locally

1. Put all files in the same folder.
2. Open a terminal in that folder.
3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Start Streamlit:

```bash
streamlit run app.py
```

5. Open the local URL shown by Streamlit, normally `http://localhost:8501`.

## Google Colab

The notebook keeps the original Google Drive workflow. Upload the CSV to the Drive folder specified by `DATA_PATH`, then run the notebook from top to bottom.

The final cells save the trained model and metadata to Google Drive.

## Important project note

The final model includes PV system size because system capacity is a valid input when estimating expected annual production for a known installation.

A second Random Forest experiment removes both PV system-size variables. This produces a much lower R² and demonstrates that the remaining project/location information is less predictive.

The dataset does not directly include detailed irradiance, weather, panel orientation or tilt variables, so this should be presented as a machine-learning estimate based on the available project data rather than a full physical solar simulation.
