# 📘 Judul Proyek
Klasifikasi Agama Suatu Negara Berdasarkan Karakteristik Bendera Menggunakan Machine Learning dan Deep Learning

## 👤 Informasi
- **Nama:** [Arenta Putri Maharani]  
- **Repo:** [https://github.com/arentapm/Proyek-Machine-Learning.git]  
- **Video:** [https://drive.google.com/drive/folders/1Zk7q7y50MBDyAvmMCL3RCEDM7rAKR9fL?usp=drive_link]  

---

# 1. 🎯 Ringkasan Proyek
- Menyelesaikan permasalahan sesuai domain  
- Melakukan data preparation  
- Membangun 3 model: **Baseline**, **Advanced**, **Deep Learning**  
- Melakukan evaluasi dan menentukan model terbaik  

---

# 2. 📄 Problem & Goals
**Problem Statements:**  
- [1.	Dataset Flags memiliki karakteristik multivariat yang terdiri dari fitur numerik, kategorikal, dan biner, sehingga diperlukan metode preprocessing agar data dapat digunakan dengan baik untuk proses klasifikasi.]  
- [2.	Hubungan antara krakteristik visual bendera dan agama dominan suatu negara tidak bersifat langsung, sehingga dibutuhkan model machine learning yang mampu mengenali pola dari kombinasi fitur fitur tersebut.]  
- [3.	Ukuran dataset yang kecil relatif berpotensi menyebabkan model mengalami overfitting, sehingga perlu dilakukan pemilihan algoritma dan evaluasi model yang sesuai.]  

**Goals:**  
- [1. Membangun model machine learning untuk mengklasifikasikan agama dominan suatu negara berdasarkan karakteristik bendera menggunakan dataset Flags.]  
- [2.	Mengevaluasi kinerja model klasifikasi menggunakan metrik evaluasi seperti akurasi, precision, recall, dan confusion matrix.] 
- [3.	Menentukan model klasifikasi yang memberikan performa terbaik dan stabil pada datset yang digunakan.] 
 
---
## 📁 Struktur Folder
```
project/
│
├── data/ 
│   └── flag.data
|
├── notebooks/              
│   └── Tugas_UAS_DS.ipynb
│
├── src/                    
│   
├── models/                 
│   ├── naive_bayes_model.pkl
│   ├── random_forest_model.pkl
│   └── mlp_model.h5
│
├── images/                 
│   └── featureImportance.png
|   └── matrikMLP.png
|   └── mtrikNaiveBayes.png
|   └── matrikRandomForest.png
|   └── matrikMLP.png
│   └── ModelSummary.png
|   └── perbandinganMetrikModel.png
|   └── TrainingValidationAccuracyperEpoch.png
|   └── TrainingValidationLossperEpoch.png
|   └── visualisasi_1_EDA.png
|   └── visualisasi_2_EDA.png
|   └── visualisasi_3_EDA.png
|
├── requirements.txt        
├── .gitignore
└── README.md
```
---

# 3. 📊 Dataset
- **Sumber:** [UCI Machine Learning Repository]  
- **Jumlah Data:** [194]  
- **Tipe:** [Classification]  

### Fitur Utama
| Nama Fitur | Deskripsi |
|:---|:---|
| **Nama** | Nama Negara |
| **Landmass** | Benua tempat negara berada (1 = Amerika Utara, 3 = Eropa, 4 = Afrika, 5 = Asia, 6 = Oseania) |
| **Zone** | Zone geografis berdasarkan Greenwich dan Equator (1 = NE, 2 = SE, 3 = SW, 4 = NW) |
| **Area** | Luas wilayah negara dalam ribuan mil persegi |
| **Population** | Jumlah penduduk dalam jutaan |
| **Language** | Bahasa utama negara (1 = English, 2 = Spanish, 8 = Arabic, dll) |
| **Religion** | Agama dominan negara (0 = Catholic, 1 = Other Christian, 2 = Muslim, dll) |
| **Bars** | Jumlah garis vertikal pada bendera |
| **Stripes** | Jumlah garis horizontal pada bendera |
| **Colours** | Jumlah warna berbeda pada bendera |
| **Red** | Keberadaan warna merah pada bendera |
| **Green** | Keberadaan warna hijau pada bendera |
| **Blue** | Keberadaan warna biru pada bendera |
| **Gold** | Keberadaan warna emas/kuning pada bendera |
| **White** | Keberadaan warna putih pada bendera |
| **Black** | Keberadaan warna hitam pada bendera |
| **Orange** | Keberadaan warna oranye/coklat pada bendera |
| **Mainhue** | Warna dominan utama pada bendera |
| **Circles** | Jumlah simbol lingkaran pada bendera |
| **Crosses** | Jumlah simbol salib tegak pada bendera |
| **Saltires** | Jumlah simbol salib diagonal pada bendera |
| **Quarters** | Jumlah bagian seperempat pada bendera |
| **Sunstars** | Jumlah simbol matahari atau bintang pada bendera |
| **Crescent** | Keberadaan simbol bulan sabit pada bendera |
| **Triangle** | Keberadaan bentuk segitiga pada bendera |
| **Icon** | Keberadaan ikon benda mati (misal: kapal) pada bendera |
| **Animate** | Keberadaan ikon makhluk hidup pada bendera |
| **Text** | Keberadaan teks atau tulisan pada bendera |
| **Topleft** | Warna di sudut kiri atas bendera |
| **Botright** | Warna di sudut kanan bawah bendera |
---

# 4. 🔧 Data Preparation
- Cleaning (missing/duplicate/outliers)  
- Transformasi (encoding/scaling)  
- Splitting (train/val/test)  

---

# 5. 🤖 Modeling
- **Model 1 – Baseline:** [Naive Bayes]  
- **Model 2 – Advanced ML:** [Random Forest]  
- **Model 3 – Deep Learning:** [Multi Layer Perceptron (MLP)]  

---

# 6. 🧪 Evaluation
**Metrik:** Accuracy / F1 / MAE / MSE (pilih sesuai tugas)

### Hasil Singkat
| Model | Accuracy | F1-Score | Catatan |
|:---|:---:|:---:|:---|
| **Baseline (Naive Bayes)** | 0.3077 | 0.1960 | **Underfitting.** Model terlalu sederhana; asumsi independensi fitur tidak cocok untuk dataset Flags yang fiturnya saling berkorelasi. |
| **Advanced (Random Forest)** | **0.6410** | **0.3847** | **Model Terbaik.** Paling stabil dan mampu menangkap hubungan non-linear antar fitur dengan efisiensi training yang baik. |
| **Deep Learning (MLP)** | 0.5385 | 0.2904 | **Overfitting.** Mengalami kenaikan validation loss setelah epoch 6 dan gap akurasi yang besar antara data training dan testing. |

---

# 7. 🏁 Kesimpulan
- Model terbaik: [Random Forest (Advanced/ML)]  
- Alasan: [•	Random Forest memberikan keseimbangan terbaik antara performa, stabilitas, dan efisiensi traing dibandingkan model lain.
•	Performanya unggul dibanding Naive Bayes (baseline) dan MLP (deep learning) untuk dataset Flags, Akurasi test set 64,10% (lebih tinggi daripada Naive Bayes 30,77% dan MLP 53,85%) dan F1-Score: 0.3847, lebih baik dari baseline dan MLP
•	Mampu menangkap hubungan non-linier antar fitur numerik dan kategorikal yang sulit ditangani Naive bayes.
•	Tidak mengalami overfitting berlebihan seperti MLP, sehingga performa test set relatif stabil
]  
- Insight penting: [1.	Model Random Forest lebih efektif menangkap pola non-linear. Performanya lebih baik dibanding Naive Bayes dan MLP karena mampu memanfaatkan interaksi antar fitur numerik dan kategorikal.
2.	Deep Learning (MLP) mengalami overfitting meskipun dataset relatif kecil. Train accuracy tinggi (>70%) tetapi validation accuracy stabil di 50–60%. Ini menunjukkan MLP terlalu kompleks untuk dataset tabular kecil seperti Flags.
]  

---

# 8. 🔮 Future Work
- [Data: Dataset Flags yang digunakan relatif kecil (194 sampel), sehingga model—terutama deep learning—belum dapat belajar pola secara optimal. Pengumpulan data tambahan, baik dari sumber lain maupun perluasan atribut bendera, dapat meningkatkan generalisasi model dan mengurangi risiko overfitting.]    
- [Tuning model :Pengembangan model dapat dilakukan dengan feature engineering lanjutan untuk memperkaya informasi fitur, hyperparameter tuning yang lebih menyeluruh agar performa optimal, serta mencoba arsitektur deep learning yang lebih kompleks. Selain itu, penggunaan ensemble methods dengan menggabungkan beberapa model berpotensi meningkatkan akurasi dan stabilitas prediksi. ]   
 

---

# 9. 🔁 Reproducibility
Gunakan environment:
Python version : 3.13
Main Library :
numpy        	: 2.0.2
matplotlib 	    : 3.10.0
seaborn    	    : 0.13.2
scikit-learn	: 1.6.1
tensorflow 	    : 2.19.0
keras      	    : 3.10.0

