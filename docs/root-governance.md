# Root Governance: Cursor-SOP (PPM V6 Unified)

Dokumen ini adalah **hukum tertinggi** repositori Cursor-SOP. Semua AI Agent dan kontributor wajib mematuhinya.

---

## Arsitektur: One-Tier Unified

Repositori ini menggunakan **satu layer** tunggal. Tidak ada lagi pemisahan `TECHNICAL-CORE` vs root RAKs.
Setiap dokumen harus berdiri sendiri — komprehensif, mudah dipahami, dan teknis sekaligus.

---

## Hierarki 5-Level

```
Rak (RAK) → Sub-Rak (SR) → Buku (BK) → Chapter (CH) → Section (SC)
```

| Level | Kode | Contoh |
|---|---|---|
| Rak | `RAK-01` | Domain pengetahuan utama |
| Sub-Rak | `SR-01` | Kluster topik dalam satu RAK |
| Buku | `BK-01` | Materi spesifik dalam SR |
| Chapter | `CH-01` | Bab dalam sebuah Buku |
| Section | `SC-01` | Sub-bab detail |

---

## Standar Dokumen: PPM V6 Unified

Setiap `README.md` di level RAK **wajib** memiliki 6 elemen berikut secara berurutan:

| No | Elemen | Isi |
|---|---|---|
| 0 | 🌟 **Gampangnya...** | 1–2 paragraf bahasa santai, tidak teknis |
| 1 | 📖 **Konteks & Sejarah** | Kenapa ini ada, latar belakang |
| 2 | ⚙️ **Cara Kerja** | Mekanisme teknis (+ Mermaid diagram jika relevan) |
| 3 | 🗺️ **Kapan Digunakan** | Panduan per mode AI (DISCUSS/EXECUTE/dll.) |
| 4 | 🛠️ **Cara Pakai** | Langkah praktis, template prompt siap pakai |
| 5 | 🧪 **Lab Praktek** | Skenario nyata, contoh konkret |
| 6 | ⚠️ **Jebakan & Solusi** | Kesalahan umum + cara menghindarinya |

---

## Konvensi Penomoran

- **Rak**: `RAK-00`, `RAK-01`, ..., `RAK-09`
- **Sub-Rak**: `SR-01`, `SR-02`, ...
- **Buku**: `BK-01`, `BK-02`, ...
- **Chapter**: `CH-01`, `CH-02`, ...
- **Section**: `SC-01`, `SC-02`, ...

---

## Struktur Root

```
Cursor-SOP/
  ├── .cursorrules         ← Hukum interaksi AI
  ├── README.md            ← Pendahuluan & Taxonomy
  ├── CHANGELOG.md         ← Log semua perubahan besar
  ├── status.md            ← Progress dashboard
  ├── docs/
  │   └── root-governance.md  ← Dokumen ini
  ├── RAK-00-The-Gateway/
  ├── RAK-01 s/d RAK-09/   ← Semua rak utama (One-Tier)
  └── examples/
```

---

## Status

Aktif. Mematuhi **PPM V6 Unified** sejak 2026-03.
