# BK-01: Post-Execute Audit Ritual — Ritual Wajib Pasca-Koding

## 🌟 Gampangnya...

Banyak developer (dan AI) merasa tugas selesai begitu kode "tidak error". Padahal, di sanalah bahaya bermula. **Post-Execute Audit Ritual** adalah serangkaian langkah wajib yang harus kamu lakukan SETELAH kode selesai ditulis, tapi SEBELUM kamu menutup sesi chat. Tujuannya adalah memastikan kodingan baru tidak merusak file lain dan tetap mengikuti gaya koding (coding style) proyekmu.

---

## 📖 Konteks & Sejarah

Error yang ditemukan di masa depan (post-production) biayanya 10x lebih mahal daripada yang ditemukan sekarang. Dengan melakukan audit 5 menit setelah eksekusi, kamu bisa menangkap 90% kesalahan kecil (typo, unused variable, inconsistent spacing) yang sering dilewatkan AI dalam mode buru-buru.

---

## ⚙️ Cara Kerja

### The 3-Step Ritual

1. **Integrity Check**: Apakah file lain yang meng-import file ini masih jalan?
2. **Standard Check**: Apakah nama variabel dan struktur file sudah sesuai `.cursorrules`?
3. **Ghost Check**: Apakah ada kode sampah (*commented-out code*) yang lupa dihapus AI?

---

## 🗺️ Kapan Mode Ini Relevan

| Mode | Ritual Audit |
|---|---|
| ⚡ **EXECUTE** | **WAJIB** segera setelah AI berhenti mengetik. |
| ♻️ **REFACTOR** | Audit untuk memastikan fungsionalitas lama tidak hilang. |
| 🧪 **TEST** | Audit untuk memastikan test case benar-benar valid. |

---

## 🛠️ Cara Pakai

### Mantra: The Final Cleanup

Setiap kali AI bilang "Selesai", balas dengan ini:
```markdown
"Bagus. Sekarang lakukan RITUAL AUDIT terakhir:
 1. Hapus semua komentar sampah atau kode yang sudah tidak dipakai.
 2. Pastikan penamaan variabel 100% konsisten dengan @[Nama File Standar].
 3. Cek kembali apakah ada file lain yang 'patah' akibat perubahan ini.
 4. Berikan konfirmasi status: AMAN/BUTUH PERBAIKAN."
```

### Automation dalam .cursorrules

Tanamkan di global rules:
```markdown
# POST-EXECUTION POLICY
After every EXECUTE task, you MUST offer to perform a cleanup and integrity check.
```

---

## 🧪 Lab Praktek

**Skenario: AI meninggalkan "sampah" logika**

1. AI baru saja refactoring fungsi besar.
2. AI bilang: "Selesai, saya sudah optimasi kodenya."
3. Jalankan ritual: *"Audit kembali. Apakah ada variabel global yang sekarang jadi yatim piatu (tidak dipanggil siapapun) karena perubahan tadi?"*
4. AI akan menemukan sisa-sisa kodingan lama yang harus dihapus.
5. **Hasil**: Codebase tetap ringan dan bersih.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **"Nanti Saja" Syndrome** | Kamu menunda audit sampai akhir sprint | **JANGAN.** Auditlah setiap kali satu fitur/task kecil selesai. |
| **Trusting the UI** | Di Cursor terlihat hijau (no errors), tapi logikanya salah | Jalankan aplikasi secara manual atau minta AI melakukan **Trace Logic Audit**. |
| **Audit Fatigue** | Kamu malas baca checklist audit | Suruh AI yang melakukan auditnya, kamu cukup membaca **Ringkasan Temuan**-nya. |

---

### 📖 Materi Selanjutnya
- [RAK-08: Matrix Intersection (Cross-Project Sync)](../../../RAK-08-Matrix-Intersection/README.md)
