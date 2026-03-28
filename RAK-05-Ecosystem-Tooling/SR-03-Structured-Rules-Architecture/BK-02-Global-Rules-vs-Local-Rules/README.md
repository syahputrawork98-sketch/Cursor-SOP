# BK-02: Global Rules vs Local Rules

## Gampangnya...

Tidak semua aturan layak hidup di semua proyek. Ada aturan yang memang universal, dan ada aturan yang hanya cocok untuk repo tertentu.

---

## Konteks & Sejarah

Masalah umum dalam ekosistem multi-proyek adalah ini:
- aturan terlalu global, jadi tidak cocok di proyek tertentu,
- atau terlalu lokal, jadi standar lintas proyek hilang.

Karena itu, pemisahan global vs local rules adalah tulang punggung rules architecture.

---

## Cara Kerja

| Jenis | Cocok Untuk |
|---|---|
| **Global Rules** | discuss-first, anti-offside, quality discipline, handoff minimum |
| **Local Rules** | stack notes, folder convention, domain boundary, deploy boundary |

### Rule of Thumb

- jika aturan berlaku hampir di semua proyekmu, taruh di global
- jika aturan hanya relevan untuk satu repo atau satu workspace, taruh di local

---

## Kapan Digunakan

Gunakan buku ini saat:
- menulis template pusat,
- mengaudit kenapa rules lintas repo mulai bertabrakan,
- ingin membuat override tanpa merusak standar utama.

---

## Cara Pakai

### Contoh Global

- default mode adalah `DISCUSS`
- jangan eksekusi tanpa trigger yang jelas
- gunakan artifact map bila artefak mulai banyak

### Contoh Local

- frontend pakai responsive-first review
- backend wajib audit validation dan error handling
- workspace gabungan wajib sinkronkan contract FE-BE

### Formula

`global = perilaku inti`

`local = konteks proyek`

---

## Lab Praktek

**Skenario: repo backend butuh aturan auth khusus**

Aturan auth itu tidak perlu dipaksakan ke semua proyek. Simpan di local rules backend, sementara anti-offside tetap di global rules.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Semua dijadikan global** | rules terlalu berat | pindahkan konteks proyek ke local |
| **Semua dijadikan local** | standar pusat hilang | pertahankan hukum universal di global |
| **Override diam-diam** | AI berperilaku aneh antar repo | tulis local override secara eksplisit |

---

## Materi Selanjutnya

- [BK-03: Artifact Governance di Dalam .cursorrules](../BK-03-Artifact-Governance-di-Dalam-cursorrules/README.md)
