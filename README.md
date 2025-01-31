# UAS_PROJEK_ML_C

# Klasifikasi Jenis Bahan Bakar Menggunakan Decision Tree Classifier

Proyek ini menggunakan **Decision Tree Classifier** untuk memprediksi jenis bahan bakar (Petrol, Diesel, atau CNG) dari sebuah mobil berdasarkan fitur-fiturnya. Model ini dilatih menggunakan dataset yang berisi informasi mobil, dan kode ini mencakup langkah-langkah preprocessing data, pelatihan model, evaluasi, dan visualisasi.

## Prasyarat

Sebelum menjalankan proyek ini, Anda perlu menginstal beberapa pustaka Python berikut:

- `pandas`
- `numpy`
- `sklearn`
- `matplotlib`

# Dataset
Dataset yang digunakan dalam proyek ini adalah cardekho_data.csv. Dataset ini berisi informasi tentang mobil, termasuk:

- Selling_Price: Harga jual mobil.
- Present_Price: Harga mobil saat ini.
- Year: Tahun pembuatan mobil.
- Kms_Driven: Jumlah kilometer yang telah ditempuh oleh mobil.
- Fuel_Type: Jenis bahan bakar yang digunakan mobil (Petrol, Diesel, CNG).

# Langkah-langkah
### Preprocessing Data
Dataset dimuat ke dalam DataFrame pandas, dan kolom Fuel_Type dipetakan ke nilai numerik:

- Petrol: 0
- Diesel: 1
- CNG: 2
Transformasi ini memungkinkan model untuk memproses data kategorikal sebagai fitur numerik.

### Pemilihan Fitur
Fitur-fitur yang digunakan untuk memprediksi jenis bahan bakar adalah:

- Selling_Price
- Present_Price
- Year
- Kms_Driven
Fitur-fitur ini dipilih dari dataset dan disimpan dalam variabel X, sementara variabel target y berisi jenis bahan bakar (Fuel_Type).

### Pembagian Data
Data dibagi menjadi data pelatihan dan data uji menggunakan train_test_split dari sklearn.model_selection. 80% dari data digunakan untuk melatih model, dan 20% digunakan untuk pengujian.

### Pelatihan Model
Model DecisionTreeClassifier dari sklearn.tree digunakan untuk melatih model. Model ini dilatih menggunakan data pelatihan (X_train, y_train).

### Evaluasi Model
Kinerja model dievaluasi menggunakan:

- Akurasi: Akurasi model pada data uji (accuracy_score).
- Laporan Klasifikasi: Precision, recall, dan F1-score untuk setiap kelas (classification_report).
- Matriks Kebingunguan: Visualisasi matriks kebingunguan untuk menunjukkan kinerja prediksi model (ConfusionMatrixDisplay).
### Visualisasi Model
Pohon keputusan yang telah dilatih divisualisasikan menggunakan fungsi plot_tree untuk menggambarkan bagaimana proses pengambilan keputusan dilakukan.

# Hasil
Setelah menjalankan skrip, output berikut akan ditampilkan:

- Akurasi model dalam memprediksi jenis bahan bakar.
- Laporan klasifikasi yang merinci precision, recall, dan F1-score untuk setiap jenis bahan bakar.
- Matriks kebingunguan yang menunjukkan nilai asli dan prediksi.
- Visualisasi grafis pohon keputusan.
