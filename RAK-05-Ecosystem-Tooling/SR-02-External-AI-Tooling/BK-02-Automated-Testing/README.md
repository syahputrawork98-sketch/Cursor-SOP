# BK-02: Automated Testing Integrations â€” AI sebagai QA Engineer

## ðŸŒŸ Gampangnya...

Menulis unit test itu membosankan, kan? Tapi sangat penting agar kodemu tidak pecah. **Automated Testing Integrations** adalah cara menggunakan AI untuk menulis, menjalankan, dan memperbaiki test secara otomatis. Bayangkan kamu punya asisten yang tugasnya khusus memastikan tidak ada bug yang lolos sebelum kodemu "naik cetak".

---

## ðŸ“– Konteks & Sejarah

Dalam siklus pengembangan (SDLC), testing seringkali menjadi botol leher (bottleneck). AI sangat kuat dalam memahami logika fungsi dan memetakan semua kemungkinan input (edge cases). Dengan mengintegrasikan AI ke dalam workflow testing, tingkat kepercayaan diri (*confidence score*) pada setiap perubahan kode akan meningkat drastis.

---

## âš™ï¸ Cara Kerja

### Loop: Test -> Fail -> AI Fix -> Pass

1. **Generation**: AI menulis test berdasarkan file logika.
2. **Execution**: Terminal menjalankan test tersebut (`npm test`).
3. **Feedback**: Jika gagal (Fail), pesan error dikirim balik ke AI.
4. **Correction**: AI memperbaiki kode aslinya sampai test-nya Pass.

---

## ðŸ—ºï¸ Kapan Mode Ini Relevan

| Mode | Peran AI | Output |
|---|---|---|
| ðŸ§ª **TEST** | Menulis unit test & integration test. | File `.test.ts` atau `.spec.js`. |
| ðŸ› **DEBUG** | Menganalisis log kegagalan test di terminal. | Fix plan & root cause analysis. |
| ðŸ” **REVIEW** | Memastikan cakupan test (*coverage*) sudah cukup. | Report coverage. |

---

## ðŸ› ï¸ Cara Pakai

### Teknik 1: "Test-Driven Development (TDD) with AI"

Berikan requirement-mu, lalu minta AI tulis test-nya dulu:
```markdown
"Saya ingin buat fungsi kalkulasi diskon. 
 Tuliskan 5 Unit Test (menggunakan Jest) yang mencakup:
 - Diskon standar
 - Diskon 0%
 - Input negatif (error)
 - Diskon di atas 100% (error)
 JANGAN tulis kodingan fungsinya dulu."
```

### Teknik 2: "Fail-to-Fix" Protocol

Saat test gagal di terminal, paste error-nya ke AI:
```markdown
"Test di @src/auth.test.ts gagal dengan error: [PASTE ERROR].
 Baca file logikanya di @src/auth.ts dan perbaiki agar test ini PASS."
```

---

## ðŸ§ª Lab Praktek

**Skenario: Mengejar 100% Test Coverage**

1. Buka file yang sudah jadi (misal: `utils.ts`).
2. Ketik prompt: *"Analisis cakupan test untuk file ini. Tuliskan test case tambahan untuk setiap percabangan (if/else) yang belum ter-cover."*
3. Eksekusi test di terminal. 
4. Hasil: Proyekmu sekarang jauh lebih aman dari "regresi" (bug lama muncul lagi).

---

## âš ï¸ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Brittle Tests** | Test yang dibuat AI terlalu kaku dan sering pecah saat kode berubah sedikit | Fokus pada testing *Behavior* (hasil akhir), bukan *Implementation* (cara koding). |
| **Logic Loop** | AI menulis test yang salah untuk kode yang salah | **SELALU** baca logika test yang dibuat AI. Jangan berasumsi testnya benar hanya karena "hijau". |
| **Slow Test Suite** | AI membuat test yang terlalu berat sehingga terminal jadi lambat | Minta AI meng-optimasi test dengan menggunakan *Mocks* atau *Stubs*. |

---

### ðŸ“– Materi Selanjutnya
- [RAK-05/SR-03: IDE Optimization](../../SR-02-IDE-Fine-Tuning/BK-01-Indexing-Optimization/README.md)

