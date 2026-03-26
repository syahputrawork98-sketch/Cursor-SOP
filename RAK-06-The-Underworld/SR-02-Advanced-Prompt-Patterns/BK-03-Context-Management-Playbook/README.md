# BK-01: Session Refresh Protocol — Kapan Harus "Mulai dari Nol"?

## 🌟 Gampangnya...

Bayangkan kamu sedang mengobrol dengan seseorang selama 5 jam nonstop. Di jam ke-4, pasti obrolan mulai melantur dan dia mulai bingung siapa yang sedang dibicarakan. Hal yang sama terjadi pada AI. **Session Refresh Protocol** adalah panduan untuk mengetahui kapan kamu harus menutup chat yang lama dan membuka chat baru agar AI kembali segar (fresh) dan tidak membawa "beban" memori dari diskusi yang sudah lewat.

---

## 📖 Konteks & Sejarah

Banyak blunder AI (seperti tiba-tiba menghapus file yang benar) terjadi bukan karena AI bodoh, tapi karena **Context Pollution** (Pencemaran Konteks). Sesi chat yang terlalu panjang berisi terlalu banyak kodingan lama yang mungkin sekarang sudah tidak relevan. AI mulai bingung mana versi kode yang benar.

---

## ⚙️ Cara Kerja

### Siklus Hidup Konteks (Context Lifecycle)

1. **Morning (Fresh)**: AI sangat tajam, mengikuti rules 100%. (Turn 1-15)
2. **Afternoon (Tired)**: AI mulai abai pada detail kecil. (Turn 16-30)
3. **Evening (Dementia)**: AI mulai berhalusinasi dan gagal membedakan instruksi. (Turn 31+)

---

## 🗺️ Kapan Mode Ini Relevan

| Kondisi | Keputusan | Tindakan |
|---|---|---|
| Ganti Fitur Besar | **Refresh!** | Save notes, tutup chat, buka baru. |
| AI Mulai Melawan Rules | **Refresh!** | Ingatkan sekali, jika gagal → Buka baru. |
| Fix Bug Kecil Lanjut ke Fitur Baru | **Refresh!** | Jangan campur bug-fixing dengan feature building. |

---

## 🛠️ Cara Pakai

### Protokol "Handover" (Sebelum Ganti Sesi)

Jangan langsung tutup chat! Lakukan **Handover** agar konteks tidak hilang:

```markdown
# Ketik di chat lama:
"Sesi ini sudah terlalu panjang. Buat ringkasan 'Handover' 
 dalam 5 poin untuk saya bawa ke sesi chat baru:
 1. Status terakhir fitur [X].
 2. Keputusan teknis yang kita ambil.
 3. Masalah yang belum selesai.
 4. File utama yang sedang kita kerjakan."
```

### Memulai Sesi Baru dengan "Clean Context"

1. Tekan `Ctrl/Cmd + L` (Chat baru) atau `Ctrl/Cmd + K` (Inline baru).
2. Paste ringkasan handover tadi.
3. Tambahkan: *"Gunakan @session-notes.md dan ringkasan di atas sebagai baseline. Mari kita lanjut."*

---

## 🧪 Lab Praktek

**Skenario: Kamu sudah debug fitur X selama 1 jam, sekarang mau pindah ke fitur Y.**

**SALAH**: Lanjut bertanya di chat yang sama. AI akan membawa bug-bug fitur X ke fitur Y.
**BENAR**:
1. Minta ringkasan fitur X.
2. Simpan di `docs/DONE-X.md`.
3. Buka CHAT BARU.
4. Katakan: *"Lupakan fitur X. Sekarang kita kerjakan Fitur Y. Status proyek saat ini: [...]"*

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Malas Ganti Sesi** | AI terus-terusan mengulangi kesalahan yang sama | Ikuti aturan: **30 Turns = Refresh**. Jangan dinegosiasi. |
| **Kehilangan History** | Kamu lupa apa yang dilakukan di chat sebelumnya | Gunakan file fisik seperti `CHANGELOG.md` untuk mencatat progres manual. |
| **Konteks Terputus** | AI di chat baru tidak tahu variabel di chat lama | Selalu gunakan `@mention` file yang relevan di chat baru. |

---

### 📖 Materi Selanjutnya
- [Fase Selanjutnya: Foundational Depth (RAK-01 s/d 04)](../../status.md)
