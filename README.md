# UTS Deep Learning: Song Year Prediction (Regression)

Repository ini disusun sebagai tugas Ujian Tengah Semester (UTS) mata kuliah Deep Learning. Fokus tugas ini adalah membangun model **End-to-End Deep Learning** untuk tugas Regresi, yaitu memprediksi tahun rilis lagu berdasarkan fitur audio.

## 👤 Identitas Mahasiswa
* **Nama:** Juandra Alghifary
* **NIM:** 1103220165

## 📊 Deskripsi Dataset
Dataset yang digunakan adalah `midterm-regresi-dataset.csv` (Audio Features).
* **Target:** Kolom pertama (Tahun Rilis Lagu).
* **Fitur:** 90 kolom fitur numerik (Timbre audio measures).
* **Tipe Masalah:** Regresi (Memprediksi nilai kontinu).

## 🧠 Arsitektur Model (Neural Network)
Model dibangun menggunakan framework **TensorFlow / Keras** dengan arsitektur **Multi-Layer Perceptron (MLP)**:

* **Input Layer:** Menerima 90 fitur audio.
* **Hidden Layer 1:** 128 Neuron (Activation: ReLU).
* **Hidden Layer 2:** 64 Neuron (Activation: ReLU).
* **Hidden Layer 3:** 32 Neuron (Activation: ReLU).
* **Output Layer:** 1 Neuron (Linear) -> Karena outputnya adalah tahun (angka).

## 🛠️ Metodologi
1.  **Preprocessing:**
    * Load data tanpa header (`header=None`).
    * Memisahkan fitur (X) dan target (y).
    * **Standard Scaling:** Normalisasi data agar proses training Neural Network lebih cepat dan stabil.
    * Split Data: Train (80%) dan Test (20%).
2.  **Training:**
    * **Optimizer:** Adam.
    * **Loss Function:** Mean Squared Error (MSE).
    * **Epochs:** 20.
3.  **Evaluasi:**
    * Mengukur performa model menggunakan MSE Loss pada data test.

## 🚀 Cara Menjalankan Code
1.  Pastikan library Deep Learning terinstall:
    ```bash
    pip install pandas numpy tensorflow scikit-learn matplotlib
    ```
2.  Buka file `tugas_dl_regression.ipynb`.
3.  Pastikan dataset `midterm-regresi-dataset.csv` tersedia.
4.  Run All Cells.

## 📈 Hasil
Model Deep Learning berhasil dilatih dan menunjukkan penurunan Loss (Error) yang signifikan dari epoch awal hingga akhir, menunjukkan model mampu mempelajari pola dari fitur audio untuk menebak tahun lagu.
