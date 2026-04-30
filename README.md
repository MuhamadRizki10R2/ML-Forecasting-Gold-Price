📈 Gold Price Forecasting: A Professional Quant Approach
![alt text](https://img.shields.io/badge/Python-3.8%2B-blue)

![alt text](https://img.shields.io/badge/TensorFlow-2.x-orange)

![alt text](https://img.shields.io/badge/License-MIT-yellow.svg)

Proyek ini mendemonstrasikan implementasi Deep Learning (LSTM) untuk memprediksi harga emas (Gold Futures GC=F) menggunakan pendekatan finansial profesional. Alih-alih memprediksi harga absolut secara langsung, model ini memprediksi Daily Returns untuk memastikan stasioneritas data, menghasilkan akurasi prediksi yang sangat tinggi.

🎯 Key Highlights
Metode Quant: Mengubah data Non-Stationary (Harga) menjadi Stationary (Returns) untuk performa model yang stabil.

Multivariate Forecasting: Menggunakan 15+ fitur termasuk indikator teknikal: RSI, MACD, Bollinger Bands, Moving Averages, dan Volatility.

Pencegahan Data Leakage: Implementasi StandardScaler yang ketat (hanya di-fit pada data training).

Akurasi Tinggi: Mencapai Mean Absolute Error (MAE) sebesar ~
39
∗
∗
p
a
d
a
h
a
r
g
a
a
s
e
t
s
e
n
i
l
a
i
∗
∗
39∗∗padahargaasetsenilai∗∗
5,000+.

📂 Dataset
Dataset bersumber dari Yahoo Finance via Kaggle, mencakup 5 tahun data historis harian dengan kolom:

OHLCV: Open, High, Low, Close, Volume.

Technical Indicators: ma_7, ma_30, rsi, macd, bb_upper, bb_lower, dll.

Target: daily_return (Persentase perubahan harian).

🛠️ Tech Stack
Languages: Python

Libraries: TensorFlow/Keras, Pandas, NumPy, Scikit-Learn, Matplotlib, Joblib.

Platform: Google Colab.

🧠 Model Architecture (LSTM)
Model dibangun menggunakan arsitektur Recurrent Neural Network khusus memori jangka panjang:

LSTM Layer 1: 50 units (Return Sequences).

Dropout: 0.2 (Mencegah Overfitting).

LSTM Layer 2: 50 units.

Dropout: 0.2.

Dense Layers: 25 units & 1 unit (Output).

Early Stopping: Berhenti otomatis jika Validation Loss tidak lagi membaik.

📊 Results & Visualization
Setelah memprediksi Daily Returns, model merekonstruksi harga menggunakan rumus:
Price_t = Price_{t-1} * (1 + Predicted_Return_t)

Prediksi vs Aktual
![alt text](https://github.com/USERNAME/REPO_NAME/raw/main/hasil_prediksi.png)

(Saran: Upload screenshot grafik hijau Anda ke folder repo lalu ganti link gambar di atas)

Performance Metrics:
Mean Absolute Error (MAE): $39.64

Root Mean Squared Error (RMSE): $66.36

🚀 How to Run
Clone repository ini:

code
Bash
git clone https://github.com/USERNAME/REPO_NAME.git
Buka file .ipynb di Google Colab.

Upload dataset gold_price_forecasting_dataset.csv.

Run semua cell.

💡 Professional Insights & Best Practices
Stationarity is King: Neural Networks kesulitan memprediksi harga yang terus naik tanpa batas. Dengan memprediksi Return, model belajar pola volatilitas yang jauh lebih konsisten.

1-Step-Ahead Forecasting: Model ini menggunakan data aktual hari kemarin untuk memprediksi hari ini, menjadikannya sangat relevan untuk strategi Day Trading.

Scalability: File feature_scaler.pkl disimpan secara terpisah agar model siap digunakan untuk data baru di masa depan (Production-Ready).

👨‍💻 Author
[Nama Anda]

LinkedIn: [link-linkedin-anda]

Kaggle: [link-kaggle-anda]
