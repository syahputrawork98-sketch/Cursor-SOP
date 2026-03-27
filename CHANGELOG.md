# CHANGELOG - Cursor-SOP

Semua perubahan besar pada repositori ini dicatat di sini secara kronologis.

---

## [2026-03-28] - RAK-07 Expansion: Curator Workflows

### New Features
- Menambahkan `SR-03-Curator-Workflows` di `RAK-07-Specialization`.
- Menambahkan empat pola kurator utama:
  - `Creation` untuk project baru,
  - `Repair` untuk perbaikan dan bugfix,
  - `Refactor` untuk pembenahan struktur,
  - `Documentation` untuk handover dan penangkapan pengetahuan.

### Notes
- Kurator dibedakan berdasarkan **jenis operasi terhadap proyek**, bukan berdasarkan domain seperti website atau backend.

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

## [2026-03-28] - RAK-09 Expansion: Antigravity Model Optimization

### New Features
- Menambahkan `SR-04-Antigravity-Model-Optimization` di `RAK-09-AI-Arsenal`.
- Menambahkan panduan baru untuk:
  - peta model premium di Antigravity,
  - keluarga Gemini,
  - keluarga Claude,
  - model economy seperti `GPT-OSS 120B Medium`,
  - strategi kuota dan routing task,
  - playbook pemilihan model per jenis kerja.

### Notes
- Konten baru difokuskan pada optimasi lineup model yang tersedia di akun premium yang sedang digunakan, bukan pada dokumentasi Gemini app umum.

---

## [2026-03-28] - RAK-02 Expansion: AI Interaction Modes

### New Features
- Menambahkan `SR-02-AI-Interaction-Modes` di `RAK-02-Foundation-Core-Rules`.
- Menambahkan panduan baru untuk:
  - peta 10 mode inti internal repo,
  - extended modes dari praktik internet modern,
  - panduan kapan memakai mode yang tepat,
  - hubungan antara mode dasar dan curator workflow,
  - living registry serta protokol update mode.

### Notes
- Sub-rak baru ini sengaja memakai pendekatan dua lapis: `core modes` untuk aturan operasional repo, dan `extended modes` untuk pengetahuan luas yang berkembang di internet.

---

## [2026-03-27] - Unified Architecture Refactoring (PPM V6)

### Breaking Changes
- **Arsitektur Two-Tier dihapus**: folder `TECHNICAL-CORE/` akan di-merge ke root RAKs dan dihapus.
- **PPM V4 & V5 digantikan oleh PPM V6 Unified**: satu standar komprehensif untuk semua dokumen.

### New Features
- **PPM V6 Unified**: 6 elemen wajib per dokumen RAK (Gampangnya -> Konteks -> Cara Kerja -> Kapan Digunakan -> Cara Pakai -> Lab Praktek -> Jebakan).
- **10 Mode Interaksi AI**: `DISCUSS`, `BLUEPRINT`, `PLAN`, `ANALYZE`, `EXECUTE`, `REVIEW`, `DEBUG`, `TEST`, `REFACTOR`, `DOCUMENT`.
- **RAK-09: AI Arsenal** (baru): panduan pemilihan model AI (Gemini vs ChatGPT) + Quota Blending Strategy.
- **SR-04-Updates** di `RAK-00`: sub-rak baru untuk mencatat update AI dan best practice revisions.

### Modifications
- `.cursorrules`: ditulis ulang total dengan PPM V6 + Anti-Blunder Protocol.
- `docs/root-governance.md`: updated ke One-Tier Unified + definisi PPM V6.
- `status.md`: reset dan diformat ulang.

---

## [2026-03-26] - Granular Deepening (PPM V4, sebelum refaktori)

- Semua 28 Buku (BK) di `RAK-01` s.d. `RAK-08` dikonversi ke struktur direktori dengan chapter.
- Two-Tier Architecture diimplementasikan (root Human-First + `TECHNICAL-CORE`).

---
