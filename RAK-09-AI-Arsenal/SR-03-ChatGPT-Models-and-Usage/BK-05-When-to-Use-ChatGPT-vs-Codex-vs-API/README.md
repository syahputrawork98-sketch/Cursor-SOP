# BK-05: When to Use ChatGPT vs Codex vs API

## Gampangnya...

ChatGPT, Codex, dan API datang dari keluarga yang sama, tapi pekerjaan idealnya berbeda. ChatGPT unggul untuk dialog, penjelasan, dan analisis cepat. Codex lebih cocok untuk kerja agentic di codebase. API cocok ketika kamu ingin membangun produkmu sendiri.

Kalau kamu tahu kapan harus pindah alat, kamu akan jauh lebih efisien dan lebih sedikit salah ekspektasi.

> Status per 2026-03-28.

---

## Konteks & Sejarah

Semakin dewasa ekosistem OpenAI, semakin penting membedakan tiga konteks kerja:
- **ChatGPT** untuk interaksi langsung manusia-model,
- **Codex** untuk agentic coding,
- **API** untuk integrasi ke aplikasi.

Masalah umum user adalah berharap satu alat bisa melakukan semua hal dengan sama baiknya. Padahal, desain produk setiap alat berbeda.

---

## Cara Kerja

| Alat | Fokus Utama | Cocok Untuk |
|---|---|---|
| **ChatGPT** | Chat, reasoning, drafting, review | Brainstorming, penjelasan, analisis, planning |
| **Codex** | Agentic coding | Membaca repo, mengedit file, menjalankan task coding |
| **API** | Integrasi produk | Fitur AI di aplikasi sendiri, workflow otomatis |

### Tentang Model Codex/API

Nama-nama berikut termasuk ke ranah model teknis atau coding-focused, bukan default picker ChatGPT biasa:
- `gpt-5.3-codex`
- `gpt-5.2-codex`
- `gpt-5.1-codex-max`
- `gpt-5.1-codex-mini`
- `gpt-5 mini`

Artinya:
- mereka penting untuk dipahami,
- tapi jangan dicampur seolah-olah semuanya adalah opsi utama di UI ChatGPT.

---

## Kapan Digunakan

### Gunakan ChatGPT jika:

- kamu ingin diskusi,
- kamu sedang blueprint,
- kamu ingin penjelasan cepat,
- kamu sedang review atau synthesis.

### Gunakan Codex jika:

- kamu ingin agent membaca codebase,
- kamu butuh edit file nyata,
- kamu ingin task coding yang lebih terikat ke workspace dan tooling.

### Gunakan API jika:

- kamu sedang membangun produk sendiri,
- kamu butuh model di backend atau automation,
- kamu ingin kontrol programatis terhadap request dan response.

---

## Cara Pakai

### Workflow yang Efisien

1. Gunakan ChatGPT untuk:
   - memperjelas masalah,
   - menyusun blueprint,
   - membandingkan opsi.
2. Gunakan Codex untuk:
   - membaca repo,
   - mengubah file,
   - menjalankan pekerjaan coding.
3. Gunakan API untuk:
   - memindahkan workflow yang sudah matang ke produk nyata.

### Contoh Alur Kerja

- diskusi arsitektur di ChatGPT,
- implementasi dan edit file di Codex,
- integrasi fitur ke aplikasi melalui API.

---

## Lab Praktek

**Skenario: membangun fitur baru**

Tahap 1:
gunakan ChatGPT untuk membedah requirement dan menyusun blueprint.

Tahap 2:
gunakan Codex untuk implementasi, review, dan iterasi di repo.

Tahap 3:
jika fitur itu akan menjadi kemampuan produk, gunakan API untuk integrasi ke aplikasi.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **ChatGPT dipaksa jadi coding agent penuh** | Hasil tidak sepresisi workflow agentic | Pindah ke Codex untuk kerja repo nyata |
| **Codex dipakai untuk diskusi ringan** | Workflow terasa terlalu berat | Gunakan ChatGPT untuk ideasi dan review awal |
| **API dibahas terlalu cepat** | User bingung padahal belum butuh integrasi | Tahan dulu sampai use case produk benar-benar matang |
| **Campur model picker dengan model ID** | Salah ekspektasi terhadap UI | Kembali ke BK-01 dan bedakan konteks alat |

---

## Referensi Resmi

- https://platform.openai.com/docs/models/gpt-5.3-codex
- https://platform.openai.com/docs/models/gpt-5.2-codex
- https://platform.openai.com/docs/models/gpt-5.1-codex-max
- https://platform.openai.com/docs/models/gpt-5.1-codex-mini
- https://platform.openai.com/docs/models/gpt-5-mini

---

## Materi Sebelumnya

- [BK-01: ChatGPT Product Map](../BK-01-ChatGPT-Product-Map/README.md)
