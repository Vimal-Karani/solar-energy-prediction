# Solar Energy Production Prediction

A machine learning regression project that estimates **annual photovoltaic (PV) energy production in kWh** for solar projects.

## Project Overview

The model uses project-level information such as location, utility, developer, PV system size, storage, metering information, and dates.

The workflow includes:

- Data inspection and exploratory analysis
- Data cleaning
- Duplicate removal
- Date processing
- Feature engineering
- Numerical and categorical preprocessing
- Random Forest regression
- Model evaluation using MAE, RMSE, and R²
- Feature importance analysis
- Comparison of models with and without PV system-size variables

## Model

**Random Forest Regressor**

The final model includes PV system size because system capacity is a meaningful input when estimating the expected production of a known or proposed solar installation.

A second experiment removes the direct system-size variables to understand how much predictive information comes from the remaining project and location features.

## Files

- `Solar_Energy_Production_Prediction_Polished.ipynb` — polished Google Colab notebook
- `README.md` — project documentation
- `requirements.txt` — Python dependencies

## Running the Notebook

The notebook was designed for **Google Colab**.

1. Open the notebook in Google Colab.
2. Mount Google Drive.
3. Update `DATA_PATH` if your dataset is stored elsewhere.
4. Run the notebook from top to bottom.
5. Review the model evaluation, feature importance, and comparison results.

## Key Learning Outcomes

This project demonstrates:

- Regression modelling
- Data cleaning
- Feature engineering
- Date-based feature creation
- Categorical preprocessing
- Random Forest regression
- Model evaluation
- Feature importance analysis
- Comparing alternative feature sets

## Important Limitation

The dataset does not directly contain detailed irradiance, weather, panel orientation, tilt, or other physical variables required for a complete solar-production simulation.

Therefore, the model should be described as a **machine learning estimate based on available project information**, rather than a full physical solar-energy simulation.
