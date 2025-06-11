# 💡 Machine Learning – Harumnesia Perfume Recommendation System

## 📌 Project Overview

Proyek ini mengembangkan **dua model rekomendasi parfum berbasis machine learning** dengan memanfaatkan data parfum lokal serta gabungan lokal dan internasional.  
- **Model pertama** menyajikan rekomendasi berdasarkan input pengguna seperti *gender, situasi, konsentrasi, ukuran, harga,* dan *deskripsi parfum*. Deskripsi diproses menggunakan **Gemini API** dan **LangChain** untuk mengekstrak *notes*, yang kemudian diolah melalui **scaling**, **one-hot encoding**, dan **TF-IDF**. Fitur yang dihasilkan direduksi menggunakan **autoencoder** dan dikelompokkan dengan **K-Means**, memungkinkan pencocokan preferensi pengguna ke dalam klaster dan pemberian rekomendasi berdasarkan **cosine similarity**.  
- **Model kedua** menggunakan pendekatan content-based filtering secara langsung, dengan merepresentasikan *notes* parfum melalui **TF-IDF Vectorization**, yang kemudian dikonversi ke **TensorFlow** untuk proses rekomendasi.

Kedua model ini diintegrasikan ke dalam sistem melalui file `.h5` dan `.pkl`, membentuk fondasi rekomendasi yang cepat, relevan, dan adaptif terhadap preferensi pengguna.

---

## 📂 Dataset

Terdapat dua dataset utama yang digunakan:

1. **Dataset Parfum Lokal**  
   Dikumpulkan secara manual dari e-commerce parfum lokal.  
   🔗 [Akses Dataset Lokal](https://github.com/Harumnesia/Machine-Learning/blob/main/Dataset/Dataset_Clean/Dataset_Harumnesia_clean.csv)

2. **Dataset Gabungan (Lokal + Luar Negeri)**  
   Merupakan gabungan dataset lokal dan dataset dari Kaggle.  
   🔗 [Akses Dataset Gabungan](https://github.com/Harumnesia/Machine-Learning/blob/main/Dataset/Dataset_Gabungan/dataset_parfum_gabungan.csv)

---

## ⚙️ Machine Learning Workflow

### 1. 🧩 Data Collection

- **Parfum lokal**: dikumpulkan dari berbagai sumber online shop.  
- **Parfum luar**: diambil dari dataset Kaggle.

### 2. 🧼 Data Cleaning

- Menstandarkan format huruf dan harga.  
- Menghapus kolom tidak relevan (mis. kolom "No").  
- Menyatukan berbagai jenis *notes* menjadi satu kolom deskriptif.

### 3. 🧪 Data Preprocessing

#### a. Model Pertama

- Deskripsi parfum diproses dengan **Gemini API + LangChain** → menghasilkan notes.  
- Notes diolah menjadi numerik melalui:
  - **Scaling**
  - **One-hot encoding**
  - **TF-IDF**
- Hasilnya direduksi dengan **autoencoder** sebelum dilakukan clustering.

#### b. Model Kedua

- Notes parfum langsung diolah dengan **TF-IDF Vectorization**.

### 4. 🧠 Model Development

#### a. Model Pertama

- **Autoencoder** (Neural Network) untuk ekstraksi fitur.  
- **K-Means Clustering** untuk pengelompokan parfum.  
- Rekomendasi dengan **cosine similarity** berdasarkan input user.

#### b. Model Kedua

- TF-IDF → TensorFlow conversion.  
- Rekomendasi berdasarkan kemiripan teks notes.

### 5. 🏋️‍♀️ Training

- Model dilatih menggunakan **TensorFlow** dan **Keras**.

### 6. ✅ Evaluasi

- **Autoencoder**: dievaluasi dengan **Mean Squared Error (MSE)**.  
- **K-Means**: dievaluasi menggunakan **Silhouette Score**.

---

## 🧾 Cara Menjalankan Kode / How to Run the Code

### 🗂 Struktur Proyek

## 🛠️ How to Run the Code

Ikuti langkah-langkah berikut untuk menjalankan proyek ini secara lokal:

### **Clone Repository**
```bash
git clone https://github.com/Harumnesia/Machine-Learning.git
cd Machine-Learning

### **Virtual Environment**

python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

### **Install Dependencies**
pip install -r requirements.txt

### **Jalankan Notebook (via Google Colab)**

Klik salah satu notebook di folder `Notebook/` untuk membukanya langsung di Google Colab:

- [Model 1 - Parfum Lokal (Harumnesia)](https://colab.research.google.com/github/Harumnesia/Machine-Learning/blob/main/Notebook/Model_1_Harumnesia.ipynb)
- [Model 2 - Parfum Gabungan (Lokal + Luar)](https://colab.research.google.com/github/Harumnesia/Machine-Learning/blob/main/Notebook/Model_2_Gabungan.ipynb)
