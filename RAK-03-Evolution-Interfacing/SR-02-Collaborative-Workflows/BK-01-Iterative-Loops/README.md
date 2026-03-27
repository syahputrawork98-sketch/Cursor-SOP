# BK-01: Iterative Loops â€” Rahasia Koding Cepat Tanpa Error

## ðŸŒŸ Gampangnya...

Jangan pernah mencoba membangun gedung 10 lantai dalam satu kali perintah. **Iterative Loops** adalah teknik membangun kodingan secara bertahap: Lantai 1 dulu, cek, baru lantai 2. Dengan cara ini, jika ada kesalahan di lantai 1, kamu bisa memperbaikinya segera sebelum kesalahan itu terkubur di bawah 9 lantai lainnya. Ini adalah workflow paling efisien untuk bekerja dengan AI Agent.

---

## ðŸ“– Konteks & Sejarah

Kesalahan terbesar developer pemula saat memakai AI adalah memberikan instruksi yang terlalu raksasa (*One-Shot Mega-Prompt*). AI akan kelelahan, token habis, dan akurasi turun drastis. Teknik iteratif (perulangan kecil) merubah pengerjaan fitur besar menjadi serangkaian kemenangan kecil yang terjamin kualitasnya.

---

## âš™ï¸ Cara Kerja

### Siklus "Plan-Act-Review"

1. **Slicing**: Pecah tugas besar (misal: "Bikin E-commerce") menjadi tugas kecil ("Bikin tombol Add-to-cart").
2. **Iteration**: Selesaikan tugas kecil tersebut.
3. **Review**: Pastikan tugas kecil itu sudah sempurna.
4. **Repeat**: Ulangi untuk bagian selanjutnya.

---

## ðŸ—ºï¸ Kapan Mode Ini Relevan

| Ukuran Task | Pendekatan | Risiko Kegagalan |
|---|---|---|
| **Kecil** (< 20 baris) | Direct Action | Rendah. |
| **Menengah** (1-2 file) | **Iterative (2 loops)** | Sedang. |
| **Besar** (Multi-file) | **Iterative (5+ loops)** | Sangat Tinggi (Wajib Iteratif). |

---

## ðŸ› ï¸ Cara Pakai

### Teknik "Micro-Commit" Interaction

Gunakan pola ini saat membangun fitur moderat:
```markdown
# Loop 1:
"Buat skeleton (kerangka) fungsinya dulu di @file.ts. Jangan isi logikanya."
# Setelah OK...
# Loop 2:
"Sekarang isi logika kalkulasinya berdasarkan skeleton tadi."
# Setelah OK...
# Loop 3:
"Sekarang tambahkan error handling dan logging."
```

---

## ðŸ§ª Lab Praktek

**Skenario: Membangun Form Registrasi yang Kompleks**

1. **Loop 1**: Minta AI buat UI HTML-nya saja. (Review: layout sudah rapi?).
2. **Loop 2**: Minta AI buat fungsi Validasi-nya. (Review: email sudah dicek?).
3. **Loop 3**: Minta AI buat fungsi Push-to-Database-nya. (Review: data masuk?).
4. **Hasil**: Kamu punya form yang sempurna karena setiap bagian di-audit secara terpisah.

---

## âš ï¸ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Too Small Loops** | Kamu terlalu sering interupsi AI untuk hal remeh | Gabungkan tugas-tugas kecil yang satu domain (misal: "Satu folder UI sekaligus"). |
| **Forgetting History** | Di loop ke-3 AI lupa apa yang dilakukan di loop ke-1 | Selalu @mention file pondasi yang dibuat di loop sebelumnya. |
| **Final Integration Failure** | Bagian-bagian kecil sudah OK tapi tidak nyambung | Sisakan loop terakhir khusus untuk **Integration Check**. |

---

### ðŸ“– Materi Selanjutnya
- [RAK-04: Core Mechanics & Internals](../../../RAK-04-Core-Mechanics-Internals/README.md)

