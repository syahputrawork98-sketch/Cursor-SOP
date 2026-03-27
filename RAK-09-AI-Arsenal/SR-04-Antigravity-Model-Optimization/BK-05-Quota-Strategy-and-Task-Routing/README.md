# BK-05: Quota Strategy and Task Routing

## Gampangnya...

Ini adalah jantung sub-rak ini. Tujuannya sederhana: **jangan pakai model premium untuk semua hal**. Simpan tenaga mahal untuk pekerjaan mahal, dan dorong pekerjaan volume ke model yang lebih hemat.

Kalau routing modelmu disiplin, kualitas kerja bisa tetap tinggi tanpa membuat kuota premium cepat jebol.

> Status per 2026-03-28.

---

## Konteks & Sejarah

Mentok kuota biasanya bukan karena model premium "kurang banyak", tetapi karena user tidak punya sistem routing. Semua task terasa penting, semua task terasa ingin dinaikkan, dan akhirnya premium dipakai untuk pekerjaan yang sebenarnya bisa dikerjakan model lain.

Quota Strategy lahir untuk mengubah pemakaian model dari kebiasaan impulsif menjadi keputusan sadar.

---

## Cara Kerja

### Task Triage

| Kelas Task | Contoh | Routing Awal |
|---|---|---|
| **Ringan** | rewrite, draft awal, boilerplate | economy / cepat |
| **Menengah** | coding biasa, review ringan, planning | model menengah / premium hemat |
| **Mahal** | debug berat, audit final, keputusan arsitektur | premium reasoning |

### Aturan Routing

1. Tugas ringan turun ke model hemat atau cepat.
2. Tugas menengah naik ke model yang stabil tapi tidak harus paling mahal.
3. Tugas mahal baru dinaikkan ke model paling kuat.

### Prinsip Emas

- jangan mulai semua task di premium,
- jangan takut turun model setelah fase berat selesai,
- selalu sisakan kuota untuk debug dan audit yang benar-benar penting.

---

## Kapan Digunakan

Gunakan buku ini ketika:
- kuota mulai terasa cepat habis,
- kamu tidak tahu task mana yang layak naik model,
- kamu ingin punya ritme kerja harian dan mingguan yang lebih sehat.

---

## Cara Pakai

### Strategi Harian

Pagi:
- pakai model kuat untuk blueprint, analisis inti, atau debug berat.

Siang:
- turunkan ke model hemat untuk drafting, rewrite, atau eksekusi volume.

Sore:
- naikkan lagi jika ada audit final atau keputusan penting.

### Strategi Mingguan

- awal minggu: kerjakan task mahal lebih dulu,
- tengah minggu: dorong volume ke model hemat,
- akhir minggu: sisakan cadangan untuk review dan bug mendadak.

### Anti-Boros Pattern

- jangan lakukan rewrite kecil di model paling mahal,
- jangan buka banyak thread premium untuk satu task ringan,
- jangan tahan model hemat hanya karena merasa "kurang bergengsi".

### Template Prompt

```text
"Sebelum mulai, klasifikasikan task ini:
ringan, menengah, atau mahal jika salah.
Lalu rekomendasikan model yang paling efisien,
bukan model yang paling prestisius."
```

---

## Lab Praktek

**Skenario: Sehari kerja campuran**

1. `Gemini 3.1 Pro` atau `Claude Sonnet 4.6 Thinking` untuk analisis utama.
2. `Gemini Flash` atau `GPT-OSS 120B Medium` untuk drafting dan iterasi.
3. `Gemini 3.1 Pro High` atau `Claude Opus 4.6 Thinking` hanya untuk audit yang memang mahal jika salah.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Semua task terasa mahal** | Routing selalu naik ke premium | Pakai triage ringan-menengah-mahal |
| **Tidak turun level** | Setelah fase berat selesai, model tetap premium | Turunkan model saat kerja berubah jadi volume |
| **Panic routing** | Kuota menipis lalu semua task jadi kacau | Buat ritme harian dan sisakan cadangan |

---

## Materi Selanjutnya

- [BK-06: Playbook Pemilihan Model per Jenis Kerja](../BK-06-Playbook-Pemilihan-Model-per-Jenis-Kerja/README.md)
