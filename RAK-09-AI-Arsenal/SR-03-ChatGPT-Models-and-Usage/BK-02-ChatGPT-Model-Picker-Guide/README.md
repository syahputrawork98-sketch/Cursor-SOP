# BK-02: ChatGPT Model Picker Guide

## Gampangnya...

Tidak ada satu model ChatGPT yang terbaik untuk semua hal. Model yang cepat belum tentu paling aman untuk keputusan mahal, dan model yang paling dalam belum tentu efisien untuk tugas ringan.

Dokumen ini membantu menjawab pertanyaan praktis: **kalau saya sedang ada di ChatGPT, model mana yang sebaiknya saya pilih untuk task ini?**

> Status per 2026-03-28.
> Mengacu pada artikel resmi OpenAI tentang GPT-5.3 dan GPT-5.4 di ChatGPT.

---

## Konteks & Sejarah

OpenAI secara berkala merapikan lineup model di ChatGPT. Per 2026, model lama seperti GPT-4o, GPT-4.1, GPT-4.1 mini, o4-mini, serta GPT-5 Instant/Thinking generasi sebelumnya telah dipensiunkan dari ChatGPT. Sebagai gantinya, user diarahkan ke keluarga GPT-5.3 dan GPT-5.4 di pengalaman ChatGPT yang lebih terpadu.

Implikasinya sederhana:
- jangan terlalu mengandalkan hafalan lineup lama,
- selalu cek status tanggal dokumen,
- pakai prinsip memilih model berdasarkan jenis tugas, bukan nostalgia nama lama.

---

## Cara Kerja

### Model yang Relevan di ChatGPT

| Opsi | Karakter Umum | Cocok Untuk |
|---|---|---|
| **Auto** | Sistem otomatis yang dapat merutekan antara Instant dan Thinking | User yang ingin cepat tanpa mikir banyak |
| **GPT-5.3 Instant** | Cepat, ringan, adaptif untuk penggunaan harian | Tanya cepat, drafting, iterasi ringan |
| **GPT-5.4 Thinking** | Lebih dalam dan lebih sabar menganalisis | Debug sulit, analisis kompleks, coding berat |
| **GPT-5.4 Pro** | Varian premium untuk kerja yang paling penting | Keputusan mahal, audit final, work session kritis |

### Cara Membaca Tabel Ini

- `cepat` berarti cocok untuk iterasi dan volume,
- `dalam` berarti cocok untuk reasoning dan pengecekan bertahap,
- `premium` berarti simpan untuk pekerjaan yang salahnya mahal.

---

## Kapan Digunakan

### Auto

Gunakan ketika:
- kamu ingin pengalaman default yang simpel,
- kamu tidak ingin mikir routing model secara manual,
- task-mu campuran dan berubah-ubah.

Catatan penting:
- `Auto` dapat memilih antara GPT-5.3 Instant dan GPT-5.4 Thinking.
- Jika Auto merutekan task ke Thinking, ChatGPT tidak selalu menampilkan thinking log saat reasoning-nya pendek.

Kelebihan:
- paling mudah,
- cocok untuk user yang tidak mau overthinking picker.

Kekurangan:
- kontrolmu lebih sedikit,
- kurang ideal kalau kamu sengaja mau menghemat jatah model tertentu.

### GPT-5.3 Instant

Gunakan ketika:
- kamu butuh respons cepat,
- task jelas dan tidak terlalu mahal kalau salah,
- kamu sedang brainstorming, rewrite, atau drafting.

Kelebihan:
- cepat,
- nyaman untuk iterasi banyak,
- cocok sebagai langkah pertama.

Kekurangan:
- tidak selalu ideal untuk analisis panjang dan sulit,
- bisa kalah hati-hati dibanding mode thinking untuk problem berlapis.

### GPT-5.4 Thinking

Gunakan ketika:
- kamu sedang debug susah,
- kamu butuh penalaran bertahap,
- kamu sedang membandingkan beberapa opsi teknis,
- kamu ingin model lebih berhati-hati sebelum menyimpulkan.

Kelebihan:
- lebih kuat untuk task kompleks,
- lebih cocok untuk coding, science-style analysis, dan synthesis.

Kekurangan:
- lebih lambat,
- kurang efisien untuk tugas receh.

### GPT-5.4 Pro

Gunakan ketika:
- task sangat penting,
- kamu ingin quality bar tertinggi,
- kamu sedang review final sebelum keputusan besar.

Kelebihan:
- cocok untuk pekerjaan kritis,
- memberi rasa aman lebih tinggi untuk audit dan final check.

Kekurangan:
- jangan dibuang untuk tugas sederhana,
- availability dan limit bergantung pada plan,
- beberapa tool ChatGPT tidak tersedia pada Pro.

---

## Cara Pakai

### Rumus Cepat Memilih Model

1. Jika tugasmu ringan dan jelas, mulai dari **GPT-5.3 Instant**.
2. Jika tugasmu ambigu, teknis, atau salahnya mahal, pindah ke **GPT-5.4 Thinking**.
3. Jika sesi itu benar-benar penting, gunakan **GPT-5.4 Pro** untuk pengecekan terakhir.
4. Jika kamu malas memilih manual, gunakan **Auto**.

### Catatan Availability Ringkas

- Semua user ChatGPT yang login mendapat akses ke GPT-5.3.
- Plus, Go, Pro, dan Business punya pola akses yang berbeda untuk model picker dan thinking.
- GPT-5.4 Pro hanya tersedia untuk plan tertentu, jadi jangan menulis asumsi bahwa semua user melihat opsi ini.

### Tabel Pilihan Praktis

| Jenis Task | Rekomendasi Awal |
|---|---|
| Rewrite teks | GPT-5.3 Instant |
| Brainstorming cepat | GPT-5.3 Instant |
| Coding ringan | GPT-5.3 Instant |
| Debug sulit | GPT-5.4 Thinking |
| Review arsitektur | GPT-5.4 Thinking |
| Final audit penting | GPT-5.4 Pro |

---

## Lab Praktek

**Skenario: satu hari kerja campuran**

Pagi:
- gunakan GPT-5.4 Thinking untuk blueprint dan analisis inti.

Siang:
- gunakan GPT-5.3 Instant untuk rewrite, drafting, dan iterasi cepat.

Sore:
- gunakan GPT-5.4 Pro untuk review keputusan final yang paling penting.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Overkill** | Pakai model berat untuk tugas receh | Mulai dari Instant dulu |
| **Underkill** | Pakai model cepat untuk problem berlapis | Pindah ke Thinking saat task mulai ambigu |
| **Picker anxiety** | Terlalu lama memilih model | Pakai Auto atau aturan 4 langkah di atas |
| **Model nostalgia** | Masih pakai peta lineup lama | Selalu cek status tanggal dokumen |

---

## Referensi Resmi

- https://help.openai.com/en/articles/11909943-gpt-53-and-gpt-54-in-chatgpt/
- https://help.openai.com/en/articles/20001051

---

## Materi Selanjutnya

- [BK-03: Thinking Selector Guide](../BK-03-Thinking-Selector-Guide/README.md)
