# UTS Deep Learning: End-to-End Model Pipeline

Repository ini disusun sebagai tugas individu Ujian Tengah Semester (UTS) mata kuliah Deep Learning. Laporan ini mencakup hasil pengerjaan model Neural Network untuk tugas Regresi dan laporan kendala pada tugas Klasifikasi.

## 👤 Identitas Mahasiswa
* **Nama:** Juandra Alghifary
* **NIM:** 1103220165

## 📝 Status Pengerjaan
| Tugas / Dataset | Jenis Masalah | Status |
| :--- | :--- | :--- |
| **Song Year Prediction** | Regression | ✅ **BERHASIL** |
| **Fraud Detection** | Classification | ⚠️ **TIDAK DILANJUTKAN** |

---

## ✅ Project 1: Song Year Prediction (Regresi)
Fokus utama repository ini adalah penyelesaian tugas prediksi tahun rilis lagu menggunakan **Deep Neural Network**.

### 1. Deskripsi Data
* **Dataset:** `midterm-regresi-dataset.csv`
* **Input:** 90 fitur audio numerik (Timbre features).
* **Target:** Tahun rilis lagu (Year).

### 2. Arsitektur Model (TensorFlow/Keras)
Model dibangun menggunakan **Multi-Layer Perceptron (MLP)** dengan konfigurasi:
* **Input Layer:** 90 Neuron.
* **Hidden Layers:**
    * Dense Layer (128 neuron, ReLU)
    * Dense Layer (64 neuron, ReLU)
    * Dense Layer (32 neuron, ReLU)
* **Output Layer:** 1 Neuron (Linear Activation) untuk output prediksi tahun.
* **Optimizer:** Adam.
* **Loss Function:** Mean Squared Error (MSE).

### 3. Hasil Evaluasi
* **Training Process:** Loss menurun drastis dari ~58,000 di epoch awal menjadi ~148 di epoch akhir.
* **Test Result:** Model mampu memprediksi tahun lagu dengan rata-rata error yang rendah pada data uji. Grafik training menunjukkan model konvergen dengan baik (tidak underfitting).

---

## ⚠️ Laporan Kendala: Fraud Detection
Saya telah berupaya merancang pipeline untuk tugas **Fraud Detection** (Deteksi Penipuan), namun proses tersebut tidak disertakan dalam hasil akhir karena kendala teknis berikut:

1.  **Isu Dataset (Missing Train Data):**
    * File data latih utama (`train_transaction.csv`) yang memuat label `isFraud` tidak ditemukan atau korup pada saat runtime di lingkungan lokal.
    * Hanya tersedia file `test_transaction.csv` yang tidak memiliki label, sehingga proses *Supervised Learning* tidak dapat dilakukan.
2.  **Keterbatasan Hardware (Resource Exhaustion):**
    * Percobaan memuat dataset transaksi dalam jumlah besar menyebabkan *Crash/Memory Error* pada perangkat yang digunakan.

**Keputusan:**
Dikarenakan kendala di atas dan batas waktu, fokus pengerjaan dialihkan sepenuhnya untuk memaksimalkan akurasi pada model **Regresi (Song Year Prediction)** yang terbukti berjalan stabil dan sukses.

---

## 🚀 Cara Menjalankan (Song Regression Model)
1.  Pastikan library berikut terinstall:
    ```bash
    pip install pandas numpy tensorflow scikit-learn matplotlib
    ```
2.  Buka file notebook **`midterm_deep_learning.ipynb`** (atau file `.ipynb` yang tersedia).
3.  Pastikan file dataset `midterm-regresi-dataset.csv` berada dalam satu folder yang sama.
4.  Jalankan semua cell (Run All).
