# BK-02: Tree-of-Thought (ToT) — Menjelajah Berbagai Cabang Solusi

## 🌟 Gampangnya...

Kalau **Chain-of-Thought (CoT)** adalah berpikir dalam satu garis lurus (satu solusi saja), maka **Tree-of-Thought (ToT)** adalah berpikir bercabang. AI disuruh membayangkan 3 atau 4 cara berbeda untuk menyelesaikan satu masalah, lalu dia sendiri yang mengaudit mana cara yang paling masuk akal sebelum memberitahukannya padamu. Ini seperti mengadakan rapat kabinet di dalam kepala AI.

---

## 📖 Konteks & Sejarah

Dalam pemecahan masalah yang kompleks (seperti arsitektur software), seringkali tidak ada satu jawaban tunggal yang benar. ToT memungkinkan AI untuk melakukan eksplorasi (*exploration*) dan evaluasi (*self-evaluation*) secara bersamaan. Teknik ini terbukti mampu memecahkan masalah yang membuat AI "biasa" menyerah atau hanya berputar-putar.

---

## ⚙️ Cara Kerja

### Mekanisme Cabang Logika

1. **Generation**: AI membuat 3 "Ide Kasar" (Branches).
2. **Evaluation**: AI memberikan skor/rating untuk setiap ide berdasarkan kriteria (performansi, kemudahan, keamanan).
3. **Elimination**: AI membuang ide yang buruk.
4. **Conclusion**: AI melanjutkan ide yang terbaik sampai tuntas.

---

## 🗺️ Kapan Mode Ini Relevan

| Task | Mode | Kenapa ToT? |
|---|---|---|
| **Pilih Library** | 📐 **BLUEPRINT** | Bandingkan 3 library yang mirip. |
| **Optimasi Performa** | ♻️ **REFACTOR** | Cari cara paling efisien buat memproses data. |
| **Security Audit** | 🔬 **ANALYZE** | Bayangkan berbagai skenario serangan (attack vectors). |

---

## 🛠️ Cara Pakai

### Template: ToT Protocol

Ketikkan prompt ini untuk masalah yang sangat rumit:
```markdown
"Gunakan Tree-of-Thought (ToT) untuk masalah ini:
 1. Berikan 3 alternatif arsitektur berbeda untuk [NAMA FITUR].
 2. Untuk setiap alternatif, sebutkan PRO dan KONTRA-nya.
 3. Beri nilai (1-5) untuk aspek: Kecepatan, Security, Scalability.
 4. Pilih satu yang terbaik dan jelaskan alasannya secara teknis.
 Tunggu instruksi saya sebelum koding."
```

### Teknik 2: The Critic vs Creative AI

Minta AI untuk berdebat dengan dirinya sendiri:
```markdown
"Buat dua persona: 
 Persona A: Developer Kreatif (usulkan solusi out-of-the-box).
 Persona B: Security Auditor (cari celah di solusi A).
 Biarkan mereka berdiskusi 2 turn, lalu berikan solusi finalnya."
```

---

## 🧪 Lab Praktek

**Skenario: Memilih Database (SQL vs NoSQL)**

Kamu tidak yakin mau pakai PostgreSQL atau MongoDB.

**Cara ToT:**
1. Prompt: *"ToT: Bandingkan PostgreSQL vs MongoDB untuk aplikasi sosial media dengan 1 juta user."*
2. AI akan me-list skenario di cabang-cabang: "Cabang 1: SQL (Data integritas tinggi)... Cabang 2: NoSQL (Skalabilitas horizontal)... Cabang 3: Hybrid..."
3. **Hasil**: Kamu dapat gambaran utuh dan alasan kuat dibalik pemilihan database tersebut.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Analysis Paralysis** | AI terlalu lama berdiskusi dan tidak memberi kode | Batasi max 3 alternatif saja. |
| **Surface Comparison** | AI cuma bilang "ini bagus, itu juga bagus" | Paksa dengan metrik skor numerik (1-5). |
| **Quota Hunger** | ToT memakan sangat banyak token | Gunakan hanya untuk level **ARSKITEKTUR/DESIGN**. Jangan untuk koding fungsi kecil. |

---

### 📖 Materi Selanjutnya
- [SR-02: Advanced Prompt Patterns](../SR-02-Advanced-Prompt-Patterns/README.md)
