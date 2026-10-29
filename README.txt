# RAG Literature Gap Matrix for Supply Chain Risk Management (SCRM)

## 1. Deskripsi Proyek

Proyek ini bertujuan mengembangkan pipeline **Retrieval-Augmented Generation (RAG)** untuk membantu proses analisis literatur ilmiah dan penyusunan *Literature Gap Matrix* pada domain **Supply Chain Risk Management (SCRM)**.

Pipeline ini memanfaatkan dokumen artikel ilmiah sebagai sumber informasi untuk mengidentifikasi masalah penelitian, metode, dataset, temuan, keterbatasan, dan peluang penelitian lanjutan (*future work*).

Hasil analisis digunakan untuk membantu proses sintesis literatur dan mengidentifikasi potensi *research gap* sebagai dasar pengembangan usulan penelitian.

## 2. Tujuan

- Mengumpulkan dan mengolah referensi artikel ilmiah pada domain SCRM.
- Mengekstraksi informasi penting dari artikel ilmiah.
- Menerapkan pendekatan RAG untuk mengambil informasi yang relevan dari dokumen.
- Menyusun Literature Gap Matrix berdasarkan hasil analisis literatur.
- Mengidentifikasi keterbatasan penelitian terdahulu dan peluang penelitian lanjutan.
- Menghasilkan sintesis research gap untuk mendukung pengembangan ide penelitian.

## 3. Domain Penelitian

**Supply Chain Risk Management (SCRM)**

Domain ini berfokus pada pengelolaan risiko dalam rantai pasok, termasuk identifikasi risiko, mitigasi risiko, penggunaan teknologi, kecerdasan buatan, dan pengambilan keputusan berbasis informasi.

## 4. Metodologi

Pipeline dirancang menggunakan tahapan berikut:

1. **Input Dokumen**  
   Menyiapkan artikel ilmiah yang relevan dengan topik SCRM.

2. **Document Processing**  
   Mengekstraksi teks dari dokumen PDF dan mempersiapkannya untuk diproses.

3. **Text Chunking**  
   Membagi teks menjadi beberapa bagian agar informasi lebih mudah diindeks dan dicari.

4. **Embedding dan Indexing**  
   Mengubah potongan teks menjadi representasi vektor untuk mendukung pencarian semantik, jika menggunakan embedding.

5. **Retrieval**  
   Mengambil potongan teks yang relevan berdasarkan pertanyaan atau aspek yang dianalisis.

6. **Generation dan Synthesis**  
   Menggunakan konteks hasil retrieval untuk membantu menyusun informasi literatur dan kandidat research gap.

7. **Literature Gap Matrix**  
   Menyusun hasil analisis ke dalam tabel terstruktur.

8. **Validation**  
   Memeriksa kesesuaian metadata, metode, temuan, keterbatasan, dan informasi lain terhadap artikel ilmiah asli.

*Catatan: Tahapan teknis yang benar-benar diterapkan mengikuti implementasi pada notebook yang tersedia di repository.*

## 5. Struktur Repository

```text
RAG-Literature-Gap-Matrix/
├── README.md
├── requirements.txt
└── RAG_Literature_Gap_Matrix.ipynb
```

Keterangan:

- `README.md`: dokumentasi proyek.
- `requirements.txt`: daftar dependensi Python yang dibutuhkan.
- `RAG_Literature_Gap_Matrix.ipynb`: notebook berisi implementasi pipeline RAG.

## 6. Teknologi

Teknologi yang dapat digunakan dalam proyek ini meliputi:

- Python
- Google Colab
- Pandas dan NumPy untuk pengolahan data
- PyPDF untuk ekstraksi teks PDF
- Sentence Transformers dan PyTorch jika digunakan untuk embedding
- Scikit-learn jika digunakan untuk pemrosesan atau analisis tambahan

Dependensi aktual mengikuti kode dan file `requirements.txt` pada repository.

## 7. Output Proyek

Output yang ditargetkan meliputi:

- Literature Gap Matrix untuk 10 artikel ilmiah.
- Informasi masalah penelitian (*problem*).
- Metode penelitian (*method*).
- Dataset yang digunakan.
- Temuan penelitian (*findings*).
- Keterbatasan penelitian (*limitations*).
- Peluang penelitian lanjutan (*future work*).
- Analisis sintesis research gap sebagai dasar usulan penelitian.

## 8. Cara Menjalankan

### Menggunakan Google Colab

1. Buka notebook `RAG_Literature_Gap_Matrix.ipynb`.
2. Unggah atau siapkan dokumen artikel ilmiah sesuai petunjuk di notebook.
3. Pastikan dependensi yang diperlukan sudah terpasang.
4. Jalankan setiap sel notebook secara berurutan.
5. Periksa hasil retrieval dan hasil penyusunan Literature Gap Matrix.
6. Validasi hasil terhadap artikel ilmiah asli sebelum digunakan dalam laporan.

### Instalasi Dependensi

Jika menjalankan proyek di lingkungan Python yang mendukung `pip`, gunakan perintah:

```bash
pip install -r requirements.txt
```

## 9. Validasi Hasil

Hasil yang dihasilkan oleh pipeline RAG tidak otomatis dianggap benar. Informasi penting perlu diperiksa kembali dengan artikel sumber, khususnya:

- Judul, penulis, tahun, dan DOI.
- Metode penelitian dan dataset.
- Temuan utama.
- Keterbatasan yang dinyatakan oleh penulis.
- Future work yang dinyatakan atau disarankan dalam artikel.
- Kutipan dan nomor halaman, apabila digunakan sebagai bukti.

Perbedaan antara keterbatasan eksplisit dari penulis dan interpretasi hasil sintesis harus dijelaskan dengan jelas.

## 10. Batasan

- Kualitas hasil bergantung pada relevansi dan kualitas artikel yang digunakan.
- PDF hasil pemindaian atau dokumen dengan format yang kompleks dapat memengaruhi ekstraksi teks.
- Retrieval dapat melewatkan informasi yang relevan jika pemotongan teks atau pencarian kurang sesuai.
- Research gap yang dihasilkan tetap memerlukan evaluasi dan validasi manusia.
- Hasil analisis tidak menggantikan pembacaan kritis terhadap artikel ilmiah asli.

## 11. Luaran Akademik

Proyek ini dikembangkan untuk mendukung tugas akademik mengenai penerapan RAG dalam analisis literatur dan penyusunan Literature Gap Matrix pada domain Supply Chain Risk Management.

Hasil akhir meliputi source code pipeline, Literature Gap Matrix, dan analisis research gap.

## 12. Author

Nama: [Nama anggota atau kelompok]

Institusi: [Nama universitas]

Mata Kuliah: [Nama mata kuliah]

Repository: [URL repository GitHub]

---

**Disclaimer:** Literature Gap Matrix merupakan hasil bantuan analisis berbasis dokumen. Semua klaim akademik perlu diverifikasi dengan artikel ilmiah sumber sebelum digunakan dalam laporan atau publikasi.