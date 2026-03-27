# BK-01: Few-Shot in Coding â€” Belajar Lewat Contoh Nyata

## ðŸŒŸ Gampangnya...

AI itu pintar meniru. Kalau kamu cuma bilang *"Bikin tombol"*, dia akan kasih tombol standar. Tapi kalau kamu kasih lihat 3 contoh tombol yang sudah kamu buat sebelumnya, dia akan buat tombol ke-4 dengan gaya yang **persis sama**. **Few-Shot** adalah teknik memberikan "beberapa contoh" (shots) di dalam prompt agar AI paham standar kualitas, gaya koding (*coding style*), dan pola yang kamu inginkan tanpa banyak penjelasan.

---

## ðŸ“– Konteks & Sejarah

LLM bekerja dengan mencocokkan pola. Memberikan 1-3 contoh (*few-shot*) jauh lebih efektif daripada menulis 10 halaman dokumentasi. Ini adalah cara tercepat untuk menangani proyek yang memiliki standar koding sangat spesifik atau library internal yang tidak diketahui oleh AI secara umum.

---

## âš™ï¸ Cara Kerja

### Zero-Shot vs Few-Shot

- **Zero-Shot**: "Buat fungsi login." (AI menebak gayamu).
- **Few-Shot**: "Ini contoh fungsi Register dan ForgotPassword saya: [KODE]. Sekarang buat fungsi Login dengan gaya yang sama." (AI meniru gayamu).

---

## ðŸ—ºï¸ Kapan Mode Ini Relevan

| Task | Kegunaan Few-Shot |
|---|---|
| **Naming Convention** | Memberi contoh cara kamu menamakan variabel. |
| **Unit Testing** | Memberi contoh struktur test yang kamu pakai. |
| **UI Components** | Memberi contoh cara kamu menggunakan Tailwind/CSS-in-JS. |

---

## ðŸ› ï¸ Cara Pakai

### Teknik 1: Pattern Injection (The "Shot" Method)

Kirimkan contoh sebelum instruksi:
```markdown
"Ini adalah pola koding saya untuk services:
 [FILE 1: Auth Service]
 [FILE 2: User Service]
 
 Sekarang buat [FILE 3: Product Service] dengan pola, error handling, 
 dan logging yang persis sama seperti contoh di atas."
```

### Teknik 2: Few-Shot in `.cursorrules`

Gunakan rules untuk menyimpan "Shot" permanen:
```markdown
# STYLE GUIDE FEW-SHOT
Example of Good Variable Name: countItems, isFinished (camelCase).
Example of Bad Variable Name: count_items, finished_flag (snake_case).
Always follow the GOOD example.
```

---

## ðŸ§ª Lab Praktek

**Skenario: Menyeragamkan cara penanganan Error Response**

Kamu mau semua API kamu mengembalikan format JSON yang sama.

**Cara Few-Shot:**
1. Berikan satu file controller yang sudah jadi.
2. Ketik: *"Baca @controller-lama.ts. Lihat bagaimana saya me-return error. Sekarang buat @controller-baru.ts dengan standar error response yang identik."*
3. **Hasil**: AI akan menggunakan `res.status(400).json({ status: 'fail', message: '...' })` sesuai contoh, bukan format aslinya sendiri.

---

## âš ï¸ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Bad Example** | Kamu kasih contoh kode yang berantakan, AI jadi ikut berantakan | **PASTIKAN** contoh yang kamu berikan adalah "Gold Standard" kamu. |
| **Over-Cluttering** | Kamu kasih 10 contoh sekaligus, AI jadi bingung | Cukup berikan **1-3 contoh terbaik**. Lebih dari itu hanya membuang token. |
| **Stale Example** | Kamu kasih contoh dari versi library lama | Selalu update "Shot" kamu jika ada update library. |

---

### ðŸ“– Materi Selanjutnya
- [BK-02: Constraint-Based Prompting](../BK-02-Constraint-Based-Prompting/README.md)

