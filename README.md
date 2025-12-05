# UTS Deep Learning: Song Year Prediction (End-to-End Pipeline)

Repository ini disusun sebagai tugas individu Ujian Tengah Semester (UTS) mata kuliah Deep Learning. Proyek ini bertujuan membangun pipeline **Deep Neural Network** untuk memprediksi tahun rilis lagu berdasarkan fitur audio (Regression Task).

## 👤 Identitas
* **Nama:** Juandra Alghifary
* **NIM:** 1103220165

## 📂 Gambaran Proyek
Dataset yang digunakan adalah `midterm-regresi-dataset.csv`.
* **Input:** 90 fitur numerik (audio features dari sinyal musik).
* **Output:** Tahun rilis lagu (Tahun 2000, 2001, dst).
* **Tujuan:** Membuat model yang bisa menebak tahun rilis dengan error sekecil mungkin.

## 🧠 Arsitektur Model (Deep Learning)
Saya menggunakan framework **TensorFlow/Keras** dengan arsitektur Multi-Layer Perceptron (MLP):
1.  **Input Layer:** 90 Neuron (sesuai jumlah fitur).
2.  **Hidden Layer 1:** 128 Neuron (Activation: ReLU).
3.  **Hidden Layer 2:** 64 Neuron (Activation: ReLU).
4.  **Hidden Layer 3:** 32 Neuron (Activation: ReLU).
5.  **Output Layer:** 1 Neuron (Linear) -> Untuk output angka kontinu (tahun).

## 🛠️ Alur Pengerjaan (Pipeline)
1.  **Data Loading:** Mengimpor dataset tanpa header.
2.  **Preprocessing:**
    * Memisahkan fitur (X) dan target (y).
    * **Feature Scaling:** Menggunakan `StandardScaler` untuk menstandarisasi rentang data agar training lebih stabil.
    * **Train-Test Split:** Membagi data menjadi 80% Training dan 20% Testing.
3.  **Modeling & Training:**
    * Optimizer: `Adam`
    * Loss Function: `Mean Squared Error (MSE)`
    * Epochs: 20
4.  **Evaluasi:** Mengukur performa akhir menggunakan data test.

## 📊 Hasil
* **Training Loss:** Menurun signifikan dari 58,000+ ke ~140.
* **Test Loss (MSE):** ~124.45 (Rata-rata kesalahan prediksi tahun cukup rendah).
* Grafik training menunjukkan konvergensi yang baik (tidak underfitting/overfitting parah).

## 🚀 Cara Menjalankan
1.  Buka file `midterm_transaction_data.ipynb` di Google Colab atau VS Code.
2.  Pastikan file `midterm-regresi-dataset.csv` satu folder dengan notebook.
3.  Run All Cells.
