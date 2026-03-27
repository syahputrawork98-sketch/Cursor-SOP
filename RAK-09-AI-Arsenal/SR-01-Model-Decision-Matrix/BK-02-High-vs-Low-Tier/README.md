# BK-02: High-vs-Low Tier Budgeting — Efisiensi Tanpa Batas

## 🌟 Gampangnya...

Bayangkan kamu adalah manajer proyek yang punya 1 Jenderal (Model Pro) dan 10 Prajurit (Model Flash). Jenderal itu sangat pintar tapi mahal dan jumlahnya sedikit (ada kuota). Prajurit itu cepat dan gratis (tak terbatas) tapi terkadang ceroboh. **High-vs-Low Tier Budgeting** adalah cara kamu mengatur kapan harus menurunkan Jenderal ke medan perang, dan kapan cukup mengirim Prajurit untuk tugas harian.

---

## 📖 Konteks & Sejarah

Banyak user menghabiskan kuota "Pro" mereka hanya untuk bertanya hal sepele seperti *"Apa perintah NPM untuk install React?"*. Akibatnya, saat mereka butuh AI untuk debugging error yang sangat sulit, kuotanya sudah habis. Strategi budgeting ini memastikan "Otak Besar" AI hanya digunakan untuk "Masalah Besar".

---

## ⚙️ Cara Kerja

### Pembagian Tugas (Triage Level)

- **Low-Tier (Gemini Flash / GPT-4o-mini)**:
  - Tugas rutin: Ganti nama file, buat komentar, pasang folder.
  - Pertanyaan umum: Perintah terminal, help docs library.
- **High-Tier (Gemini Pro / Claude 3.5 Sonnet)**:
  - Fitur baru: Membangun logika dari nol.
  - Refactoring: Mengubah struktur banyak file sekaligus.
  - Debugging: Mencari error yang penyebabnya tidak jelas.

---

## 🛠️ Cara Pakai

### Aturan Emas: The 3-Turn Policy

1. Gunakan **Flash** (Low-tier) untuk instruksi awal.
2. Jika dalam **3 Turn (percobaan)** Flash masih gagal atau "offside", jangan teruskan! Kamu hanya akan membuang waktu.
3. Langsung switch ke **Pro** (High-tier) di turn ke-4.

```markdown
# TIPS:
Ubah model di pojok kanan bawah Cursor SECARA SADAR 
sesuai tingkat kesulitan task!
```

---

## 🧪 Lab Praktek

**Skenario: Refactor Style CSS**

1. Mode: **Low-Tier (Flash)**.
2. Instruksi: *"Ganti semua warna biru menjadi indigo di seluruh file CSS."* (Flash sangat jago di sini).
3. Setelah selesai...
4. Task baru: *"Optimalkan performa rendering halaman ini."*
5. Mode: Switch ke **High-Tier (Pro)** sebelum menekan Enter.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Flash Offside** | Flash mulai ngaco dan menghapus kode penting | Stop! Flash kelelahan membaca context. Switch ke Pro. |
| **Quota Panic** | Kuota Pro tinggal 10% di awal bulan | Mulai gunakan **Blended Workflows** (RAK-09/SR-02). |
| **Under-estimating Flash** | Kamu pakai Pro untuk segalanya | Coba tantang Flash untuk tugas menengah. Kamu akan kaget betapa pintarnya dia jika dipadu dengan **RAK-06 (Advanced Prompt patterns)**. |

---

### 📖 Materi Selanjutnya
- [BK-01: Blended Workflows](../../SR-02-Quota-Blending-Strategy/BK-01-Blended-Workflows/README.md)
