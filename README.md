# Air Quality Analysis

## Project Overview
This project aims to analyze air quality data and predict Air Quality Index (AQI) using machine learning models. The analysis focuses on exploring key pollutants and their impact on air quality across various cities.

## Features
- **Data Preprocessing**: Handles missing values using imputation techniques and performs feature engineering, such as combining pollutants into new features.
- **Data Visualization**: Visualizations are used to understand the trends in pollutant levels and AQI across different time periods and locations.
- **Machine Learning Models**: Gradient Boosting and Random Forest algorithms are used to predict AQI based on pollutant levels and other environmental factors.
- **Model Evaluation**: Performance is evaluated using metrics such as Mean Squared Error (MSE), and the results are visualized with comparison graphs between actual and predicted AQI values.

## Dataset
The dataset `city_day.csv` includes air quality data with the following columns:
- **Date**: Date of the measurement.
- **PM2.5, PM10**: Particulate matter concentrations.
- **NO2, CO, SO2, O3**: Levels of key pollutants.
- **AQI**: Air Quality Index.
- **AQI_Bucket**: Categorical air quality rating.

## Requirements
To run the project, you will need the following Python libraries:
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `sklearn`

You can install the required packages using:
```bash
pip install -r requirements.txt
```

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/air_quality_analysis.git
   ```
2. Run the Jupyter Notebook `Air_Quality_Project.ipynb` for the analysis and modeling steps.

## File Structure
- `Air_Quality_Project.ipynb`: Jupyter Notebook containing the code for data analysis, preprocessing, and modeling.
- `city_day.csv`: Air quality dataset.
- `newCityData.csv`: Processed dataset after feature engineering.

## Visualizations
The project includes visualizations such as:
- Time-series plots of AQI and pollutant levels.
- Comparisons of actual vs. predicted AQI values from different models.

## Conclusions and Findings

### 1. **Impact of Particulate Matter on AQI**
   - Both **PM2.5** and **PM10** (particulate matter with diameters less than 2.5 and 10 micrometers, respectively) significantly contribute to the degradation of air quality. High levels of these pollutants often correlate with a poor AQI.
   
### 2. **Pollutant Combinations and Feature Engineering**
   - By aggregating the pollutants like Benzene, Toluene, and Xylene into a single metric (**BTX**) and combining particulate matter measurements, new features were engineered that help in more accurate AQI predictions. These feature combinations provide insights into the cumulative effects of various pollutants on air quality.
   
### 3. **Model Performance**
   - Machine learning models, specifically **Linear Regression**, **Gradient Boosting** and **Random Forest**, were used for predicting AQI. **Linear Regression** and **Random Forest** showed promising results in predicting AQI, with **Random Forest** slightly outperforming Linear Regression in terms of lower mean squared error and better prediction accuracy.
   
### 4. **Visualization Insights**
   - The visualizations of actual vs. predicted AQI highlighted that the models were able to capture general trends and patterns in the data, though some outliers and extreme cases were harder to predict.
   - The time-series plots revealed significant seasonal variations in AQI and pollutant levels, with certain months showing spikes in pollution levels, likely due to increased vehicular emissions or industrial activity during those periods.

### 5. **Categorical Air Quality Trends**
   - The `AQI_Bucket` analysis revealed that most of the cities studied frequently fall into the **'Satisfactory'** or **'Moderate'** categories, though there are occasional periods of **'Poor'** air quality, particularly during certain seasons or in highly industrialized cities.



