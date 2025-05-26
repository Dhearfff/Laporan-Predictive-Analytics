# Laporan-Predictive-Analytics - Dhea Rachma Febiana

## Domain Proyek
##### Latar Belakang
Kanker payudara merupakan salah satu jenis kanker yang paling banyak ditemukan dan menjadi penyebab utama kematian akibat kanker di kalangan wanita di seluruh dunia. Menurut data terbaru dari World Health Organization (WHO), kanker payudara menyebabkan sekitar 670.000 kematian di seluruh dunia pada tahun 2022. Kanker ini terjadi di semua negara, dan menjadi jenis kanker paling umum pada perempuan di 157 dari 185 negara. Menariknya, sekitar setengah dari kasus kanker payudara terjadi pada perempuan yang tidak memiliki faktor risiko khusus selain jenis kelamin dan usia. Meskipun lebih sering menyerang perempuan, sekitar 0,5% hingga 1% kasus juga terjadi pada laki-laki (WHO, 2022). Di Indonesia sendiri, menurut data Kementerian Kesehatan, kanker payudara menempati urutan pertama sebagai jenis kanker yang paling banyak diderita oleh wanita, dengan insiden yang terus meningkat setiap tahunnya. 
World Health Organization (WHO) menyatakan bahwa diagnosis dan deteksi dini sangat penting untuk keberhasilan pengobatan dan tingkat kelangsungan hidup pasien. Diagnosis manual yang bergantung pada interpretasi visual gambar dan biopsi, bagaimanapun, seringkali memakan waktu lama dan rentan terhadap kesalahan manusia.

Deteksi dini dan diagnosis yang tepat sangat krusial dalam upaya pengendalian penyakit ini karena tingkat kelangsungan hidup pasien sangat bergantung pada stadium kanker saat didiagnosis. Metode konvensional diagnosis, seperti biopsi dan pemeriksaan citra medis, meskipun efektif, masih memerlukan waktu yang relatif lama dan bergantung pada pengalaman serta ketelitian tenaga medis. Kesalahan dalam diagnosis atau keterlambatan pengambilan keputusan dapat berdampak fatal bagi pasien.
Seiring dengan kemajuan teknologi dan ilmu komputer, penerapan machine learning sebagai alat bantu diagnosis medis mulai mendapatkan perhatian yang signifikan. Machine learning dapat mengolah data numerik dan pola kompleks yang sulit diidentifikasi oleh manusia secara manual, sehingga memungkinkan prediksi dan klasifikasi penyakit dengan tingkat akurasi yang tinggi dan waktu yang lebih singkat.

##### Mengapa dan Bagaimana Masalah Ini Harus Diselesaikan
Permasalahan dalam diagnosis kanker payudara perlu segera diatasi mengingat dampak signifikan yang ditimbulkan terhadap kesehatan masyarakat, terutama pada wanita. Tingginya prevalensi serta angka kematian akibat kanker payudara menunjukkan urgensi pengembangan metode deteksi yang lebih cepat, tepat, dan mudah dijangkau. Keterlambatan atau ketidakakuratan dalam diagnosis dapat menyebabkan penanganan medis yang tidak efektif dan mengurangi peluang kesembuhan pasien(Zhou et al.,2020).

Pemanfaatan machine learning sebagai solusi memberikan kemampuan untuk mengolah data medis secara otomatis dan terstruktur, sehingga dapat mengurangi ketergantungan pada interpretasi manual yang seringkali rentan terhadap bias dan kesalahan. Algoritma klasifikasi seperti Random Forest dan XGBoost telah terbukti mampu mengelola data medis dengan baik dan memberikan prediksi yang akurat, menjadikannya pilihan yang tepat untuk diterapkan dalam kasus ini (Wang et al., 2021).

Dalam proyek ini, solusi yang diusulkan adalah pembangunan model klasifikasi untuk tumor payudara menggunakan dataset Breast Cancer Wisconsin dengan penerapan teknik reduksi dimensi yaitu dengan menggunakan PCA (Principal Component Analysis) untuk mengurangi jumlah fitur dari 30 menjadi sekitar 10 fitur utama yang mewakili informasi penting serta algoritma ensemble (Random Forest & XGBoost). Model tersebut akan dievaluasi menggunakan metrik akurasi, precision, recall, dan F1-score untuk memastikan tidak hanya ketepatan prediksi, tetapi juga kemampuan generalisasi yang memadai sehingga dapat diaplikasikan secara efektif dalam praktik klinis.

##### Referensi
Kementerian Kesehatan Republik Indonesia. (2025). *Profil Kesehatan Indonesia 2021*. Jakarta: Kementerian Kesehatan RI. https://sehatnegeriku.kemkes.go.id/baca/umum/20220202/1639254/kanker-payudaya-paling-banyak-di-indonesia-kemenkes-targetkan-pemerataan-layanan-kesehatan/

Wang, S., Chen, J., & Li, Z. (2021). Machine learning in breast cancer diagnosis and prognosis: A review. *Journal of Healthcare Engineering*, 2021, Article ID 9954584. https://doi.org/10.1155/2021/9954584

World Health Organization. (2021). *Breast cancer*. https://www.who.int/news-room/fact-sheets/detail/breast-cancer

Zhou, X., Huang, X., & He, L. (2020). Application of machine learning techniques for breast cancer diagnosis: A systematic review. *Computers in Biology and Medicine*, 123, 103915. https://doi.org/10.1016/j.compbiomed.2020.103915

Dua, D., & Graff, C. (2019). *Breast Cancer Wisconsin (Diagnostic) Data Set*. UCI Machine Learning Repository. Retrieved from https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data


## Business Understanding

### Problem Statements

- Ketapatan hasil prediksi yang masih menggunakan metode konvesional itu membutuhkan waktu lama dan hanya bergantung pada keahlian tenaga medis, sehingga ketepatan predikasinya masih menjadi masalah utama
- Keterbatasan akses ke fasilitas kesehatan dan tenaga ahli yang dapat menyebabkan keterlambatan diagnosis yang tepat, sehingga penanganannya juga menjadi semakin lama
- Kurangnya sistem yang dapat dengan mudah digunakan untuk mendiagnosis tumor kanker secara cepat, akurat, dan mudah

### Goals

- Mengembangkan model klasifikasi berbasis machine learning yang dapat membedakan secara akurat antara tumor ganas dan jinak menggunakan dataset numerik karakteristik tumor payudara.
- Mewujudkan solusi teknologi yang mempercepat dan mempermudah proses klasifikasi tumor sehingga dapat membantu tenaga medis dalam pengambilan keputusan klinis yang lebih cepat dan tepat.
- Menghasilkan sistem dengan model klasifikasi yang memiliki performa tinggi dan kemampuan generalisasi yang baik, sehingga dapat diterapkan secara luas

### Solution statements
Untuk menghasilkan model klaisfikasi yang akurat, diterapkan beberapa solusi yaitu:
- Penggunaan dua algoritma klasifikasi yang berbeda, yaitu Random Forest dan XGBoost.
Random Forest dipilih karena kemampuannya menangani dataset dengan fitur numerik kompleks serta robust terhadap overfitting.
XGBoost dipilih sebagai model boosting yang terkenal efektif dalam meningkatkan akurasi dan performa prediksi pada dataset medis.
- Penerapan teknik reduksi dimensi menggunakan Principal Component Analysis (PCA) untuk mengurangi jumlah fitur tanpa mengorbankan informasi penting. Teknik ini membantu meningkatkan efisiensi pemodelan dan mengurangi risiko overfitting.
- Dilakukan evaluasi model menggunakan metrik evaluasi yang lengkap, yaitu akurasi, precision, recall, dan F1-score, untuk memastikan bahwa model yang dikembangkan tidak hanya akurat tetapi juga dapat membedakan kelas tumor dengan baik.



## Data Understanding
Dataset yang digunakan dalam proyek ini adalah Breast Cancer Wisconsin (Diagnostic) Dataset yang diperoleh dari platform Kaggle [https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data]. Dataset ini berisi data numerik mengenai karakteristik tumor payudara dengan tujuan klasifikasi jenis tumor menjadi ganas atau jinak.

### Variabel-variabel pada reast Cancer Wisconsin (Diagnostic) Dataset adalah sebagai berikut:

- diagnosis: Target variabel yang menunjukkan jenis tumor (0 = jinak, 1 = ganas).
- radius_mean: Rata-rata jarak dari pusat ke tepi tumor.
- texture_mean: Rata-rata variasi intensitas abu-abu pada gambar tumor.
- perimeter_mean: Rata-rata panjang keliling tumor.
- area_mean: Rata-rata luas area tumor.
- smoothness_mean: Rata-rata variasi lokal dalam radius tumor.
- compactness_mean: Rata-rata perbandingan perimeter kuadrat terhadap luas area tumor.
- concavity_mean: Rata-rata tingkat cekungan (kelengkungan) tepi tumor.
- concave points_mean: Rata-rata jumlah titik cekung pada tepi tumor.
- symmetry_mean: Rata-rata simetri tumor.
- fractal_dimension_mean: Rata-rata kompleksitas tepi tumor (dimensi fraktal).
- radius_se: Standar error (kesalahan baku) dari radius tumor.
- texture_se: Standar error dari tekstur tumor.
- perimeter_se: Standar error dari perimeter tumor.
- area_se: Standar error dari area tumor.
- smoothness_se: Standar error dari smoothness tumor.
- compactness_se: Standar error dari compactness tumor.
- concavity_se: Standar error dari concavity tumor.
- concave points_se: Standar error dari concave points tumor.
- symmetry_se: Standar error dari symmetry tumor.
- fractal_dimension_se: Standar error dari fractal dimension tumor.
- radius_worst: Nilai maksimum radius tumor pada sampel.
- texture_worst: Nilai maksimum tekstur tumor.
- perimeter_worst: Nilai maksimum perimeter tumor.
- area_worst: Nilai maksimum area tumor.
- smoothness_worst: Nilai maksimum smoothness tumor.
- compactness_worst: Nilai maksimum compactness tumor.
- concavity_worst: Nilai maksimum concavity tumor.
- concave points_worst: Nilai maksimum jumlah titik cekung tumor.
- symmetry_worst: Nilai maksimum simetri tumor.
- fractal_dimension_worst: Nilai maksimum fractal dimension tumor.
- diagnosis_label: Label asli diagnosis berupa string ('B' untuk jinak, 'M' untuk ganas).

### Exploratory Data Analysis (EDA)
1. Distribusi Kelas Diagnosis
Distribusi kelas target (diagnosis) diamati untuk memastikan bahwa dataset tidak terlalu tidak seimbang (imbalanced). Berikut visualisasi distribusi kelas menggunakan grafik batang (countplot):
```
plt.figure(figsize=(6,4))
sns.countplot(x='diagnosis_label', data=df)
plt.title('Distribusi Kelas Diagnosis')
plt.xlabel('Diagnosis')
plt.ylabel('Jumlah')
plt.show()
```
![Distribusi Kelas Diagnosis](https://i.postimg.cc/wTMGZ6qR/Visual1.png)

Hasil dari visualisiasi itu akan menunjukkan bahwa data terdiri dari dua kelas yaitu Jinak(B) dan Ganas(M), dimana jumlah data pada B adalah 357 dan pada M adalah 212.

2. Distribusi Fitur Numerik
Untuk beberapa fitur utama seperti radius_mean, texture_mean, perimeter_mean, area_mean, dan smoothness_mean, histogram dengan kurva kepadatan kernel (KDE) dibuat untuk melihat sebaran nilai fitur:
```
features_to_plot = ['radius_mean', 'texture_mean', 'perimeter_mean', 'area_mean', 'smoothness_mean']

for feature in features_to_plot:
    plt.figure(figsize=(6,4))
    sns.histplot(df[feature], bins=30, kde=True)
    plt.title(f'Distribusi {feature}')
    plt.xlabel(feature)
    plt.ylabel('Frekuensi')
    plt.show()
```
![Distribusi Radius Mean](https://i.postimg.cc/T3cL1Nfp/visual2.png)
![DTM](https://i.postimg.cc/wBhW1p3D/DTM.png)
![DPM](https://i.postimg.cc/wMBF4R2k/DPM.png)
![DAM](https://i.postimg.cc/tCY2hPYq/DAM.pngg)
![DSM](https://i.postimg.cc/KYyfSHQj/DSM.png)

Visualisiasi ini adalah untuk mengidentifikasi apakah fitur memiliki distribusi normal, skewed, atau memiliki nilai ekstrim.

3. Korelasi Antar Fitur
Analisis korelasi dilakukan untuk memahami hubungan linear antara fitur numerik dalam dataset. 
Visualisasi korelasi dilakukan menggunakan heatmap sebagai berikut:
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
plt.figure(figsize=(12,10))
sns.heatmap(numeric_df.corr(), cmap='coolwarm', annot=False)
plt.title('Heatmap Korelasi Fitur')
plt.show()
```
![HEATMAP KORELASI](https://i.postimg.cc/0QV0S2vK/HEATMAP-KORELASI.png)

Hasil visualisasi menunjukkan adanya fitur-fitur yang memiliki korelasi tinggi satu sama lain, seperti antara radius_mean, perimeter_mean, dan area_mean, yang mengindikasikan adanya hubungan linier kuat. I

4. Perbandingan Fitur Berdasarkan Diagnosis
Metode boxplot digunakan untuk membandingkan median, kuartil, serta sebaran nilai antar kelas.
```
for feature in features_to_plot:
    plt.figure(figsize=(6,4))
    sns.boxplot(x='diagnosis', y=feature, data=df)
    plt.title(f'{feature} berdasarkan Diagnosis (0=Benign, 1=Malignant)')
    plt.xlabel('Diagnosis')
    plt.ylabel(feature)
    plt.show()
```
Hasil dari visualisasi tersebut terlihat perbedaan distribusi yang signifikan pada beberapa fitur, seperti radius_mean dan area_mean, antara pasien dengan tumor jinak dan ganas. Ini menunjukkan bahwa fitur-fitur tersebut memiliki potensi tinggi sebagai indikator diagnosis.





## Data Preparation

1. Penghapusan Kolom Kosong
```
if 'Unnamed: 32' in df.columns:
    df.drop(['Unnamed: 32'], axis=1, inplace=True)
```
Kolom Unnamed: 32 hanya berisi nilai kosong (NaN) dan tidak memiliki informasi penting. Oleh karena itu, kolom ini dihapus agar tidak memengaruhi proses pelatihan model.

2. Pemisahan Fitur dan Target
```
X = df.drop(['diagnosis', 'diagnosis_label'], axis=1)
y = df['diagnosis']
```
Data dipisahkan menjadi variabel fitur X dan variabel target y. Variabel diagnosis digunakan sebagai target karena merupakan label klasifikasi (ganas/jinak), sedangkan diagnosis_label tidak diperlukan karena merupakan bentuk string dari diagnosis.



3. Pemeriksaan Missing Values
```
print("\nMissing values di fitur:", X.isnull().sum().sum())
print("Missing values di target:", y.isnull().sum())
```
 Bertujuan untuk memastikan tidak ada nilai kosong yang tersisa di dalam fitur maupun target. Hasilnya menunjukkan semua data valid.
 
 4. Split Data: Train dan Test
 ```
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42, stratify=y)
```
Data dibagi menjadi 80% data latih dan 20% data uji. Penggunaan stratify=y bertujuan untuk menjaga proporsi label (ganas/jinak) tetap seimbang pada kedua subset.

5. Standarisasi Data
```
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)
```
Standarisasi dilakukan agar setiap fitur memiliki distribusi dengan rata-rata 0 dan standar deviasi 1. Karena fitur dalam skala besar (seperti area_mean) bisa mendominasi model jika tidak dinormalisasi.

6. Reduksi Dimensi dengan PCA
```
pca = PCA(n_components=0.95, random_state=42)
X_train_pca = pca.fit_transform(X_train_scaled)
X_test_pca = pca.transform(X_test_scaled)
```
PCA (Principal Component Analysis) digunakan untuk mengurangi jumlah fitur, namun tetap mempertahankan 95% variansi data. Bagian ini dilakukan untuk membantu mengjindari overfitting dan mempercepat pelatihan model.

## Modeling
Pada tahap modelling ini dilakukan pendekatan klasifikasi untuk memprediksi jenis tumor (jinak atau ganas) berdasarkan data karakteristik numerik tumor payudara/Breast Cancer. Digunakan dua algoritma machine learning yaitu **Random Forest Classifier** dan **XGBoost Classifier**.

1. **Random Forest Classifier**
- Model dilatih menggunakan data hasil PCA
- Model default dari RandomForestClassifier() digunakan tanpa tuning hyperparameter.
```
rf_model = RandomForestClassifier(random_state=42)
rf_model.fit(X_train_pca, y_train)
y_pred_rf = rf_model.predict(X_test_pca)
```
- Parameter utama (default):
  n_estimators=100 (jumlah pohon)
  criterion='gini'
  random_state=42

- Kelebihan:
  Mudah digunakan dan cukup akurat tanpa banyak tuning.
  Mampu menangani dataset dengan fitur numerik dan tidak sensitif terhadap multikolinearitas.

- Kekurangan
  Model cenderung besar (kompleks) dan lambat untuk interpretasi.
  Bisa overfitting jika tidak dikontrol dengan pruning atau max depth.

2. **XGBoost Classifier**
- Model dilatih dengan data PCA menggunakan XGBClassifier.
- Parameter disesuaikan minimal agar tidak ada error label encoder dan untuk menetapkan evaluas
```
xgb_model = XGBClassifier(use_label_encoder=False, eval_metric='logloss', random_state=42)
xgb_model.fit(X_train_pca, y_train)
y_pred_xgb = xgb_model.predict(X_test_pca)
```

- Parameter utama:
  eval_metric='logloss'
  use_label_encoder=False
  random_state=42

- Kelebihan:
  Memiliki performa prediksi yang tinggi, unggul dalam akurasi dan generalisasi.
  Mendukung parallel computing dan regularisasi, sehingga mengurangi risiko overfitting.

- Kekurangan:
  Relatif kompleks, membutuhkan waktu training lebih lama dibanding Random Forest.
  Perlu tuning parameter lebih lanjut untuk mencapai performa optimal.

### Pemilihan Model Terbaik
Berdasarkan hasil evaluasi, XGBoost memberikan performa yang lebih baik dibanding Random Forest, dengan akurasi mencapai 97%, sedangkan Random Forest hanya mencapai 94%. Selain itu, nilai precision dan recall untuk kelas ganas (malignant) juga lebih tinggi pada XGBoost, yang sangat penting dalam konteks deteksi kanker.

Oleh karena itu, model ***XGBoost*** dipilih sebagai solusi akhir dalam proyek klasifikasi ini karena memiliki akurasi yang lebih tinggi dan mampu meminimalkan kesalahan klasifikasi pada kasus tumor ganas.


## Evaluation
### Metrik Evaluasi yang Digunakan
Model dievaluasi menggunakan empat metrik utama klasifikasi, yaitu akurasi, precision, recall, dan F1-score. Pemilihan metrik ini didasarkan pada kebutuhan untuk tidak hanya memperoleh prediksi yang benar secara keseluruhan, tetapi juga untuk meminimalkan kesalahan pada klasifikasi tumor ganas, yang berisiko tinggi.
1. Akurasi: Mengukur seberapa banyak prediksi model yang benar secara keseluruhan.
![Akurasi Rumus](https://i.postimg.cc/zDpg3gs6/accurasy.png)
2. Precision: Mengukur berapa banyak prediksi positif yang benar-benar positif.
![Precision Rumus](https://i.postimg.cc/mrxcKN9z/precision.png)
3. Recall (Sensitivity): Mengukur seberapa banyak kasus positif (ganas) berhasil dikenali oleh model.
![Recall Rumus](https://i.postimg.cc/T1H10rGP/recall.png)
4. F1-score: Merupakan harmonic mean dari precision dan recall.
![Recall Rumus](https://i.postimg.cc/x8JgSJJy/F1-SCORE.avif)

### Hasil Evaluasi Model

| Metrik    | Random Forest | XGBoost |
|-----------|----------------|---------|
| Accuracy  | 93.86%         | 97.37%  |
| Precision | 92.68%         | 97.56%  |
| Recall    | 90.48%         | 95.24%  |
| F1-score  | 91.57%         | 96.39%  |








.
