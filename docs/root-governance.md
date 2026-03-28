# Root Governance: Cursor-SOP (PPM V6 Unified)

Dokumen ini adalah hukum tertinggi repositori Cursor-SOP. Semua AI agent dan kontributor wajib mematuhinya.

---

## Arsitektur: One-Tier Unified

Repositori ini menggunakan satu layer tunggal. Tidak ada lagi pemisahan `TECHNICAL-CORE` vs root RAKs.
Setiap dokumen harus berdiri sendiri: komprehensif, mudah dipahami, dan tetap teknis saat perlu.

---

## Hierarki 5-Level

```text
Rak (RAK) -> Sub-Rak (SR) -> Buku (BK) -> Chapter (CH) -> Section (SC)
```

| Level | Kode | Contoh |
|---|---|---|
| Rak | `RAK-01` | Domain pengetahuan utama |
| Sub-Rak | `SR-01` | Kluster topik dalam satu RAK |
| Buku | `BK-01` | Materi spesifik dalam SR |
| Chapter | `CH-01` | Bab dalam sebuah buku |
| Section | `SC-01` | Sub-bab detail |

---

## Standar Dokumen: PPM V6 Unified

Setiap `README.md` di level RAK wajib memiliki elemen berikut secara berurutan:

| No | Elemen | Isi |
|---|---|---|
| 0 | **Gampangnya...** | 1-2 paragraf bahasa santai, tidak teknis |
| 1 | **Konteks & Sejarah** | Kenapa ini ada, latar belakang |
| 2 | **Cara Kerja** | Mekanisme teknis, diagram jika relevan |
| 3 | **Kapan Digunakan** | Panduan per mode AI |
| 4 | **Cara Pakai** | Langkah praktis dan template prompt |
| 5 | **Lab Praktek** | Skenario nyata dan contoh konkret |
| 6 | **Jebakan & Solusi** | Kesalahan umum dan cara menghindarinya |

---

## Taxonomy Mode AI

Repo ini membedakan tiga lapisan agar istilah kerja AI tidak tercampur:

| Lapisan | Fungsi | Status |
|---|---|---|
| **Core Modes** | Mode operasional resmi repo untuk kerja harian | Wajib dipatuhi |
| **Extended Modes** | Mode atau pola luas dari praktik internet modern | Pengetahuan tambahan |
| **Curator Workflows** | Rangkaian beberapa mode untuk jenis kerja tertentu | Workflow spesialis |

### Aturan Dasar

- **Core Modes** adalah set mode resmi yang dipakai di aturan operasional repo.
- **Extended Modes** boleh dikenali, dipelajari, dan dipetakan, tetapi tidak otomatis menjadi aturan kerja harian.
- **Curator Workflows** bukan mode baru; mereka adalah orkestrasi dari beberapa mode dasar.
- Jika ada istilah baru dari luar, status awalnya adalah `extended` sampai dievaluasi lewat registry dan governance.

### Rujukan Utama

- `RAK-02 / SR-02` untuk peta `core modes`, `extended modes`, dan update protocol.
- `RAK-07 / SR-03` untuk `curator workflows` dan orkestrasi mode berdasarkan jenis kerja.
- `RAK-07 / SR-04` untuk `domain AI profiles` dan lensa spesialis seperti database.

---

## Konvensi Penomoran

- **Rak**: `RAK-00`, `RAK-01`, ..., `RAK-09`
- **Sub-Rak**: `SR-01`, `SR-02`, ...
- **Buku**: `BK-01`, `BK-02`, ...
- **Chapter**: `CH-01`, `CH-02`, ...
- **Section**: `SC-01`, `SC-02`, ...

---

## Struktur Root

```text
Cursor-SOP/
  .cursorrules
  README.md
  CHANGELOG.md
  status.md
  docs/
    root-governance.md
  RAK-00-The-Gateway/
  RAK-01 s/d RAK-09/
  examples/
```

---

## Status

Aktif. Mematuhi **PPM V6 Unified** sejak 2026-03.


