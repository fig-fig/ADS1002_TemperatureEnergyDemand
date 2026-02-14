# Temperature & Energy Demand Modelling
### ADS1002 Data Challenges 2 | Semester 2 2022

## Introduction

This project investigates how **air temperature affects energy demand in Victoria (Melbourne)**.  
Using half-hourly weather and electricity demand data (2014–2019), multiple regression and forecasting models were developed to predict energy consumption based on temperature and historical trends.

## Variables

### Target Variable
- `TOTALDEMAND` (Energy demand in Victoria)

### Main Feature
- `Air Temperature (°C)` – Olympic Park Weather Station (Melbourne)

### Additional Time Variable
- `dateTime` (Half-hourly timestamp)


## Project Workflow

1. **Data Wrangling & Cleaning**
   - Combined 72 monthly demand files
   - Filtered Olympic Park weather data (2014–2019)
   - Converted timestamps
   - Removed irregular time intervals
   - Merged datasets using `pd.merge`

2. **Exploratory Data Analysis**
   - Demand vs Temperature (seasonality patterns)
   - Summer vs Winter daily comparisons

3. **Modelling Techniques**

   - **Linear Regression**
     - Very low R² (~0.026)
   
   - **Multivariate Polynomial Regression (Degree 4)**
     - RMSE ≈ 804.86  
     - R² ≈ 0.183  

   - **Random Forest Regression**
     - n_estimators = 1000  
     - RMSE ≈ 797.4  
     - R² ≈ 0.19  

   - **Neural Prophet Forecasting (Time-Series)**
     - Forecasted temperature & demand  
     - Demand RMSE ≈ 529 (Best performing model)

4. **Evaluation**
   - Train–Test Split
   - RMSE (Root Mean Squared Error)
   - MAE (Mean Absolute Error)
   - R² Score

<br>

---

## Built With

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Deepnote](https://img.shields.io/badge/Deepnote-3793EF?style=for-the-badge&logo=deepnote&logoColor=white)
![Matplotlib](https://img.shields.io/badge/matplotlib-11557C?style=for-the-badge)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![NeuralProphet](https://img.shields.io/badge/NeuralProphet-FF6F00?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

## License

This project was developed for academic purposes 2022.  
If reused or distributed, please provide proper academic attribution.
