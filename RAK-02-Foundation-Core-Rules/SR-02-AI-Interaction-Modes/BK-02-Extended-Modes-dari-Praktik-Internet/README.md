# BK-02: Extended Modes dari Praktik Internet

Buku ini membahas mode tambahan yang banyak muncul di praktik agent modern di internet. Ini bukan daftar mode resmi repo, melainkan perpustakaan istilah dan pola kerja yang penting untuk dipahami agar wawasanmu tidak berhenti di 10 mode internal saja.

> Status per 2026-03-28.
> Isi buku ini adalah sintesis dari praktik umum yang tampak di sumber resmi OpenAI, Anthropic, dan Google. Tidak ada satu standar industri yang menetapkan jumlah mode universal.

---

## Gampangnya...

Internet modern tidak bicara hanya soal `DISCUSS`, `PLAN`, dan `EXECUTE`. Di praktik agent modern, kamu juga akan sering melihat istilah seperti `tool use`, `retrieval`, `memory`, `handoff`, `guardrail`, dan `self-correction`.

Istilah-istilah ini penting untuk diketahui supaya kamu paham bahwa dunia luar bekerja dengan lensa yang lebih lebar. Tetapi repo ini sengaja tidak menjadikan semuanya sebagai mode inti, agar sistem sehari-harinya tetap rapi.

---

## Konteks & Sejarah

Sumber resmi modern menggambarkan agent sebagai sistem yang:
- dapat memilih alat,
- bisa menjalankan loop beberapa langkah,
- bisa mengambil konteks,
- dapat handoff ke agent lain,
- dan perlu guardrail agar tetap aman.

OpenAI menekankan model, tools, dan instructions sebagai komponen dasar agent. Anthropic menekankan tool use, memory, context management, dan agent loop. Google menyorot agent yang dapat plan, execute, dan synthesize multi-step tasks.

Dari sinilah muncul mode-mode tambahan yang sering beredar di internet.

---

## Cara Kerja

### Daftar Extended Modes yang Paling Umum

| Istilah | Kategori | Fungsi Ringkas | Hubungan ke Core Modes |
|---|---|---|---|
| `INTAKE / CLARIFY` | `Mode` | Menangkap tujuan dan batasan | Dekat dengan `DISCUSS` |
| `RESEARCH / RETRIEVE` | `Mode` | Mengambil informasi dan referensi | Dekat dengan `ANALYZE` |
| `TOOL USE` | `Mechanism` | Memakai tool, function, atau API | Sering terjadi saat `EXECUTE` atau `ANALYZE` |
| `MEMORY / CONTEXT MANAGEMENT` | `Mechanism` | Menyimpan dan mengatur konteks | Mendukung semua mode |
| `HANDOFF / ROUTE / ESCALATE` | `Workflow Concern` | Menyerahkan kerja ke agent lain, model lain, atau user | Dekat dengan workflow kurator |
| `MONITOR / GUARDRAIL` | `Workflow Concern` | Menjaga batas, kebijakan, dan keamanan | Dekat dengan `REVIEW` |
| `REFLECT / SELF-CORRECT` | `Mode` | Mengoreksi diri sebelum lanjut | Dekat dengan `REVIEW` dan `ANALYZE` |
| `SYNTHESIZE` | `Mode` | Merangkum hasil multi-sumber menjadi jawaban utuh | Dekat dengan `DOCUMENT` |
| `ORCHESTRATE` | `Mechanism` | Mengatur urutan agent, tool, dan langkah | Dekat dengan `PLAN` dan kurator |

### Cara Membaca Kategori Ini

- `Mode` berarti ia bisa dipahami sebagai posisi kerja yang relatif mandiri.
- `Mechanism` berarti ia lebih sering menjadi cara kerja lintas mode, bukan mode harian yang berdiri sendiri.
- `Workflow Concern` berarti ia biasanya hidup di level orkestrasi, kontrol, atau pengelolaan alur, bukan di level mode kerja dasar.

### Penjelasan Detail per Mode

#### `INTAKE / CLARIFY`

Apa itu:
fase menerima kebutuhan dan memperjelas maksud user.

Kenapa muncul:
karena banyak workflow agent modern perlu memastikan tujuan dan constraint di awal.

Kapan dipakai:
- saat kebutuhan user belum jelas,
- saat ada ruang salah tafsir besar.

Hubungan ke core modes:
repo ini menyerapnya terutama ke `DISCUSS`.

#### `RESEARCH / RETRIEVE`

Apa itu:
fase mencari informasi dari web, dokumen, database, atau knowledge base.

Kenapa muncul:
karena agent modern sering perlu konteks eksternal, bukan hanya berpikir dari memori model.

Kapan dipakai:
- saat topik butuh sumber,
- saat perlu data terbaru,
- saat perlu basis keputusan.

Hubungan ke core modes:
biasanya menjadi bagian dari `ANALYZE`, tapi di sistem luas sering dipisah sendiri.

#### `TOOL USE`

Apa itu:
fase ketika model memakai tool, function call, search, shell, editor, atau API.

Kenapa muncul:
karena agent modern semakin banyak bekerja dengan alat nyata, bukan sekadar teks.

Kapan dipakai:
- saat butuh aksi atau data yang tidak bisa didapat hanya lewat percakapan.

Hubungan ke core modes:
sering menjadi mekanisme di dalam `ANALYZE`, `DEBUG`, atau `EXECUTE`.

#### `MEMORY / CONTEXT MANAGEMENT`

Apa itu:
fase mengelola konteks, ringkasan, state, atau ingatan kerja agent.

Kenapa muncul:
karena percakapan panjang dan tool-heavy workflows butuh pengelolaan konteks yang sadar.

Kapan dipakai:
- saat session panjang,
- saat agent perlu mempertahankan state,
- saat perlu compaction atau caching.

Hubungan ke core modes:
repo ini lebih sering memperlakukannya sebagai mekanisme lintas mode, bukan mode inti terpisah.

#### `HANDOFF / ROUTE / ESCALATE`

Apa itu:
fase menyerahkan kerja ke agent lain, tool lain, model lain, atau kembali ke user.

Kenapa muncul:
karena agent modern sering multi-agent atau multi-model.

Kapan dipakai:
- saat satu agent tidak lagi paling cocok,
- saat butuh kontrol manusia,
- saat perlu model atau spesialisasi berbeda.

Hubungan ke core modes:
paling dekat dengan konsep `curator workflows` dan orkestrasi, sehingga lebih tepat dipahami di level workflow concern.

#### `MONITOR / GUARDRAIL`

Apa itu:
fase menjaga agar agent tetap aman, patuh aturan, dan tidak keluar jalur.

Kenapa muncul:
karena agent yang bisa bertindak juga perlu pagar.

Kapan dipakai:
- saat ada kebijakan,
- saat ada risiko keamanan,
- saat aksi yang salah bisa mahal.

Hubungan ke core modes:
repo ini biasanya memadukannya ke `REVIEW`, rules, dan governance, bukan memisahkannya menjadi mode kerja harian.

#### `REFLECT / SELF-CORRECT`

Apa itu:
fase ketika agent mengecek diri sendiri dan memperbaiki langkahnya.

Kenapa muncul:
karena beberapa model dan framework modern memberi ruang untuk reflection atau corrective loop.

Kapan dipakai:
- saat task kompleks,
- saat ada banyak langkah,
- saat biaya kesalahan tinggi.

Hubungan ke core modes:
dekat dengan `ANALYZE` dan `REVIEW`, tapi di internet kadang dibedakan sendiri.

#### `SYNTHESIZE`

Apa itu:
fase merangkai banyak temuan menjadi jawaban utuh.

Kenapa muncul:
karena research agent dan long-form agent sering menghasilkan banyak potongan hasil.

Kapan dipakai:
- saat hasil datang dari banyak sumber,
- saat perlu laporan atau ringkasan akhir.

Hubungan ke core modes:
dekat dengan `DOCUMENT`, walau fokusnya lebih ke penyatuan temuan.

#### `ORCHESTRATE`

Apa itu:
fase mengatur siapa melakukan apa, kapan, dan dalam urutan apa.

Kenapa muncul:
karena agent modern tidak selalu single-threaded; kadang ada manager agent, tools, dan handoff.

Kapan dipakai:
- saat multi-agent,
- saat multi-tool,
- saat workflow bercabang.

Hubungan ke core modes:
dekat dengan `PLAN`, tapi lebih meta karena mengatur sistem kerja, bukan hanya daftar langkah task. Karena itu ia lebih cocok dibaca sebagai mechanism daripada core mode.

---

## Kapan Digunakan

Pakai buku ini saat:
- kamu ingin wawasan yang lebih luas dari 10 mode inti,
- kamu menemukan istilah agentic baru di luar repo dan ingin tahu posisinya,
- kamu sedang merancang workflow baru dan butuh bahasa yang lebih kaya,
- kamu ingin menilai apakah satu mode tambahan layak diadopsi atau cukup dipahami saja.

Kalau kebutuhanmu hanya "task saya harus mode apa?", langsung lompat ke `BK-03`.

---

## Cara Pakai

### Cara Membaca Buku Ini dengan Sehat

1. Anggap buku ini sebagai kamus tambahan, bukan konstitusi harian.
2. Saat menemukan istilah baru, cari dulu mode inti tetangganya.
3. Tanyakan:
   - apakah ini benar-benar mode terpisah,
   - atau hanya mekanisme di dalam mode yang sudah ada?
4. Jika istilah itu berulang kali berguna, catat untuk evaluasi di `BK-05`.

### Sumber Rujukan Utama

- OpenAI: agent design, tools, orchestration, and handoffs.
- Anthropic: tool use, memory, context management, and agent loop.
- Google: plan, execute, synthesize, background execution, and context tools.

---

## Lab Praktek

**Skenario: agent riset modern**

Workflow luasnya bisa terlihat seperti ini:

`INTAKE -> RESEARCH -> TOOL USE -> PLAN -> EXECUTE -> SYNTHESIZE -> REVIEW`

Kalau ditarik ke sistem repo:

`DISCUSS -> ANALYZE -> PLAN -> EXECUTE -> DOCUMENT/REVIEW`

**Pelajaran**

Satu workflow luas dari internet sering kali bisa dipetakan ke beberapa core modes yang sudah lebih ringkas.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Semua istilah dianggap mode wajib** | Sistem jadi gemuk | Jadikan mode tambahan sebagai wawasan dulu |
| **Mode mekanis disalahpahami sebagai mode kerja** | `TOOL USE` dianggap selalu berdiri sendiri | Lihat dulu apakah ia hanya mekanisme di mode lain |
| **Tren baru langsung diadopsi** | Repo jadi tidak stabil | Gunakan `BK-05` untuk evaluasi |
| **Mode luas tidak dipetakan ke core** | User bingung memakai istilah luar di repo | Selalu cari core mode tetangganya |
