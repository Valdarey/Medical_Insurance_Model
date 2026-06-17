# Prediksi Biaya Asuransi Kesehatan

Project ini membangun model **regresi machine learning** untuk memprediksi biaya asuransi kesehatan (`charges`) berdasarkan profil seseorang.

## Tentang Dataset

Dataset berisi informasi 1.337 individu dengan fitur:

| Fitur | Keterangan |
|---|---|
| `age` | Umur |
| `sex` | Jenis kelamin |
| `bmi` | Body Mass Index |
| `children` | Jumlah anak/tanggungan |
| `smoker` | Status merokok (yes/no) |
| `region` | Wilayah tempat tinggal |
| `charges` | Biaya asuransi (target prediksi) |

## Tujuan

Menjawab pertanyaan: *"Berdasarkan profil seseorang, berapa estimasi biaya asuransi kesehatan yang akan dikenakan?"*

## Tools & Library

- Python, Pandas, NumPy
- Scikit-learn (preprocessing, model, evaluasi)
- Matplotlib, Seaborn (visualisasi)
- Joblib (simpan model)

## Model yang Dibandingkan

| Model | MAE | R² Score |
|---|---|---|
| Linear Regression | $4,177 | 0.807 |
| Decision Tree | $2,805 | 0.810 |
| Random Forest | $2,663 | 0.878 |
| **Gradient Boosting** | **$2,517** | **0.901** |

Model terbaik (**Gradient Boosting**) mampu menjelaskan **90% variasi** biaya asuransi.

## Insight Utama

Berdasarkan feature importance, dua faktor paling dominan adalah:
1. **Status merokok** — perokok membayar ±4x lebih mahal
2. **Umur** — semakin tua, biaya cenderung meningkat

Faktor gender dan wilayah hampir tidak berpengaruh terhadap biaya.

## Struktur File

```
├── insurance_analysis.ipynb     # Notebook lengkap (EDA + model + evaluasi)
├── model_insurance.pkl          # Model yang sudah dilatih
├── data/
│   └── medical_insurance.csv    # Dataset
└── README.md
```

## Cara Menjalankan

```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib
jupyter notebook insurance_analysis.ipynb
```

## Visualisasi

Notebook mencakup:
- Correlation matrix antar fitur numerik
- Boxplot biaya berdasarkan status merokok
- Perbandingan performa 4 model
- Feature importance

---

**Dibuat sebagai project pembelajaran Data Science — regresi dengan Scikit-learn.**
