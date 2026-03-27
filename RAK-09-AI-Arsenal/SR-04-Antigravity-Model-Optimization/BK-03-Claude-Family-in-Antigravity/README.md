# BK-03: Claude Family in Antigravity

## Gampangnya...

Keluarga Claude sering terasa "mahal tapi nyaman". Banyak user menyukainya untuk review, reasoning yang rapi, dan penulisan yang enak dibaca. Masalahnya, kenyamanan itu bisa berubah jadi pemborosan kalau semua task dinaikkan ke model Claude premium.

---

## Konteks & Sejarah

Dalam workflow nyata, Claude sering menonjol di area:
- review,
- penulisan teknis,
- penjelasan bernuansa,
- audit yang butuh reasoning lebih rapih.

Tapi tanpa disiplin routing, user bisa terlalu cepat naik ke model tertinggi hanya karena hasilnya terasa halus.

---

## Cara Kerja

### Peta Keluarga Claude

| Model | Kesan Umum | Cocok Untuk |
|---|---|---|
| **Claude Sonnet 4.6 Thinking** | premium hemat yang rapi | review, writing, analysis menengah-berat |
| **Claude Opus 4.6 Thinking** | premium lebih berat | audit final, synthesis besar, keputusan mahal |

### Prinsip Membacanya

- `Sonnet` sering cukup untuk banyak task yang butuh kualitas,
- `Opus` layak dipakai saat salah sedikit terasa mahal atau saat synthesis-nya sangat berat.

---

## Kapan Digunakan

### Pakai Sonnet jika:
- kamu butuh review yang rapi,
- kamu sedang menulis atau merapikan dokumentasi,
- kamu ingin reasoning yang kuat tanpa langsung naik ke mode paling mahal.

### Pakai Opus jika:
- kamu sedang audit final,
- kamu butuh penilaian sangat hati-hati,
- kamu sedang membandingkan keputusan besar yang tidak murah kalau meleset.

---

## Cara Pakai

### Aturan Praktis

- mulai dari Sonnet untuk review dan writing yang serius,
- naik ke Opus hanya jika task benar-benar menuntut kualitas tertinggi,
- jangan jadikan Opus sebagai default harian.

### Template Prompt

```text
"Saya ingin mengerjakan [task review / writing / analysis].
Sebelum mulai, jelaskan apakah Sonnet sudah cukup,
atau mengapa task ini benar-benar layak dinaikkan ke Opus."
```

---

## Lab Praktek

**Skenario: Audit hasil kerja**

Gunakan `Claude Sonnet 4.6 Thinking` untuk review menengah dan cross-check implementasi.

Naik ke `Claude Opus 4.6 Thinking` hanya jika:
- keputusan final sangat penting,
- dokumen atau review-nya benar-benar berat,
- atau kamu butuh second opinion premium yang lebih hati-hati.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Sonnet dianggap tanggung** | Semua task dinaikkan ke Opus | Beri Sonnet ruang sebagai default premium yang hemat |
| **Opus dipakai karena prestige** | Kuota cepat menipis | Simpan Opus untuk audit dan keputusan mahal |
| **Claude dipakai untuk semua hal** | Routing model kehilangan disiplin | Kembalikan keputusan ke task triage |

---

## Materi Selanjutnya

- [BK-04: GPT-OSS and Economy Models](../BK-04-GPT-OSS-and-Economy-Models/README.md)
