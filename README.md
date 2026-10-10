# Dengue Fever Hematological Classification 🦟💉

Repositori ini berisi kode dan dokumentasi untuk proyek analisis data serta pengembangan model *machine learning* dalam mengklasifikasikan kondisi pasien terhadap risiko Demam Berdarah Dengue (DBD) menggunakan variabel hematologi darah lengkap (*Complete Blood Count*).

---

## 📌 Latar Belakang

Indonesia memiliki tingkat kejadian demam berdarah yang relatif tinggi setiap tahunnya. Penyakit yang disebabkan oleh virus *dengue* ini dapat memicu komplikasi parah hingga kematian jika tidak dideteksi dan ditangani sejak dini. 

Oleh karena itu, identifikasi awal melalui parameter hematologi (seperti kadar hemoglobin, jumlah trombosit, leukosit, hematokrit, dll.) menjadi kunci utama dalam manajemen pasien yang efektif. Proyek ini bertujuan untuk membantu tenaga medis mempercepat proses deteksi dini dan meningkatkan akurasi pencegahan risiko fatal.

---

## 📂 Struktur Dataset

Dataset yang digunakan (*Dengue_Fever_Hematological_Dataset.csv*) mencakup total 1.548 baris data dan 19 kolom variabel, yang terdiri dari:
- **Demografi:** `Gender`, `Age`
- **Parameter Hematologi:** `Hemoglobin(g/dl)`, `Neutrophils(%)`, `Lymphocytes(%)`, `Monocytes(%)`, `Eosinophils(%)`, `RBC`, `HCT(%)`, `MCV(fl)`, `MCH(pg)`, `MCHC(g/dl)`, `RDW-CV(%)`, `Total Platelet Count(/cumm)`, `MPV(fl)`, `PDW(%)`, `PCT(%)`, `Total WBC count(/cumm)`
- **Target Variabel:** `Result` (*positive* / *negative*)

---

## 📊 Tahapan Proyek (Workflow)

1. **Exploratory Data Analysis (EDA):**
   - Pemeriksaan bentuk, tipe data, dan statistik deskriptif awal.
   - Deteksi anomali data, nilai kosong (*missing values*), inkonsistensi kategori (*Gender*), dan duplikasi baris.
2. **Data Preprocessing & Cleaning:**
   - Pembersihan inkonsistensi data teks dan penanganan nilai yang hilang.
   - Penanganan *outlier* dan distribusi data.
3. **Resampling & Scaling:**
   - Menangani ketidakseimbangan kelas menggunakan teknik **SMOTE** (*Synthetic Minority Over-sampling Technique*).
   - Normalisasi fitur menggunakan *StandardScaler* / *RobustScaler*.
4. **Model Training & Evaluation:**
   - Melatih beberapa algoritma pemodelan: *Random Forest Classifier*, *Gradient Boosting Classifier*, *Decision Tree*, dan *Logistic Regression*.
   - Evaluasi performa model menggunakan metrik *Accuracy*, *Precision*, *Recall*, *F1-Score*, dan *ROC-AUC Score*.

---

## 🛠️ Kebutuhan Pustaka (Libraries)

Pastikan pustaka berikut terinstal di lingkungan Python Anda sebelum menjalankan kode:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
