# BK-02: Chain-of-Thought (CoT) â€” Memaksa AI Berpikir Sebelum Menulis

## ðŸŒŸ Gampangnya...

Pernahkah kamu merasa AI menjawab terlalu cepat dan hasilnya "setengah matang"? Itu karena AI langsung menebak kata berikutnya tanpa melalui proses perenungan. **Chain-of-Thought (CoT)** adalah teknik memaksa AI untuk "menulis coret-coretan" di kertas buram (menuliskan alur pikirannya) sebelum dia memberikan jawaban akhir. Ini adalah cara paling ampuh untuk meningkatkan kecerdasan AI dalam tugas logika yang sulit.

---

## ðŸ“– Konteks & Sejarah

Dalam riset AI, ditemukan bahwa jika kita menyuruh AI *"Think step by step"*, akurasi jawabannya meningkat drastis. Ini karena AI menggunakan token responsnya untuk memproses logika secara serial. Tanpa CoT, AI seperti orang yang menjawab kuis secara spontan; dengan CoT, AI seperti orang yang mengerjakan soal matematika di papan tulis.

---

## âš™ï¸ Cara Kerja

### Perbedaan Tanpa vs Dengan CoT

**Tanpa CoT**: Input â†’ Output (Seringkali dangkal)
**Dengan CoT**: Input â†’ **Langkah 1 â†’ Langkah 2 â†’ Langkah 3** â†’ Output (Deep Reasoning)

Dengan menulis setiap langkah, AI bisa mengevaluasi "langkah sebelumnya" untuk memastikan langkah berikutnya benar. Jika ada kesalahan di Langkah 1, dia bisa mengoreksinya di Langkah 2 sebelum sampai ke Output akhir.

---

## ðŸ—ºï¸ Kapan Mode Ini Relevan

| Task | Mode | Urgensi CoT |
|---|---|---|
| **Debugging** | ðŸ› **DEBUG** | **VVIP** (Wajib trace alur error). |
| **Arsitektur** | ðŸ“ **BLUEPRINT** | **Tinggi** (Cek trade-off desain). |
| **Refactoring** | â™»ï¸ **REFACTOR** | **Tinggi** (Cek dependensi yang terpengaruh). |

---

## ðŸ› ï¸ Cara Pakai

### Teknik 1: The Step-by-Step Trigger

Gunakan kalimat sakti ini di setiap prompt yang membutuhkan logika:
```markdown
"Selesaikan task ini dengan Chain-of-Thought: 
 1. Identifikasi masalah utama.
 2. Analisis file yang berhubungan.
 3. Tuliskan 3 alternatif solusi beserta plus/minus-nya.
 4. Pilih satu solusi dan jelaskan MENGAPA itu yang terbaik.
 JANGAN berikan kode sebelum langkah 1-4 selesai."
```

### Teknik 2: The Logic Guard (Dalam .cursorrules)

Tanamkan aturan ini agar CoT menjadi otomatis:
```markdown
# CoT ENFORCEMENT
"For any complexity > 3, you MUST outline your thought process 
 using bullet points before suggesting any code changes."
```

### Teknik 3: Show Your Evidence (Papan Bukti)

Paksa AI untuk memberikan referensi baris kode:
```markdown
"Gunakan CoT untuk menganalisis error ini. 
 Sebutkan nomor baris di file @[nama-file] yang menjadi penyebabnya."
```

---

## ðŸ§ª Lab Praktek

**Skenario: Bug yang sulit ditemukan**

Kamu punya error *"Undefined is not a function"*, AI biasanya langsung memberi tebakan.

**Cara CoT:**
1. Prompt: *"Gunakan CoT untuk debug error ini. Tunjukkan alur data dari login sampai logout."*
2. AI akan menulis: "Langkah 1: User klik login... Langkah 2: Token disimpan... Langkah 3: Logout dipanggil tapi token tidak dihapus... Masalah ketemu!"
3. **Hasil**: Kamu bukan cuma dapat solusi, tapi paham **kenapa** error itu terjadi.

---

## âš ï¸ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **CoT Overkill** | Kamu cuma mau tanya "Apa itu HTML?" tapi AI jawab 10 langkah | Gunakan CoT hanya untuk tugas **Logika/Koding**. Jangan untuk pertanyaan pengetahuan umum. |
| **Langkah Terlalu Banyak** | AI lupa tujuan awal karena langkah terlalu detail | Batasi CoT maksimal 3-5 langkah utama. |
| **CoT Tanpa Evidence** | AI buat alur pikir tapi tidak nyambung ke kode asli | Tambahkan syarat: *"Always reference specific line numbers in your CoT."* |

---

### ðŸ“– Materi Selanjutnya
- [RAK-06/SR-02: Context Management](../../SR-02-Advanced-Prompt-Patterns/BK-03-Context-Management-Playbook/README.md)

