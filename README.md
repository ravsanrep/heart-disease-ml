# Heart Disease Prediction Using Machine Learning

## Final Project Machine Learning

Implementasi dan analisis beberapa algoritma Machine Learning untuk prediksi penyakit jantung menggunakan Heart Disease UCI Dataset.

---

## Project Overview

Penyakit jantung merupakan salah satu penyebab kematian tertinggi di dunia. Deteksi dini dapat membantu proses diagnosis dan pengambilan keputusan medis.

Pada proyek ini dilakukan:

* Data preprocessing
* Exploratory Data Analysis (EDA)
* Training beberapa model Machine Learning
* Perbandingan performa model
* Analisis hasil menggunakan berbagai metrik evaluasi

---

## Dataset

Dataset yang digunakan adalah Heart Disease UCI Dataset.

### Dataset Information

* Jumlah Data : ±1025 Records
* Jumlah Fitur : 13
* Target : Heart Disease (0 = No Disease, 1 = Disease)

### Features

| Feature  | Description                 |
| -------- | --------------------------- |
| age      | Age                         |
| sex      | Gender                      |
| cp       | Chest Pain Type             |
| trestbps | Resting Blood Pressure      |
| chol     | Cholesterol                 |
| fbs      | Fasting Blood Sugar         |
| restecg  | Resting ECG                 |
| thalach  | Maximum Heart Rate Achieved |
| exang    | Exercise Induced Angina     |
| oldpeak  | ST Depression               |
| slope    | Slope of ST Segment         |
| ca       | Number of Major Vessels     |
| thal     | Thalassemia                 |
| target   | Heart Disease               |

---

## Machine Learning Models

Pada penelitian ini digunakan tiga algoritma klasifikasi:

1. Logistic Regression
2. Random Forest Classifier
3. Support Vector Machine (SVM)

---

## Project Workflow

```text
Dataset Collection
        │
        ▼
Data Cleaning
        │
        ▼
Missing Value Handling
        │
        ▼
Feature Scaling
        │
        ▼
Train-Test Split
        │
        ▼
Model Training
        │
        ▼
Model Evaluation
        │
        ▼
Performance Comparison
```

---

## Data Preprocessing

Tahapan preprocessing yang dilakukan:

### 1. Data Cleaning

* Menghapus data duplikat
* Memeriksa missing value

### 2. Feature Scaling

Menggunakan StandardScaler agar seluruh fitur berada pada skala yang sama.

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)
```

### 3. Train Test Split

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X_scaled,
    y,
    test_size=0.2,
    random_state=42,
    stratify=y
)
```

---

## Evaluation Metrics

Model dievaluasi menggunakan:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* ROC-AUC Score

---

## Exploratory Data Analysis

Visualisasi yang digunakan:

### Distribution of Target Class

Menampilkan distribusi pasien dengan dan tanpa penyakit jantung.

### Correlation Heatmap

Menunjukkan hubungan antar fitur pada dataset.

### Model Performance Comparison

Membandingkan performa:

* Logistic Regression
* Random Forest
* SVM

### Feature Importance

Mengidentifikasi fitur yang paling berpengaruh terhadap prediksi penyakit jantung menggunakan Random Forest.

---

## Results

Contoh hasil eksperimen:

| Model               | Accuracy | Precision | Recall | F1 Score |
| ------------------- | -------- | --------- | ------ | -------- |
| Logistic Regression | 0.86     | 0.85      | 0.84   | 0.85     |
| Random Forest       | 0.95     | 0.94      | 0.95   | 0.94     |
| SVM                 | 0.89     | 0.88      | 0.89   | 0.88     |

### Best Model

Random Forest menghasilkan performa terbaik pada dataset Heart Disease dengan nilai Accuracy dan Recall tertinggi.

---

## Feature Importance Analysis

Berdasarkan hasil Random Forest, fitur yang memiliki kontribusi terbesar terhadap prediksi penyakit jantung adalah:

* Chest Pain Type (cp)
* Maximum Heart Rate (thalach)
* ST Depression (oldpeak)
* Number of Major Vessels (ca)

---

## Technologies Used

* Python 3.x
* Pandas
* NumPy
* Scikit-Learn
* Matplotlib
* Seaborn

---

## Installation

Clone repository:

```bash
git clone https://github.com/username/heart-disease-ml.git
cd heart-disease-ml
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Run Project

```bash
python main.py
```

atau menggunakan Jupyter Notebook:

```bash
jupyter notebook
```

---

## Repository Structure

```text
heart-disease-ml/
│
├── dataset/
│   └── heart.csv
│
├── notebooks/
│   └── HeartDiseaseAnalysis.ipynb
│
├── images/
│   ├── heatmap.png
│   ├── confusion_matrix.png
│   ├── model_comparison.png
│   └── feature_importance.png
│
├── main.py
├── requirements.txt
└── README.md
```

---

## Conclusion

Penelitian ini menunjukkan bahwa algoritma Machine Learning dapat digunakan untuk memprediksi penyakit jantung dengan tingkat akurasi yang tinggi.

Dari beberapa model yang diuji, Random Forest memberikan performa terbaik karena mampu menangkap hubungan non-linear antar fitur kesehatan pasien secara lebih efektif dibandingkan Logistic Regression dan SVM.

---

## Author

Final Project Machine Learning

Universitas / Institusi
