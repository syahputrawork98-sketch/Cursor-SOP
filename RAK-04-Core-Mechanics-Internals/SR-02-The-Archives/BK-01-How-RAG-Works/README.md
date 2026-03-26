# BK-01: How RAG Works — Rahasia AI "Melihat" Kodemu

## 🌟 Gampangnya...

Bagaimana AI bisa tahu file mana yang relevan di ribuan file proyekmu, bahkan tanpa kamu panggil dengan `@`? Itu berkat **RAG (Retrieval-Augmented Generation)**. Bayangkan RAG adalah asisten perpustakaan yang sangat cepat. Saat kamu bertanya sesuatu, dia berlari ke gudang, mencari buku-buku yang mirip, membukanya, lalu membisikkan isinya ke telinga AI agar AI bisa menjawab dengan pintar.

---

## 📖 Konteks & Sejarah

AI dasar hanya tahu ilmu sampai tanggal dia dilatih (misal: 2023). Dia tidak tahu kode yang baru kamu tulis tadi pagi. RAG adalah cara untuk **menyuntikkan pengetahuan baru** (kodemu) ke dalam proses berpikir AI secara real-time. Tanpa RAG, AI hanyalah seorang ahli koding yang amnesia terhadap proyekmu.

---

## ⚙️ Cara Kerja

### The 3 Steps of RAG in Cursor

1. **Indexing (The Librarian)**: Cursor memindai seluruh folder proyekmu dan mengubah teks menjadi angka koordinat (Vektor).
2. **Retrieval (The Search)**: Saat kamu bertanya, Cursor mencari koordinat "paling dekat" dengan pertanyaanmu (pencarian semantik).
3. **Feeding (The Context)**: Cursor "menempelkan" isi file yang ditemukan itu ke instruksimu secara otomatis.

---

## 🗺️ Kapan Mode Ini Relevan

| Aktivitas | Peran RAG |
|---|---|
| **Global Search** | Mencari fungsi yang namanya kamu lupa. |
| **Codebase Chat** | Menjawab pertanyaan "Bagaimana alur login di aplikasi ini?" |
| **Background Indexing** | Memastikan file baru segera terdaftar di ingatan AI. |

---

## 🛠️ Cara Pakai

### Teknik "Semantic Search Optimization"

Agar RAG mudah menemukan filemu, gunakan nama fungsi dan komentar yang **Deskriptif (Semantic)**.

```markdown
# ❌ JELEK (RAG sulit mencari):
function fn1(p) { ... } // buat simpan data

# ✅ BAGUS (RAG sangat mudah mencari):
function saveUserToDatabase(userData) { ... } // menyimpan data ke Postgres
```

---

## 🧪 Lab Praktek

**Skenario: Bertanya tanpa @mention**

1. Pastikan status Indexing di pojok kanan bawah Cursor sudah "Finished".
2. Gunakan mode `@codebase` (tekan `Ctrl/Cmd + Enter`).
3. Tanya hal yang tersebar di banyak file: *"Jelaskan hubungan antara skema database dan API endpoint produk."*
4. Perhatikan bagaimana Cursor berhasil me-retrieve file yang tepat meski kamu tidak menyebutkan namanya.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Dirty Index** | AI mengambil referensi dari folder `node_modules` atau `dist` | Update `.cursorignore` (RAK-05) agar RAG hanya fokus di kode sumber. |
| **Outdated Index** | Kamu baru edit file mendalam tapi AI masih pakai versi lama | Klik **Rescan Codebase** di settings Cursor. |
| **Ambiguous Query** | Kamu bertanya terlalu singkat ("Kenapa error?") | Berikan kata kunci fungsional: "Kenapa error di *login flow*?" (Membantu RAG memfilter file). |

---

### 📖 Materi Selanjutnya
- [Fase Selanjutnya: Advanced & Arsenal (RAK-07 s/d 09)](../../status.md)
