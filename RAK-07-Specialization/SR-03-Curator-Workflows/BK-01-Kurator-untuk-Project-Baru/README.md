# BK-01: Kurator untuk Project Baru

## Gampangnya...

Kurator ini adalah **mandor pembangunan**. Tugasnya memastikan sesuatu yang belum ada bisa lahir dengan bentuk yang sehat, bukan langsung dilempar ke coding liar tanpa fondasi.

Kalau kamu sedang membuat proyek baru, halaman baru, atau fitur besar dari nol, kurator inilah yang paling aman dipakai.

---

## Konteks & Sejarah

Task pembuatan baru paling sering gagal karena AI terlalu cepat menulis kode sebelum bentuk sistemnya jelas. Hasilnya biasanya:
- file kebanyakan sejak awal,
- arsitektur setengah matang,
- revisi berulang karena blueprint tidak pernah dikunci,
- user kelelahan membetulkan arah yang sejak awal kabur.

Creation Curator lahir untuk memperlambat sedikit di depan, agar tidak berdarah di belakang.

---

## Cara Kerja

### Alur Creation Curator

```mermaid
graph LR
    A[DISCUSS] --> B[BLUEPRINT]
    B --> C[PLAN]
    C --> D[ANALYZE]
    D --> E[EXECUTE]
    E --> F[REVIEW]
```

### Mode Utama

- `DISCUSS` untuk memperjelas tujuan
- `BLUEPRINT` untuk merancang struktur
- `PLAN` untuk memecah kerja menjadi langkah
- `ANALYZE` untuk membaca risiko dan trade-off
- `EXECUTE` untuk implementasi bertahap
- `REVIEW` untuk memvalidasi hasil

Mode pendukung:
- `TEST`
- `DOCUMENT`

---

## Kapan Digunakan

Gunakan kurator ini ketika:
- membangun website baru,
- menambah modul besar,
- membuat halaman baru,
- mendesain fondasi fitur besar,
- memulai implementasi yang sebelumnya belum ada sama sekali.

Jangan pakai kurator ini ketika:
- sistem sudah ada tapi rusak,
- target utama hanya bugfix,
- kamu cuma ingin merapikan struktur lama,
- tugas utamanya adalah dokumentasi atau handover.

---

## Cara Pakai

### Template Prompt

```text
"Saya ingin membangun [fitur/proyek] dari nol.
Gunakan Creation Curator.
Sebelum coding:
1. Jelaskan tujuan sistem
2. Sebutkan file/folder yang akan dibuat
3. Buat blueprint singkat
4. Pecah jadi langkah eksekusi
5. Tunjukkan risiko utamanya
Jangan menulis kode dulu."
```

### Checklist Kurator

1. Apa yang sedang dibangun?
2. Apa hasil akhirnya?
3. Struktur minimal yang sehat itu seperti apa?
4. File/folder apa yang akan lahir?
5. Risiko arsitektural terbesar ada di mana?
6. Eksekusi harus dimulai dari bagian mana dulu?

### Aturan Praktis

- jangan izinkan coding sebelum blueprint tertulis,
- pecah fitur besar menjadi tahap kecil,
- batasi eksekusi awal ke file atau area paling inti,
- review tiap fase besar sebelum maju.

### Kapan Harus Serahkan ke Kurator Lain

- Serahkan ke `Repair Curator` jika masalah utama berubah dari "membangun" menjadi "memulihkan yang rusak".
- Serahkan ke `Documentation Curator` jika implementasi inti sudah stabil dan kamu perlu membuat handover atau catatan keputusan.
- Jangan menyeret `Creation Curator` terlalu lama jika pekerjaan dominannya sudah berubah.

---

## Lab Praktek

**Skenario: Landing page baru**

Task:
"Saya ingin membuat landing page baru untuk produk saya."

Dengan Creation Curator, AI seharusnya:
- menjelaskan struktur halaman,
- mengusulkan file yang dibutuhkan,
- memetakan section utama,
- baru setelah itu masuk ke implementasi.

**Skenario: Modul autentikasi baru**

Task:
"Buat sistem autentikasi dari nol."

Kurator yang benar akan meminta:
- flow login,
- keputusan token/session,
- file atau layer yang akan dibuat,
- risiko keamanan dasar.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **AI lompat ke coding** | Belum ada bentuk, tapi kode sudah mengalir | Paksa blueprint tertulis dulu |
| **Blueprint terlalu umum** | Rencana ada, tapi tidak menunjuk file dan alur | Minta detail: file, flow, risiko |
| **Scope melebar** | Fitur baru berubah jadi "sekalian kita rombak semuanya" | Batasi tujuan task sejak awal |
| **Kelahiran terlalu cepat** | Terlalu banyak file dibuat sekaligus | Eksekusi bertahap, mulai dari inti |

---

## Materi Selanjutnya

- [BK-02: Kurator untuk Perbaikan dan Bugfix](../BK-02-Kurator-untuk-Perbaikan-dan-Bugfix/README.md)
