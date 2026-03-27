# 📋 CHANGELOG — Cursor-SOP

Semua perubahan besar pada repositori ini dicatat di sini secara kronologis.

---

## [2026-03-28] - RAK-09 Expansion: ChatGPT Models and Usage

### New Features
- Menambahkan `SR-03-ChatGPT-Models-and-Usage` di `RAK-09-AI-Arsenal`.
- Menambahkan panduan baru untuk:
  - peta produk ChatGPT,
  - pemilihan model di ChatGPT,
  - selector thinking/reasoning,
  - strategi kuota mingguan,
  - batas penggunaan ChatGPT vs Codex vs API.

### Notes
- Konten baru ditulis dengan cap waktu karena lineup model dan availability plan cepat berubah.

---

## [2026-03-27] — Unified Architecture Refactoring (PPM V6)

### 💥 Breaking Changes
- **Arsitektur Two-Tier dihapus**: Folder `TECHNICAL-CORE/` akan di-merge ke root RAKs dan dihapus.
- **PPM V4 & V5 digantikan oleh PPM V6 Unified**: Satu standar komprehensif untuk semua dokumen.

### ✨ New Features
- **PPM V6 Unified**: 6 elemen wajib per dokumen RAK (Gampangnya → Konteks → Cara Kerja → Kapan Digunakan → Cara Pakai → Lab Praktek → Jebakan).
- **10 Mode Interaksi AI**: DISCUSS, BLUEPRINT, PLAN, ANALYZE, EXECUTE, REVIEW, DEBUG, TEST, REFACTOR, DOCUMENT.
- **RAK-09: AI Arsenal** (baru): Panduan pemilihan model AI (Gemini vs ChatGPT) + Quota Blending Strategy.
- **SR-04-Updates** di RAK-00: Sub-rak baru untuk mencatat update AI dan best practice revisions.

### 🔧 Modifications
- `.cursorrules`: Ditulis ulang total dengan PPM V6 + Anti-Blunder Protocol.
- `docs/root-governance.md`: Updated ke One-Tier Unified + definisi PPM V6.
- `status.md`: Reset dan diformat ulang.

---

## [2026-03-26] — Granular Deepening (PPM V4, sebelum refaktori)

- Semua 28 Buku (BK) di RAK-01 s/d RAK-08 dikonversi ke struktur direktori dengan chapter.
- Two-Tier Architecture diimplementasikan (root Human-First + TECHNICAL-CORE).

---
