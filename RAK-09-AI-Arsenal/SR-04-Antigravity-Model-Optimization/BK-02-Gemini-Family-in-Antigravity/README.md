# BK-02: Gemini Family in Antigravity

## Gampangnya...

Keluarga Gemini di Antigravity memberi kamu spektrum yang lebar: dari model cepat seperti `Gemini Flash` sampai varian yang lebih berat seperti `Gemini 3.1 Pro High`. Tantangannya bukan memilih yang paling keren, tapi memilih yang paling masuk akal untuk task yang sedang dikerjakan.

---

## Konteks & Sejarah

Gemini sering menjadi tulang punggung reasoning dan long-context work. Tapi dalam praktik harian, user mudah terjebak:
- Flash dianggap terlalu lemah padahal cukup untuk banyak task,
- Pro dipakai untuk semua hal,
- Pro High dipakai karena gengsi, bukan karena kebutuhan,
- Pro Low membingungkan karena posisinya di tengah.

Buku ini dibuat agar keluarga Gemini terasa seperti toolkit yang jelas, bukan sekadar daftar level.

---

## Cara Kerja

### Peta Keluarga Gemini

| Model | Kesan Umum | Cocok Untuk |
|---|---|---|
| **Gemini Flash** | cepat dan lincah | drafting, rewrite, iterasi, task volume |
| **Gemini 3.1 Pro** | reasoning inti serbaguna | blueprint, analysis, coding menengah-berat |
| **Gemini 3.1 Pro High** | reasoning premium yang lebih berat | debug mahal, audit penting, keputusan arsitektur |
| **Gemini 3.1 Pro Low** | kompromi kualitas dan efisiensi | task menengah yang butuh lebih dari Flash |

### Prinsip Membaca Variannya

- `Flash` untuk kecepatan dan volume
- `Pro` untuk baseline reasoning yang kuat
- `Pro High` untuk task yang mahal kalau salah
- `Pro Low` untuk menahan biaya tanpa jatuh ke mode terlalu ringan

---

## Kapan Digunakan

### Pakai Gemini Flash jika:
- kamu butuh iterasi cepat,
- kamu menulis draft awal,
- task-nya jelas dan tidak terlalu mahal jika salah.

### Pakai Gemini 3.1 Pro jika:
- kamu butuh reasoning yang kuat tapi belum level premium tertinggi,
- kamu sedang blueprint atau analysis,
- kamu ingin model serbaguna yang stabil.

### Pakai Gemini 3.1 Pro High jika:
- task sangat penting,
- debug-nya berat,
- keputusan arsitekturnya mahal kalau salah,
- kamu ingin tingkat kehati-hatian lebih tinggi.

### Pakai Gemini 3.1 Pro Low jika:
- Flash terasa terlalu ringan,
- Pro penuh terasa terlalu boros,
- kamu butuh middle ground yang lebih efisien.

---

## Cara Pakai

### Aturan Praktis

- mulai dari Flash untuk pekerjaan volume,
- naik ke Pro untuk reasoning inti,
- simpan Pro High untuk task mahal,
- gunakan Pro Low sebagai kompromi jika task menengah mulai terasa berat di Flash.

### Template Prompt

```text
"Saya akan mengerjakan [task].
Sebelum mulai, jelaskan:
1. Apakah task ini cukup untuk Flash?
2. Jika tidak, apakah perlu Pro, Pro Low, atau Pro High?
3. Apa alasan trade-off antara kualitas dan kuota?"
```

---

## Lab Praktek

**Skenario: Build dan iterate**

Pagi:
- pakai `Gemini 3.1 Pro` untuk blueprint.

Siang:
- turunkan ke `Gemini Flash` untuk drafting dan execute ringan.

Sore:
- jika ada keputusan kritis, naik ke `Gemini 3.1 Pro High`.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Flash diremehkan** | Semua task langsung ke Pro | Uji dulu apakah Flash cukup |
| **High prestige trap** | Pro High dipakai untuk task receh | Simpan High untuk task mahal |
| **Low membingungkan** | User tidak tahu kapan pakai Pro Low | Gunakan saat Flash mulai kurang tapi High terasa terlalu mahal |

---

## Materi Selanjutnya

- [BK-03: Claude Family in Antigravity](../BK-03-Claude-Family-in-Antigravity/README.md)
