# 🧠 Predictive QA Using Mining Software Repositories  
*Workflow overview for building a defect prediction model*

Dokumentasi ini merangkum alur penelitian berdasarkan diagram proses, memberikan gambaran menyeluruh mengenai bagaimana model prediksi defect dikembangkan.

---

## 1. 📚 Literature Review
Meninjau penelitian sebelumnya terkait **Mining Software Repositories (MSR)**, **defect prediction**, dan berbagai pendekatan **machine learning**.  
Tahap ini bertujuan mengidentifikasi *research gap*, metrik, serta metode yang relevan.

---

## 2. 📥 Data Extraction
Mengumpulkan data repository GitHub melalui API, meliputi **commits**, **issues**, dan **pull requests**.

**Sub-tahapan utama:**
- **Commit–File Mapping** – Menghubungkan commit dengan file yang dimodifikasi.  
- **Data Cleaning** – Menghilangkan noise dan anomali.

---

## 3. 🏷️ Labeling
Memberi label *defective* atau *non-defective* pada file dengan mendeteksi **bug-fix commits** melalui kata kunci dan tautan issue.  
File yang muncul dalam bug-fix commit ditandai sebagai *defective*.

---

## 4. 🔗 Dataset Alignment
Menggabungkan data commit, data file, dan informasi bug-fix menjadi dataset terstruktur yang siap digunakan untuk pemodelan.

---

## 5. 🛠️ Feature Engineering
Menghasilkan berbagai **process metrics**, termasuk:

- Code churn  
- Commit frequency  
- Developer experience  
- Past defects  
- Time since last modification  

Metrik-metrik ini menjadi input utama bagi model prediksi.

---

## 6. ✂️ Dataset Split
Memecah dataset menjadi **training** dan **testing set** (misal: 80:20) untuk evaluasi model yang objektif.

---

## 7. 🤖 Model Training
Melatih model machine learning seperti:  
- Logistic Regression  
- Random Forest  

Model diberi input berupa metrik proses untuk mengestimasi risiko defect.

---

## 8. 🎯 Model Prediction
Model menghasilkan prediksi risiko defect per file (probabilitas atau kategori risiko).

---

## 9. 📊 Model Evaluation
Evaluasi performa menggunakan metrik standar seperti:

- Accuracy  
- Precision  
- Recall  
- F1-Score  
- ROC-AUC  

---

## 10. 📈 Visualization & Interpretation
Menampilkan hasil dalam bentuk grafik seperti:

- Risk ranking  
- Heatmaps  
- Evaluation plots  

Visualisasi membantu memahami pola risiko dan mendukung prioritas QA.

---

## 11. 📝 Conclusion
Menutup proses dengan rangkuman temuan, kontribusi, batasan penelitian, serta peluang pengembangan ke depan.

---
