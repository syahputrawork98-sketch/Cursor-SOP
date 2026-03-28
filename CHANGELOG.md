# CHANGELOG - Cursor-SOP

Semua perubahan besar pada repositori ini dicatat di sini secara kronologis.

---

## [2026-03-28] - RAK-05 Addition: Structured Rules Architecture

### New Features
- Menambahkan `SR-03-Structured-Rules-Architecture` di `RAK-05-Ecosystem-Tooling`.
- Menambahkan rangkaian buku baru untuk:
  - blueprint standar `.cursorrules` bertingkat,
  - pemisahan `global rules` vs `local rules`,
  - artifact governance di dalam `.cursorrules`,
  - activation rules untuk role packs dan review lenses,
  - template `.cursorrules` untuk frontend, backend, dan workspace gabungan.

### Notes
- Penambahan ini dibuat sebagai fondasi untuk workflow rules yang lebih matang sebelum masuk ke AI profiles per domain di rak lain.


## [2026-03-28] - RAK-05 Expansion: Database Rules Template

### New Features
- Menambahkan `BK-08-Template-cursorrules-untuk-Project-Database` di `RAK-05-Ecosystem-Tooling/SR-03-Structured-Rules-Architecture`.
- Menambahkan template domain database untuk:
  - schema clarity,
  - migration safety,
  - rollback thinking,
  - data integrity,
  - query dan consumer impact review.
- Menambahkan `example pack` untuk database berupa:
  - `example-cursorrules.md`,
  - `example-artifact-map.md`,
  - `example-tasks.md`,
  - `example-tracker.md`.

### Notes
- Penambahan ini melengkapi trio domain template menjadi frontend, backend, workspace gabungan, dan database sebagai domain khusus yang lebih sensitif terhadap perubahan destruktif.
## [2026-03-28] - RAK-09 Addition: Task-Plan Synchronization for Antigravity

### New Features
- Menambahkan `BK-07-Sinkronisasi-Task-Implementation-Plan-dan-Tracker` di `RAK-09-AI-Arsenal/SR-04-Antigravity-Model-Optimization`.
- Menambahkan panduan baru untuk:
  - membedakan fungsi `implementation plan`, `tasks`, dan `tracker`,
  - menetapkan hirarki kebenaran antar artefak kerja,
  - mendeteksi `orphan task`, `plan drift`, `stale tracker`, dan `false completion`,
  - menjaga model cepat seperti `Gemini Flash` tetap sinkron saat bekerja bertahap.

### Notes
- Penambahan ini memperluas `SR-04` dari sekadar model picker menjadi juga **discipline layer** untuk workflow multi-artefak di Antigravity.

## [2026-03-28] - RAK-09 Addition: Practical Artifact Templates for Gemini Flash

### New Features
- Menambahkan `BK-08-Template-Artefak-Workflow-untuk-Gemini-Flash` di `RAK-09-AI-Arsenal/SR-04-Antigravity-Model-Optimization`.
- Menambahkan paket template praktis untuk:
  - `blueprint.md`,
  - `implementation-plan.md`,
  - `tasks.md`,
  - `tracker.md`,
  - `handover.md`.
- Menambahkan prompt start, prompt loop, dan prompt penutup sesi agar workflow ini lebih mudah dipakai di lapangan.

### Notes
- Buku ini dibuat sebagai pasangan praktis dari `BK-07`, agar governance sinkronisasi artefak bisa langsung diterapkan ke sesi kerja nyata dengan `Gemini Flash`.

## [2026-03-28] - RAK-09 Addition: ChatGPT Projects and Artifact Workflow

### New Features
- Menambahkan `BK-06-ChatGPT-Projects-dan-Artefak-Kerja` di `RAK-09-AI-Arsenal/SR-03-ChatGPT-Models-and-Usage`.
- Menambahkan `BK-07-Template-Artefak-Workflow-untuk-ChatGPT-Projects` di `RAK-09-AI-Arsenal/SR-03-ChatGPT-Models-and-Usage`.
- Menambahkan panduan baru untuk:
  - membedakan kerja `context-only` vs `Projects + file .md`,
  - memakai `Project instructions`, uploaded files, dan project memory secara lebih disiplin,
  - menyimpan `blueprint`, `implementation-plan`, `tasks`, `tracker`, dan `handover` sebagai artefak terpisah dalam ChatGPT Projects.

### Notes
- Penambahan ini dibuat agar workflow ChatGPT untuk kerja multi-sesi tidak bentrok dengan pola artifact governance yang sudah dibangun untuk Antigravity/Gemini.

## [2026-03-28] - RAK-08 Addition: `artifact-map.md` Template for Cross-Tool Artifact Governance

### New Features
- Menambahkan `BK-03-Template-Artifact-Map-untuk-Artifact-Governance` di `RAK-08-Matrix-Intersection/SR-01-Consistency-Management`.
- Menambahkan panduan baru untuk:
  - memakai `artifact-map.md` sebagai `artifact map` lintas ChatGPT, Gemini, dan tool lain,
  - menetapkan file authoritative dan urutan baca artefak,
  - membedakan `artifact-map.md` dari `blueprint.md`, `tasks.md`, `tracker.md`, dan `handover.md`,
  - menuliskan `conflict rules` agar AI tidak improvisasi saat artefak bentrok.

### Notes
- `artifact-map.md` diposisikan sebagai konvensi kerja lintas-tool, bukan fitur native resmi dari ChatGPT atau Gemini.

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









