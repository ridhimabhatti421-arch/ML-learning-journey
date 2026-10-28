# Linear Regression: Seoul Bike Sharing Demand

Part of my [ML-learning-journey](../README.md). This notebook predicts how many bikes are rented at noon from weather conditions, using regression models built with scikit-learn and TensorFlow.

## Dataset
[Seoul Bike Sharing Demand](https://archive.ics.uci.edu/dataset/560/seoul+bike+sharing+demand) (UCI Machine Learning Repository). Hourly rental counts alongside weather data such as temperature, humidity, wind speed, visibility, dew point, solar radiation, rainfall and snowfall.

## What's covered
1. Dataset: loading ('latin-1' encoding), renaming columns, encoding 'functional', and filtering to 'hour == 12'
2. Exploration: scatter plots of each feature against bike count, used to drop weak features ('wind', 'visibility', 'functional')
3. Train / Validation / Test split: 60% / 20% / 20%
4. Simple linear regression: bike count vs. temperature
5. Multiple linear regression: all remaining features
6. Regression with a neural network: a Keras 'Normalization' + 'Dense' model on temperature, trained for 1000 epochs with Adam

## Results (R² on the test set)

| Model              | Features         | R² |
|--------------------|------------------|----|
| Linear regression  | temperature only  | 0.17 |
| Mul lin regression | all remaining features | 0.55 |

Using more features helps a lot compared to temperature alone. The neural network on temperature alone reaches a similar fit to the simple linear regression, which shows that one feature is the real limit here.

## Files
- Lin-Reg.ipynb: notebook with code and outputs
- SeoulBikeData.csv: the dataset

## Tech stack
Python, pandas, NumPy, Matplotlib, Seaborn, scikit-learn, imbalanced-learn, TensorFlow/Keras

## Run it yourself
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn tensorflow
jupyter notebook
```
Open Lin-Reg.ipynb and run all cells.
