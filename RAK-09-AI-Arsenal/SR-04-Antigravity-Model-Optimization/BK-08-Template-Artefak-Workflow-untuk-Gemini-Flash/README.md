# BK-08: Template Artefak Workflow untuk Gemini Flash

## Gampangnya...

Kalau `BK-07` menjelaskan aturan mainnya, buku ini memberi kamu bentuk dokumen yang bisa langsung dipakai. Tujuannya sederhana: jangan biarkan `Gemini Flash` menebak-nebak posisi kerja.

Dengan paket template yang rapi, kamu tidak perlu lagi bingung mana yang harus dicentang, mana yang harus dibaca duluan, dan mana yang cuma dipakai untuk penutupan sesi.

---

## Konteks & Sejarah

Banyak workflow AI gagal bukan karena user tidak punya ide, tetapi karena artefak kerjanya lahir secara spontan:
- kadang `implementation plan` dijadikan checklist,
- kadang task list berdiri sendiri tanpa induk plan,
- kadang tracker tidak ada,
- kadang laporan akhir malah dipakai untuk menebak progres aktif.

Untuk model cepat seperti `Gemini Flash`, struktur seperti ini terlalu berisik. Model akan cenderung mengikuti dokumen yang paling dekat atau paling baru terlihat, bukan yang paling benar.

Karena itu, setelah hirarki artefak ditetapkan di `BK-07`, langkah berikutnya adalah menyediakan bentuk template yang stabil agar governance itu bisa dipraktikkan tanpa banyak improvisasi.

---

## Cara Kerja

### Paket Artefak Minimum

| File | Peran | Status |
|---|---|---|
| `blueprint.md` | arah solusi | tidak dicentang |
| `implementation-plan.md` | urutan fase | tidak dicentang |
| `tasks.md` | checklist kerja aktif | dicentang |
| `tracker.md` | status aktual | tidak dicentang |
| `handover.md` | ringkasan sesi | tidak dicentang |

### Urutan Pakai

1. Buat `blueprint.md`
2. Turunkan menjadi `implementation-plan.md`
3. Turunkan plan menjadi `tasks.md`
4. Set posisi awal di `tracker.md`
5. Kerjakan satu task aktif
6. Update `tasks.md` dan `tracker.md`
7. Tutup sesi dengan `handover.md`

### Rule Ringkas

- `blueprint.md` menjawab: kita mau membangun apa
- `implementation-plan.md` menjawab: urutannya bagaimana
- `tasks.md` menjawab: sekarang kita kerjakan apa
- `tracker.md` menjawab: kita sedang ada di mana
- `handover.md` menjawab: tadi sudah terjadi apa
- jika jumlah artefak mulai ramai, tambahkan `artifact-map.md` sebagai peta baca di awal sesi

---

## Kapan Digunakan

Gunakan buku ini saat:
- kamu ingin mulai workflow baru dengan struktur dokumen yang rapi,
- `Gemini Flash` sering loncat ke fase yang belum waktunya,
- kamu ingin satu paket template yang bisa di-copy ke proyek nyata,
- kamu butuh bentuk dokumen yang mudah dipelihara lintas sesi.

Kalau kamu masih bingung kenapa artefak-artefak ini perlu dipisah, baca `BK-07` dulu. Buku ini cocok dipakai setelah kamu setuju dengan governance dasarnya.

---

## Cara Pakai

### Template 1: `blueprint.md`

```md
# Blueprint

## Goal
- Apa yang ingin dicapai?

## Scope
- Apa yang termasuk dikerjakan?

## Out of Scope
- Apa yang sengaja tidak dikerjakan?

## Affected Areas
- File, modul, atau domain yang terdampak

## Risks
- Risiko utama
- Dependency penting

## Success Criteria
- Tanda bahwa solusi dianggap selesai
```

### Template 2: `implementation-plan.md`

```md
# Implementation Plan

## Phase 1 - Foundation
- tujuan:
- output:
- exit criteria:

## Phase 2 - Core Logic
- tujuan:
- output:
- exit criteria:

## Phase 3 - Validation
- tujuan:
- output:
- exit criteria:

## Phase 4 - Review and Handover
- tujuan:
- output:
- exit criteria:
```

### Template 3: `tasks.md`

```md
# Tasks

- [ ] T-01
  linked_plan_step: Phase 1 - Foundation
  title: Siapkan struktur awal
  notes: -

- [ ] T-02
  linked_plan_step: Phase 2 - Core Logic
  title: Implementasi logika inti
  notes: menunggu T-01 selesai

- [ ] T-03
  linked_plan_step: Phase 3 - Validation
  title: Lakukan validasi dasar
  notes: -

- [ ] T-04
  linked_plan_step: Phase 4 - Review and Handover
  title: Buat handover akhir
  notes: -
```

### Template 4: `tracker.md`

```md
# Tracker

current_mode: EXECUTE
current_plan_step: Phase 1 - Foundation
active_task_id: T-01
status: in_progress

last_completed:
- none

blockers:
- none

mismatch_check:
- tasks_vs_plan: aligned
- tracker_vs_tasks: aligned

next_action:
- selesaikan T-01
```

### Template 5: `handover.md`

```md
# Handover

## What Was Done
- ...

## Files or Areas Touched
- ...

## Key Decisions
- ...

## Unresolved Items
- ...

## Next Recommended Start Point
- ...
```

### Prompt Start Pack

Gunakan prompt ini saat memulai sesi:

```text
Gunakan workflow artefak terpisah.
1. Buat blueprint.md dulu.
2. Turunkan jadi implementation-plan.md.
3. Turunkan plan menjadi tasks.md.
4. Buat tracker.md dan tetapkan active_task_id.
Jangan mulai implementasi sebelum task aktif jelas.
```

### Prompt Loop Pack

Gunakan prompt ini setiap kali mau lanjut:

```text
Baca tracker.md dulu.
Kerjakan hanya active_task_id yang sedang aktif.
Setelah selesai, update tasks.md dan tracker.md.
Jika ada mismatch dengan implementation-plan.md,
berhenti dan laporkan konflik status.
```

### Prompt Penutup Sesi

Gunakan prompt ini saat sesi selesai:

```text
Buat handover.md berdasarkan tracker.md, tasks.md, dan implementation-plan.md.
Ringkas yang sudah selesai, yang belum selesai, dan titik mulai terbaik untuk sesi berikutnya.
```

---

## Lab Praktek

**Skenario: Membuat fitur baru dengan Gemini Flash**

Target:
membangun fitur kecil dengan empat fase: foundation, core logic, validation, dan handover.

Workflow sehat:

1. isi `blueprint.md` dulu agar scope jelas,
2. pecah menjadi empat fase di `implementation-plan.md`,
3. turunkan tiap fase menjadi task di `tasks.md`,
4. set `tracker.md` ke `T-01`,
5. minta AI hanya mengerjakan `T-01`,
6. setelah selesai, centang `T-01`, update tracker ke `T-02`,
7. ulangi sampai fase review,
8. buat `handover.md`.

Yang perlu diperhatikan:
- jangan centang phase di implementation plan,
- jangan ubah tracker tanpa mengubah task terkait,
- jangan pakai handover untuk menentukan task aktif.

Hasil yang diharapkan:
- AI tidak loncat ke fase berikutnya,
- progres bisa dibaca tanpa membuka seluruh percakapan,
- sesi berikutnya bisa lanjut dari tracker dan handover.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Semua file terasa checklist** | User bingung mana status utama | Hanya `tasks.md` yang boleh dicentang |
| **Tracker ditulis sekali lalu ditinggal** | AI mengikuti status lama | Update tracker setiap loop |
| **Task tidak punya induk plan** | AI mengerjakan item liar | Wajib isi `linked_plan_step` |
| **Handover terlalu dini** | Ringkasan dibuat sebelum progres stabil | Simpan handover untuk akhir loop besar atau akhir sesi |
| **Template terlalu besar untuk task kecil** | User malas memakainya | Untuk task receh, pakai versi ringkas dengan fase lebih sedikit |

---

## Materi Sebelumnya

- [BK-07: Sinkronisasi Task, Implementation Plan, dan Tracker](../BK-07-Sinkronisasi-Task-Implementation-Plan-dan-Tracker/README.md)
- [RAK-08 / BK-03: Template `artifact-map.md` untuk Artifact Governance](../../../../RAK-08-Matrix-Intersection/SR-01-Consistency-Management/BK-03-Template-Artifact-Map-untuk-Artifact-Governance/README.md)

