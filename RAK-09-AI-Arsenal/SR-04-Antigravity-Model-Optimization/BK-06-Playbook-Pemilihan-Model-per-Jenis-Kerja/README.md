# BK-06: Playbook Pemilihan Model per Jenis Kerja

## Gampangnya...

Kalau buku-buku sebelumnya menjelaskan teori dan keluarga model, buku ini adalah **cheat sheet kerja harian**. Saat kamu sedang sibuk, kamu tidak ingin membaca seluruh teori lagi. Kamu hanya ingin tahu: "untuk task ini, model mana yang paling tepat?"

---

## Konteks & Sejarah

Banyak sub-rak bagus gagal dipakai karena terlalu teoritis. User paham setelah membaca, tapi saat kembali bekerja dia tetap bingung memilih model. Karena itu, buku ini dibuat sebagai jembatan terakhir antara teori dan keputusan nyata.

---

## Cara Kerja

### Tabel Pemilihan Cepat

| Jenis Kerja | Model Awal | Model Cadangan | Hindari Jika Bisa |
|---|---|---|---|
| **Blueprint** | Gemini 3.1 Pro | Claude Sonnet 4.6 Thinking | GPT-OSS 120B Medium |
| **Planning** | Gemini 3.1 Pro Low | Gemini 3.1 Pro | Claude Opus 4.6 Thinking |
| **Analysis** | Gemini 3.1 Pro | Claude Sonnet 4.6 Thinking | GPT-OSS 120B Medium |
| **Execute ringan** | Gemini Flash | GPT-OSS 120B Medium | Gemini 3.1 Pro High |
| **Review** | Claude Sonnet 4.6 Thinking | Gemini 3.1 Pro | GPT-OSS 120B Medium |
| **Debug berat** | Gemini 3.1 Pro High | Claude Opus 4.6 Thinking | GPT-OSS 120B Medium |
| **Refactor** | Gemini 3.1 Pro | Claude Sonnet 4.6 Thinking | Gemini 3.1 Pro High |
| **Document** | Gemini Flash | GPT-OSS 120B Medium | Claude Opus 4.6 Thinking |

### Cara Membaca Tabel

- `Model Awal` adalah pilihan paling masuk akal untuk mulai.
- `Model Cadangan` dipakai jika kamu butuh sudut pandang lain atau kualitas lebih tinggi.
- `Hindari Jika Bisa` bukan berarti dilarang, tapi artinya ada opsi yang lebih efisien.

---

## Kapan Digunakan

Gunakan buku ini saat:
- kamu butuh keputusan cepat,
- kamu sedang kerja harian dan tidak ingin overthinking picker,
- kamu ingin memilih model berdasarkan jenis kerja, bukan berdasarkan gengsi model.

---

## Cara Pakai

### Aturan Cepat

1. Untuk `blueprint` dan `analysis`, mulai dari model reasoning yang stabil.
2. Untuk `execute ringan` dan `document`, turunkan ke model cepat atau hemat.
3. Untuk `debug berat` dan `audit final`, naikkan ke premium tertinggi hanya jika perlu.
4. Jika task berubah fase, modelnya juga boleh berubah fase.

### Workflow Campuran

**Proyek baru**
- mulai di `Gemini 3.1 Pro`,
- execute ringan di `Gemini Flash`,
- audit final jika perlu di `Claude Sonnet 4.6 Thinking`.

**Bugfix berat**
- diagnosis di `Gemini 3.1 Pro High`,
- second opinion jika perlu di `Claude Opus 4.6 Thinking`,
- dokumentasi hasil di `Gemini Flash`.

**Refactor besar**
- analisis di `Gemini 3.1 Pro`,
- review hasil di `Claude Sonnet 4.6 Thinking`,
- handover di `GPT-OSS 120B Medium` atau `Gemini Flash`.

---

## Lab Praktek

**Skenario: Task berpindah fase**

Task awal:
"Buat arsitektur modul baru."

Model awal:
- `Gemini 3.1 Pro`

Saat fase berubah menjadi drafting dan boilerplate:
- turunkan ke `Gemini Flash` atau `GPT-OSS 120B Medium`

Saat fase berubah jadi audit final:
- naikkan jika perlu ke `Claude Sonnet 4.6 Thinking` atau `Gemini 3.1 Pro High`

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Cheat sheet dibaca kaku** | Semua task dipaksa ikut tabel mentah | Gunakan tabel sebagai baseline, bukan hukum absolut |
| **Model tidak turun setelah fase berubah** | Execute ringan tetap di premium mahal | Sesuaikan model dengan fase kerja |
| **Tidak ada cadangan** | Saat satu model tidak cocok, user buntu | Selalu lihat kolom model cadangan |

---

## Materi Sebelumnya

- [BK-01: Antigravity Model Landscape](../BK-01-Antigravity-Model-Landscape/README.md)
