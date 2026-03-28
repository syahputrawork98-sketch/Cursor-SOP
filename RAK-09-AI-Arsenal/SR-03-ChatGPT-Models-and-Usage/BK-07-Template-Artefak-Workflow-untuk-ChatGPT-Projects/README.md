# BK-07: Template Artefak Workflow untuk ChatGPT Projects

## Gampangnya...

Kalau kamu sudah setuju bahwa ChatGPT sebaiknya tidak hanya mengandalkan context window untuk kerja panjang, buku ini memberi bentuk operasionalnya. Isinya adalah paket template `.md` yang bisa kamu upload atau simpan di dalam `Project`.

Tujuannya adalah membuat ChatGPT tetap fokus dan tidak bentrok antara isi chat, isi plan, dan status kerja aktual.

---

## Konteks & Sejarah

ChatGPT unggul untuk diskusi, penjelasan, dan synthesis. Tapi justru karena sifatnya sangat conversational, progres kerja sering terasa cair. Tanpa artefak yang jelas, user mudah bingung:
- mana hasil diskusi,
- mana keputusan final,
- mana task aktif,
- mana ringkasan sesi.

Template workflow ini dibuat agar ChatGPT bisa dipakai lebih disiplin tanpa harus berubah menjadi coding agent penuh seperti Codex.

---

## Cara Kerja

### Paket File Minimum

| File | Fungsi | Checklist |
|---|---|---|
| `blueprint.md` | arah solusi | tidak |
| `implementation-plan.md` | fase kerja | tidak |
| `tasks.md` | daftar task aktif | ya |
| `tracker.md` | posisi kerja saat ini | tidak |
| `handover.md` | ringkasan akhir sesi | tidak |

### Urutan Pakai

1. mulai dari `blueprint.md`
2. turunkan ke `implementation-plan.md`
3. turunkan ke `tasks.md`
4. set task aktif di `tracker.md`
5. gunakan chat untuk mengerjakan task aktif
6. update `tasks.md` dan `tracker.md`
7. tutup sesi dengan `handover.md`

### Aturan Singkat

- chat adalah tempat berpikir,
- files adalah tempat menjaga state,
- `tasks.md` adalah checklist utama,
- `tracker.md` adalah panel posisi sekarang.

---

## Kapan Digunakan

Gunakan template ini saat:
- kamu bekerja dalam satu `Project` ChatGPT selama beberapa hari,
- kamu ingin obrolan tetap fleksibel tapi state tetap rapi,
- kamu butuh handover yang jelas untuk sesi berikutnya,
- kamu ingin mengurangi bentrok antara percakapan dan progres.

Kalau kamu cuma diskusi satu kali, template ini terlalu berat. Simpan untuk kerja yang benar-benar berkembang.

---

## Cara Pakai

### Template 1: `blueprint.md`

```md
# Blueprint

## Goal
- ...

## Scope
- ...

## Out of Scope
- ...

## Risks
- ...

## Success Criteria
- ...
```

### Template 2: `implementation-plan.md`

```md
# Implementation Plan

## Phase 1 - Discovery
- tujuan:
- output:

## Phase 2 - Structuring
- tujuan:
- output:

## Phase 3 - Drafting or Execution
- tujuan:
- output:

## Phase 4 - Review and Handover
- tujuan:
- output:
```

### Template 3: `tasks.md`

```md
# Tasks

- [ ] T-01
  linked_plan_step: Phase 1 - Discovery
  title: Rapikan requirement

- [ ] T-02
  linked_plan_step: Phase 2 - Structuring
  title: Bentuk outline kerja

- [ ] T-03
  linked_plan_step: Phase 3 - Drafting or Execution
  title: Kerjakan task inti

- [ ] T-04
  linked_plan_step: Phase 4 - Review and Handover
  title: Buat handover
```

### Template 4: `tracker.md`

```md
# Tracker

current_phase: Phase 2 - Structuring
active_task_id: T-02
status: in_progress

last_completed:
- T-01

blockers:
- none

next_action:
- lanjutkan T-02
```

### Template 5: `handover.md`

```md
# Handover

## What Was Done
- ...

## Key Decisions
- ...

## Open Questions
- ...

## Next Starting Point
- ...
```

### Project Instructions yang Disarankan

Masukkan instruksi seperti ini ke `Project instructions`:

```text
Gunakan file artefak kerja sebagai sumber kebenaran utama.
Jangan jadikan chat history sebagai satu-satunya tracker.
Jika ada konflik antara obrolan dan file artefak, beri tahu saya dulu.
Untuk progres, rujuk tasks.md dan tracker.md.
```

### Prompt Start Pack

```text
Kita pakai workflow ChatGPT Project.
Baca blueprint.md dulu.
Lalu turunkan ke implementation-plan.md, tasks.md, dan tracker.md.
Jangan mulai task sebelum active_task_id jelas.
```

### Prompt Loop Pack

```text
Baca tracker.md dulu.
Fokus hanya pada active_task_id.
Setelah loop selesai, usulkan update untuk tasks.md dan tracker.md.
Jangan ubah arah plan tanpa menjelaskannya.
```

### Prompt Penutup

```text
Tutup sesi ini dengan handover.md.
Ringkas yang selesai, yang belum selesai, keputusan penting, dan titik mulai terbaik untuk sesi berikutnya.
```

---

## Lab Praktek

**Skenario: Project ChatGPT untuk kerja beberapa hari**

Hari 1:
- buat blueprint dan plan
- turunkan ke tasks
- set tracker ke task pertama

Hari 2:
- buka project yang sama
- minta ChatGPT membaca `tracker.md` dulu
- lanjutkan hanya task aktif

Hari 3:
- lakukan review
- buat handover

Dengan pola ini, kamu tidak lagi bergantung penuh pada ingatan percakapan. Chat tetap penting, tapi dia tidak memegang semua beban struktur.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Project dipakai seperti chat biasa** | file ada tapi tidak pernah dirujuk | paksa tiap sesi membaca `tracker.md` dulu |
| **Task aktif tidak jelas** | ChatGPT mengerjakan hal random | tetapkan `active_task_id` |
| **Project instructions terlalu umum** | ChatGPT tetap liar | tulis aturan artefak secara eksplisit |
| **Chat lebih dipercaya dari file** | state mulai bentrok | jadikan file artefak sebagai sumber kebenaran |

---

## Referensi Resmi

- OpenAI Help Center: https://help.openai.com/en/articles/10169521
- OpenAI Help Center: https://help.openai.com/en/articles/9309188-add-files-from-connected-apps-in-chatgpt

---

## Materi Sebelumnya

- [BK-06: ChatGPT Projects dan Artefak Kerja](../BK-06-ChatGPT-Projects-dan-Artefak-Kerja/README.md)
