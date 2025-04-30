# Klasifikasi Gambar Buah

Repositori ini merupakan bagian dari **proyek akhir Belajar Pengembangan Machine Learning** untuk membangun model klasifikasi gambar menggunakan **Convolutional Neural Network (CNN)**. Fokus utama proyek ini adalah mengenali dan mengklasifikasikan berbagai jenis buah berdasarkan gambar.

---

## Struktur Proyek

```
├── fruit-image-classification/
│   ├── notebook.ipynb
│   ├── model_saved/       -> Model dalam format SavedModel
│   ├── model.tflite       -> Model untuk perangkat mobile
│   ├── tfjs_model/        -> Model untuk TensorFlow.js (web)
│   └── requirements.txt   -> File dependensi
```

---

## Dataset

Dataset berasal dari Kaggle dan terdiri dari gambar berbagai jenis buah seperti apel, pisang, dan jeruk. Total dataset terdiri dari **lebih dari 1000 gambar** dan memiliki distribusi yang cukup merata.

---

## Cara Mengunduh Dataset di Google Colab

Ikuti langkah-langkah berikut:

1. Kunjungi [Kaggle.com](https://www.kaggle.com/) dan login.
2. Masuk ke halaman profil > Settings > API > **Create New API Token**.
3. Upload file `kaggle.json` ke Google Colab.
4. Jalankan perintah berikut di Colab:

```python
!pip install -q kaggle
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
!kaggle datasets download -d utkarshsaxenadn/fruits-c
```

---

## Tujuan Proyek

- Membangun model CNN untuk klasifikasi gambar buah.
- Mencapai akurasi minimal **85%** pada training dan testing.
- Menyimpan model dalam tiga format: SavedModel, TF Lite, dan TFJS.
- Membuat visualisasi kurva akurasi dan loss untuk analisis model.

---

## Hasil

Model berhasil dilatih hingga mencapai akurasi tinggi pada data uji. Visualisasi kurva akurasi dan loss menunjukkan proses pelatihan yang stabil.

---

## Fitur Tambahan

- Visualisasi training & validation curve
- Implementasi Callback (EarlyStopping & ModelCheckpoint)
