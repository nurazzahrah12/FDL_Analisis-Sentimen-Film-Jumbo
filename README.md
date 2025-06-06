# Proyek Analisis Sentimen: Film Jumbo

## Deskripsi Proyek

Proyek ini bertujuan untuk menganalisis sentimen dari komentar pengguna terhadap film *Jumbo*. Data diperoleh melalui proses scraping dan diproses melalui pipeline machine learning, dengan tujuan klasifikasi sentimen menjadi tiga kelas: positif, netral, dan negatif.

---

## Struktur Folder

```
├── Scrapping_Submission_Analisis_Sentimen_Nur_Salamah_Azzahrah.ipynb   # Notebook scraping data
├── Training_Submission_Analisis_Sentimen_Nur_Salamah_Azzahrah.ipynb   # Notebook pelatihan dan evaluasi model
├── scrapping_jumbo.csv                                                 # Data hasil scraping
├── data_label_clean.csv                                               # Data setelah labeling dan cleaning
├── requirements.txt                                                   # File dependensi Python
├── Kriteria Submission.txt                                            # Dokumen kriteria penilaian proyek
```

---

## Ringkasan Tahapan Proyek

### 1. Data Scraping
- Scraping dilakukan secara mandiri dari platform ulasan film.
- Total data melebihi 10.000 sampel.
- Disimpan dalam `scrapping_jumbo.csv`.

### 2. Preprocessing & Labeling
- Teks dibersihkan (lowercase, stopwords, stemming).
- Dilabeli secara kategorikal menjadi `positif`, `netral`, dan `negatif`.
- Distribusi label divisualisasikan.

### 3. Pelatihan Model
- Algoritma: Naive Bayes, SVM, Random Forest, dan Deep Learning.
- Ekstraksi fitur: TF-IDF dan Word2Vec.
- Data split: 80/20 pada semua model.
- Evaluasi: Akurasi, Precision, Recall, F1-Score.
- Akurasi model mencapai ≥92% untuk beberapa model.

### 4. Inference
- Inferensi dilakukan dalam notebook namun output perlu disesuaikan agar sesuai dengan input teks.
- Kelas prediksi: `positif`, `negatif`, dan `netral`.

---

## Umpan Balik Reviewer (Intisari)

**Kriteria utama yang sudah terpenuhi:**
- Data hasil scraping mandiri
- Labeling & preprocessing lengkap
- Model machine learning & deep learning
- Akurasi testing ≥85% (bahkan mencapai 92%)
- Dataset ≥10.000 dan terdiri dari 3 kelas

**Catatan untuk pengembangan:**
- Skema pelatihan yang dilakukan dianggap hanya dua variasi (karena proporsi data dan fitur yang sama)
- Output inferensi belum konsisten sesuai input
- Belum dilakukan error analysis dan penanganan data imbalance

---

## Saran Pengembangan
- Tambahkan variasi **skema pelatihan** (ubah algoritma, fitur, dan split)
- Buat **inference pipeline** yang menerima teks dan mengembalikan label
- Lakukan **analisis error dan penanganan imbalance**, misalnya:
  - Oversampling/undersampling
  - Gunakan `class_weight` pada model DL
- Evaluasi model dengan **metrik komprehensif**: precision, recall, F1, dan confusion matrix
- Tambahkan komentar dan dokumentasi di setiap tahap notebook
- Buat README mendalam (seperti ini!) untuk memperjelas alur proyek

---

## Cara Menjalankan

1. Install dependensi:
```bash
pip install -r requirements.txt
```

2. Jalankan notebook secara berurutan:
   - `Scrapping_Submission_*.ipynb`
   - `Training_Submission_*.ipynb`

---

## Output
- `scrapping_jumbo.csv` → hasil scraping mentah
- `data_label_clean.csv` → data siap pakai
- Model dan evaluasi disimpan dalam notebook

---

## Catatan
- Proyek ini telah menyentuh hampir semua aspek penting dalam analisis sentimen berbasis teks
- Dengan sedikit penyempurnaan di inference dan skema pelatihan, proyek ini bisa ditingkatkan ke level produksi
