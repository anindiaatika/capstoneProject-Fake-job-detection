<img width="2366" height="62" alt="image" src="https://github.com/user-attachments/assets/a42182ab-5762-4ee9-af09-88d188f10e35" /># Capstone Project: Fake Job Postings Detection using AI

## 1. Project Overview
Lowongan kerja palsu (fake job postings) merupakan salah satu permasalahan serius di era digital. Banyak individu menjadi korban akibat tergiur oleh tawaran pekerjaan yg tampak menarik namun sebenarnya palsu. Seiring dengan meningkatnya penggunaan platform pencarian kerja digital, kasus penipuan ini pun semakin marak terjadi. Berdasarkan data Bareskrim dan Kemlu RI, ribuan masyarakat menjadi korban, dengan kerugian hingga miliaran rupiah. Di level global, kasus serupa juga meningkat tajam.

Proyek ini bertujuan untuk **mendeteksi dan memahami karakteristik lowongan kerja palsu** melalui kombinasi model Machine Learning (BiLSTM) dan Large Language Model (LLM IBM Granite).

Dataset yang digunakan bersifat publik dan diambil dari Kaggle. Proyek ini mengeksplorasi data menggunakan pendekatan analisis berbasis AI dan bertujuan menghasilkan **insight yang konkret serta rekomendasi nyata untuk menghindari penipuan lowongan kerja**.

## 2. Raw Dataset
Dataset: Real or Fake? Fake Jobposting Prediction (https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction)

## 3.Analysis Process
Analisis dilakukan dalam dua tahap utama:
### 1. **Model Klasifikasi BiLSTM**
- Melalui tahapan preprocessing (cleaning, tokenizing, padding)
- Dilatih menggunakan model BiLSTM untuk klasifikasi fake/real
- Hasilnya menunjukkan akurasi yang cukup tinggi dan dapat digunakan sebagai baseline

### 2. **Insight dengan IBM Granite LLM**
- Digunakan untuk menggali pemahaman yang lebih dalam terhadap karakteristik job posting palsu
- Proses ini dilakukan dengan prompt-prompt berbasis pertanyaan seperti:
  - Pola umum dalam deskripsi pekerjaan palsu
  - Perbedaan struktur dan bahasa antara lowongan asli dan palsu
  - Evaluasi terhadap contoh deskripsi pekerjaan

## 4. Insight & Findings
Berikut beberapa insight utama dari hasil analisis:
- **Karakteristik Umum Lowongan Palsu:**
  - Menawarkan gaji besar tanpa pengalaman
  - Sering meminta "klik link", "mulai sekarang juga", atau ajakan mencurigakan
  - Tidak menyebutkan nama perusahaan secara jelas

- **Perbedaan Real vs Fake:**
  - Job asli memiliki struktur rapi, menyebutkan persyaratan teknis, dan lebih detail
  - Lowongan palsu sering mengandung bahasa persuasif berlebihan dan tidak spesifik

- **Analisis LLM menghasilkan ringkasan dan evaluasi yang menjelaskan kenapa deskripsi tertentu tergolong palsu**, misalnya:
  - "Terlalu menjanjikan"
  - "Tidak menyebutkan tanggung jawab jelas"
  - "Mengandung link yang mencurigakan"

## 5. Conclusion & Recommendations

- **Kesimpulan:**
Gabungan model BiLSTM dan IBM Granite LLM memberikan pendekatan komprehensif. BiLSTM mengklasifikasikan secara otomatis, sementara LLM memberi pemahaman mendalam terhadap konten.
- **Rekomendasi:**
  - Pencari kerja sebaiknya berhati-hati terhadap iklan kerja yang tidak menyebutkan nama perusahaan
  - Perlu dibuat sistem screening tambahan menggunakan model AI pada platform lowongan kerja
  - Model LLM sangat cocok digunakan sebagai layer interpretasi tambahan terhadap output klasifikasi model ML
 
## 6. AI Support Explanation

- **Model BiLSTM:** Digunakan untuk supervised classification (real/fake) pada deskripsi pekerjaan.
- **LLM (IBM Granite):** Digunakan untuk analisis deskriptif dan eksplorasi insight mendalam menggunakan prompt berbasis natural language.
- Platform: Google Colab + Replicate API
- Prompt contohnya: 
  - “What patterns are common in fake job descriptions?”
  - “Is this job post real or fake? Explain in 3 bullet points.”
