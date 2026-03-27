# BK-01: Antigravity Model Landscape

## Gampangnya...

Antigravity memberi kamu banyak mesin sekaligus. Masalahnya, tanpa peta mental yang jelas, semua nama model itu cuma terasa seperti daftar menu mahal yang membingungkan.

Buku ini adalah peta dasarnya: model apa saja yang tersedia, mereka masuk keluarga apa, dan kira-kira peran umumnya di workflow kerja.

> Status per 2026-03-28.
> Disusun berdasarkan lineup yang tersedia di akun premium yang sedang kamu gunakan.

---

## Konteks & Sejarah

Saat platform AI hanya menyediakan satu atau dua model, user masih bisa memilih berdasarkan insting. Tapi ketika satu workspace menyediakan banyak model sekaligus, insting saja tidak cukup. User butuh peta:
- mana model cepat,
- mana model reasoning,
- mana model premium,
- mana model hemat,
- mana yang cocok untuk audit, planning, drafting, atau execution.

Tanpa peta ini, pemilihan model berubah menjadi tebak-tebakan mahal.

---

## Cara Kerja

### Daftar Model yang Dibahas

| Model | Keluarga | Posisi Umum |
|---|---|---|
| **Gemini Flash** | Gemini | cepat, ringan, cocok untuk volume |
| **Gemini 3.1 Pro** | Gemini | reasoning inti serbaguna |
| **Gemini 3.1 Pro High** | Gemini | reasoning lebih berat untuk task mahal |
| **Gemini 3.1 Pro Low** | Gemini | kompromi antara kualitas dan efisiensi |
| **Claude Sonnet 4.6 Thinking** | Claude | review, writing, analysis yang hemat premium |
| **Claude Opus 4.6 Thinking** | Claude | audit dan reasoning premium yang lebih berat |
| **GPT-OSS 120B Medium** | Economy | draft, transformasi, dan task hemat |

### Cara Membaca Peta Ini

- `cepat` bukan berarti dangkal, tapi berarti cocok untuk iterasi lebih banyak,
- `premium` bukan berarti wajib dipakai, tapi berarti simpan untuk task yang nilainya tinggi,
- `economy` bukan berarti buruk, tapi berarti cocok untuk pekerjaan yang tidak mahal kalau salah.

---

## Kapan Digunakan

Buku ini dipakai ketika:
- kamu baru membuka Antigravity dan ingin memahami lineup-nya,
- kamu belum tahu model mana milik keluarga Gemini, Claude, atau GPT-OSS,
- kamu ingin membedakan model premium dan model hemat sebelum masuk ke strategi routing.

Jangan berhenti di buku ini kalau kamu butuh keputusan kerja harian. Setelah peta mental terbentuk, lanjut ke strategi kuota dan keluarga model.

---

## Cara Pakai

### Checklist Orientasi

1. Model mana yang termasuk keluarga Gemini?
2. Model mana yang termasuk keluarga Claude?
3. Model mana yang aman dipakai untuk task hemat?
4. Model mana yang sebaiknya disimpan untuk task yang mahal jika salah?

### Aturan Praktis

- gunakan buku ini untuk orientasi,
- gunakan buku keluarga model untuk pemahaman lebih dalam,
- gunakan buku strategi kuota untuk keputusan real di lapangan.

---

## Lab Praktek

**Skenario: User melihat banyak model sekaligus**

Kalau kamu melihat `Gemini Flash`, `Gemini 3.1 Pro High`, `Claude Opus 4.6 Thinking`, dan `GPT-OSS 120B Medium` dalam satu daftar, jangan langsung tanya "mana yang paling bagus?"

Tanya dulu:
- mana yang cepat?
- mana yang mahal?
- mana yang hemat?
- mana yang cocok untuk task saya hari ini?

Itulah fungsi buku ini.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Semua model terasa sama** | User hanya melihat nama, bukan peran | Gunakan pengelompokan keluarga model |
| **Nama premium bikin silau** | Semua task ingin dinaikkan ke model teratas | Ingat bahwa premium bukan default |
| **Model hemat diremehkan** | GPT-OSS tidak pernah dipakai | Perlakukan economy model sebagai alat volume |

---

## Materi Selanjutnya

- [BK-05: Quota Strategy and Task Routing](../BK-05-Quota-Strategy-and-Task-Routing/README.md)
