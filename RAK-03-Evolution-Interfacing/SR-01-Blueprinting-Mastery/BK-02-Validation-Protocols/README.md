# BK-02: Validation Protocols — Cara Mengecek Pekerjaan AI

## 🌟 Gampangnya...

Setelah AI selesai koding, jangan langsung percaya. **Validation Protocols** adalah daftar cek fisik (*checklist*) untuk memastikan kodingan AI tidak hanya "jalan", tapi juga "benar". Ini seperti QC (Quality Control) di pabrik. Tanpa protokol ini, kamu mungkin akan menemukan bug 2 minggu kemudian saat aplikasi sudah dipakai orang banyak.

---

## 📖 Konteks & Sejarah

AI sering mengalami **"Hallucination of Success"** — dia merasa kodenya sudah benar padahal ada variabel yang tidak ada atau fungsi yang typo. Protokol validasi lahir dari kebutuhan untuk memutus rantai blunder ini dengan mewajibkan *double-check* fungsional sebelum sesi chat ditutup.

---

## ⚙️ Cara Kerja

### The Audit Ritual (Ritual Audit)

1. **Static Analysis**: Baca kode secara visual (pencarian typo/logika aneh).
2. **Terminal Check**: Jalankan kode (run/test) dan lihat hasilnya.
3. **Cross-file Sync**: Cek apakah perubahan di file A merusak koneksi ke file B.

---

## 🗺️ Kapan Mode Ini Relevan

| Mode | Jenis Validasi |
|---|---|
| 📐 **BLUEPRINT** | Validasi Logika (Apakah masuk akal?). |
| ⚡ **EXECUTE** | Validasi Sintaks (Apakah error?). |
| 🔍 **REVIEW** | Validasi Arsitektur (Apakah rapi?). |

---

## 🛠️ Cara Pakai

### Teknik 1: The "Critique Me" Prompt

Setelah AI selesai menulis kode, paksa dia untuk mencari kesalahannya sendiri:
```markdown
"Gus, baca kode yang baru saja kamu tulis. 
 Temukan 3 potensi bug atau kelemahan (security/performance) 
 dari kodingan tersebut. Jangan bilang 'tidak ada'."
```

### Teknik 2: The "Sync Check"

Pastikan file lain tidak "patah":
```markdown
"Cek file @other-file.ts yang menggunakan fungsi ini. 
 Apakah perubahan yang baru saja kita lakukan membuatnya error? 
 Tunjukkan buktinya."
```

---

## 🧪 Lab Praktek

**Skenario: Validasi AI-generated Code**

1. AI baru saja membuat fungsi `calculateTotal`.
2. Gunakan protokol: *"Sekarang, buatkan 3 contoh input (normal, ekstrim/nol, salah tipe) dan simulasikan hasilnya tanpa menjalankan kode."*
3. Jika simulasinya salah, perbaiki kodenya sekarang.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Rubber-Stamping** | Kamu cuma klik "Accept" tanpa membaca | Paksa dirimu membaca minimal 1 menit untuk setiap 100 baris kode AI. |
| **Trusting the 'Pass'** | AI bilang 'Tests passed' tapi kamu gak liat terminalnya | **WAJIB** lihat output terminal dengan mata kepalamu sendiri. |
| **Scope Creep** | AI memvalidasi hal yang tidak berhubungan | Berikan batasan: *"Validasi hanya untuk fungsi X."* |

---

### 📖 Materi Selanjutnya
- [RAK-03/SR-02: Collaborative Workflows](../SR-02-Collaborative-Workflows/README.md)
