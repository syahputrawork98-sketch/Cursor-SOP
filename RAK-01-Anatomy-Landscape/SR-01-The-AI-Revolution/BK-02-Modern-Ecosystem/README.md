# BK-02: Modern AI Ecosystem â€” Peta Kekuatan Raksasa AI

## ðŸŒŸ Gampangnya...

Di dunia AI sekarang, ada tiga "kerajaan" besar yang masing-masing punya kelebihan: **OpenAI** (ChatGPT/GPT-4o), **Google** (Gemini), dan **Anthropic** (Claude). Di Cursor, kamu bisa berganti-ganti antar kerajaan ini. Buku ini menjelaskan siapa ahli dalam hal apa, agar kamu tidak salah pilih "pasukan" saat menghadapi masalah koding yang berbeda-beda.

---

## ðŸ“– Konteks & Sejarah

Dulu, GPT-4 adalah satu-satunya raja. Sekarang, persaingan sangat ketat. Gemini unggul dalam memori (bisa baca ribuan file), Claude unggul dalam gaya bahasa dan ketelitian koding, sementara GPT-4o adalah generalis yang sangat cepat. Perpustakaan ini (Cursor-SOP) dirancang agar kompatibel dengan ketiganya.

---

## âš™ï¸ Cara Kerja

### Peta Kekuatan (Ranking 2026)

| Dimensi | Pemenang | Kenapa? |
|---|---|---|
| **Memory (Context Window)** | **Gemini (Google)** | Bisa "mengingat" hingga 2jt+ token. Cocok buat megaproyek. |
| **Reasoning (Logika)** | **Claude (Anthropic)** | Paling jarang bikin bug logika aneh. Sangat teliti. |
| **Speed (Kecepatan)** | **GPT-4o / Flash** | Respons nyaris instan untuk tugas rutin. |

---

## ðŸ—ºï¸ Kapan Memilih Siapa?

| Situasi | Gunakan |
|---|---|
| Ingin AI audit seluruh struktur proyek | **Gemini Pro** (Antigravity) |
| Ingin kodingan yang sangat bersih & elegan | **Claude Sonnet** / **Gemini Pro** |
| Tugas cepat (refactor nama variabel, ganti nama file) | **Gemini Flash** / **GPT-4o-mini** |
| Debugging error yang sangat membingungkan | **Claude** / **o1 (OpenAI)** |

---

## ðŸ› ï¸ Cara Pakai

### Teknik: Model Switching Pre-flight

Sebelum memulai sesi berat:
1. Analisis tingkat kerumitan task.
2. Pilih model di pojok kanan bawah Cursor.

```markdown
# TIPS:
- Pakai **Gemini Pro** jika kamu akan banyak @mention file (Context heavy).
- Pakai **Claude** jika task-nya adalah refactoring logika yang sensitif (Precision heavy).
```

---

## ðŸ§ª Lab Praktek

**Skenario: Membandingkan respons model**

1. Ajukan pertanyaan logika sulit ke Gemini Flash.
2. Jika jawabannya agak "ngaco", ganti ke Gemini Pro atau Claude.
3. Perhatikan perbedaannya dalam memahami nuansa instruksimu.
4. **Insight**: Jangan paksa tentara biasa (Flash) melakukan tugas jenderal (Pro).

---

## âš ï¸ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Loyalitas Buta** | Kamu malas ganti model padahal AI sudah mulai blunder | Ingat: Setiap model punya keterbatasan. Ganti model adalah cara termurah memperbaiki bug. |
| **Boros Quota** | Pakai model Pro cuma buat nanya "cara install npm" | Gunakan model Flash/mini untuk pertanyaan sepele. Hemat Pro untuk "Perang Besar". |
| **Context Lost after Switch** | Saat ganti model, AI lupa diskusi sebelumnya | Tenang, di Cursor konteks chat tetap terbawa meski model diganti. |

---

### ðŸ“– Materi Selanjutnya
- [RAK-01/SR-02: AI as Partner Philosophy](../../SR-02-AI-as-Partner-Philosophy/BK-01-The-Cyborg-Mindset/README.md)

