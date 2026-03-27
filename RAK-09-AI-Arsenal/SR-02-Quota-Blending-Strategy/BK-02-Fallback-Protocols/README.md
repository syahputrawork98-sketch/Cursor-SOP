# BK-02: Fallback Protocols — Saat Semua Kuota Habis

## 🌟 Gampangnya...

Inilah "Rencana Darurat" (Plan B). Apa yang harus kamu lakukan jika kuota Gemini Pro habis, Flash sudah mulai ngaco, dan ChatGPT juga limit? **Fallback Protocols** memberikan urutan langkah penyelamatan agar proyekmu tetap berjalan. Ingat: **Seorang AI Orchestrator tidak pernah berhenti bekerja hanya karena kuota habis.**

---

## 📖 Konteks & Sejarah

Dalam ekosistem AI modern, kita punya banyak "Pintu Belakang". Jika pintu utama (Cursor Premium) tertutup, kita bisa menggunakan API key sendiri, beralih ke model Open Source (via Ollama), atau menggunakan trik **"The Handover to ChatGPT Web"**. Protokol ini disusun berdasarkan skala prioritas efisiensi biaya dan waktu.

---

## ⚙️ Cara Kerja

### The Hierarchy of Fallback (Hierarki Penyelamatan)

1. **Level 1 (The Blended)**: Tetap di Cursor, gunakan **Flash + High-Rigor Prompting** (BK-01).
2. **Level 2 (The External)**: Pindah ke **ChatGPT Web** (dengan copy-paste file manual).
3. **Level 3 (The API)**: Gunakan "Bring Your Own Key" (Anthropic/OpenAI API) di dalam Cursor.
4. **Level 4 (The Manual)**: Fokus ke tugas Non-Coding (Planning/SOP) sampai kuota reset.

---

## 🛠️ Cara Pakai

### Teknik "External Brain Handover" (Saat Cursor Limit)

Jika kamu butuh reasoning kuat tapi kuota Cursor habis:
1. Suruh AI di Cursor (Flash) mengumpulkan semua context yang dibutuhkan: *"Ringkas semua logic di file A, B, dan C menjadi satu draf untuk saya bawa ke model eksternal."*
2. Copy hasil ringkasan tersebut.
3. Paste ke ChatGPT Premium.
4. Selesaikan logic di sana, lalu bawa hasilnya kembali ke Cursor.

---

## 🧪 Lab Praktek

**Skenario: Simulasi Kuota Habis**

1. Berlakulah seolah-olah kamu hanya punya akses ke model paling lemah.
2. Gunakan **Level 1 Fallback**: Perbaiki bug sulit hanya dengan instruksi ultra-mendetail.
3. Rasakan "otot" prompting-mu bekerja lebih keras.
4. **Insight**: Kuota terbatas sebenarnya adalah latihan terbaik untuk menjadi *Master Prompter*.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Silent Quota Drain** | Kamu tidak sadar kuota mau habis | Aktifkan notifikasi kuota (jika ada) atau cek menu Settings secara berkala. |
| **API Bill Shock** | Kamu pakai API key pribadi tapi lupa bayarannya mahal | Selalu set **Spending Limit** (Misal: $5 max) di dashboard OpenAI/Anthropic. |
| **Security Risk** | Kamu paste kode rahasia ke model eksternal yang tidak aman | Pastikan model eksternal yang kamu pakai punya fitur "Private Mode" atau "Temporary Chat". |

---

### 📖 Materi Selanjutnya
- [Status Proyek](../../../status.md)
