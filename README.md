# Air Quality Prediction Using LSTM

## Overview

Project ini bertujuan memprediksi konsentrasi PM2.5 menggunakan model Long Short-Term Memory (LSTM) berdasarkan data kualitas udara dari stasiun Aotizhongxin, Beijing.

Model dikembangkan menggunakan pendekatan time series forecasting dengan memanfaatkan beberapa faktor lingkungan seperti PM10, CO, NO2, SO2, dan DEWP sebagai fitur prediktor.



## Dataset

Dataset: Beijing Multi-Site Air Quality Dataset

Data difokuskan pada stasiun pengamatan Aotizhongxin untuk menjaga konsistensi analisis time series.

Dataset tidak disertakan dalam repository karena ukuran file yang cukup besar.



## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib
- Seaborn



## Project Workflow

### Exploratory Data Analysis (EDA)

- Analisis distribusi PM2.5
- Analisis tren time series
- Identifikasi missing values
- Analisis korelasi antar fitur

### Data Preprocessing

- Feature Selection
- Missing Value Handling
- Min-Max Scaling
- Sequence Generation (24-Hour Window)

### Model Development

- Long Short-Term Memory (LSTM)
- Adam Optimizer
- Mean Squared Error Loss Function

### Model Evaluation

- MAE (Mean Absolute Error)
- MSE (Mean Squared Error)
- R² Score

### Time Series Cross Validation

- TimeSeriesSplit (5 Fold)
- Generalization Testing



## Results

### Test Performance

| Metric | Value |
|----------|----------|
| MAE | 17.21 |
| MSE | 875.95 |
| R² Score | 0.8748 |

### TimeSeriesSplit 5-Fold Validation

| Metric | Average |
|----------|----------|
| MAE | 20.35 |
| MSE | 1052.75 |
| R² Score | 0.8440 |

## Visualization

### Prediction vs Actual PM2.5

Model berhasil mengikuti pola aktual PM2.5 dengan cukup baik pada data pengujian.

![Prediction vs Actual](images/Prediksi%20vs%20Aktual%20(Sample).png)

### Training Loss

Kurva training menunjukkan model berhasil mempelajari pola data selama proses pelatihan.

![Training Loss](images/Training%20Loss.png)

### LSTM vs RNN Comparison

Perbandingan performa menunjukkan LSTM menghasilkan nilai MAE dan MSE yang lebih rendah serta R² yang lebih stabil dibandingkan RNN pada sebagian besar fold validasi.

![LSTM vs RNN](images/Perbandingan%20LSTM%20vs%20RNN.png)

## Key Findings

- LSTM mampu memprediksi konsentrasi PM2.5 dengan performa yang baik.
- Model menjelaskan sekitar 87% variasi data pada pengujian.
- Performa model stabil pada validasi TimeSeriesSplit 5-Fold.
- LSTM menunjukkan performa yang lebih baik dibandingkan RNN pada seluruh fold evaluasi.



## Author

Irma Innayah
