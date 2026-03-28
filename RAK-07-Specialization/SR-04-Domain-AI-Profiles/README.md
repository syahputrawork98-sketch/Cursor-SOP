# SR-04: Domain AI Profiles

Sub-rak ini membahas cara membuat AI bekerja dengan identitas spesialis per domain, tanpa mengubah `core modes` menjadi taxonomy baru. Fokusnya adalah memberi lensa kerja yang berbeda untuk frontend, backend, database, dan workspace lintas domain.

> Status per 2026-03-28.
> Sub-rak ini dibuka sebagai jembatan antara arsitektur rules di `RAK-05` dan workflow spesialis di `RAK-07`.

---

## Gampangnya...

Kalau `RAK-05` mengajari bagaimana menulis `.cursorrules`, maka sub-rak ini mengajari bagaimana AI berpikir sebagai spesialis domain tertentu. Jadi yang dibedakan di sini bukan mode inti, melainkan fokus, kualitas audit, dan kebiasaan kerja per domain.

Anggap saja ini seperti memilih profesi di dalam satu organisasi. Orangnya sama-sama bekerja di bawah aturan umum, tetapi frontend, backend, dan database tetap punya cara melihat risiko yang berbeda.

---

## Konteks & Sejarah

Saat workflow AI makin matang, muncul kebutuhan yang tidak cukup dijawab oleh rules umum saja:
- AI frontend perlu peka ke hierarchy visual dan polish,
- AI backend perlu disiplin pada contract dan validation,
- AI database perlu sangat hati-hati pada schema, migration, dan rollback,
- workspace lintas domain perlu tahu kapan fokus satu sisi dulu dan kapan harus menjembatani dua sisi.

Kalau semua domain ini diperlakukan sama, AI akan memakai lensa yang terlalu datar. Hasilnya sering kabur: review visual dilakukan seperti audit API, atau schema change dianggap seperti edit kecil biasa.

---

## Cara Kerja

### Prinsip Domain Profile

| Elemen | Fungsi |
|---|---|
| **Base Persona** | karakter dasar AI yang tetap konsisten lintas proyek |
| **Domain Lens** | fokus utama saat membangun dan menilai hasil |
| **Review Priorities** | aspek kualitas yang harus diaudit lebih dulu |
| **Boundary Awareness** | titik sensitif yang tidak boleh dianggap sepele |
| **Handoff Pattern** | cara melaporkan dampak ke domain lain |

### Hubungan dengan Rak Lain

| Rak | Peran |
|---|---|
| **RAK-02** | rumah `core modes` universal |
| **RAK-05** | rumah `.cursorrules` dan rules architecture |
| **RAK-07 / SR-04** | rumah identitas spesialis per domain |
| **RAK-08** | rumah sinkronisasi lintas domain dan lintas repo |

### Urutan Baca yang Disarankan

1. Baca template rules domain di `RAK-05` jika belum ada baseline `.cursorrules`.
2. Masuk ke profile domain yang sedang kamu pakai.
3. Gunakan profile itu sebagai lensa saat `DISCUSS`, `PLAN`, `EXECUTE`, dan `REVIEW`.
4. Jika perubahan menyentuh domain lain, sambungkan handoff ke `RAK-08`.

---

## Kapan Digunakan

Gunakan sub-rak ini saat:
- kamu merasa AI sudah punya rules, tapi fokus domainnya masih kabur,
- kamu ingin membedakan cara audit frontend, backend, dan database,
- kamu bekerja di beberapa repo/domain yang bertemu dalam satu workspace,
- kamu ingin AI punya kebiasaan review yang sesuai dengan jenis resikonya.

---

## Cara Pakai

### Aturan Praktis

- jangan buat domain profile sebagai `core mode` baru,
- pakai satu profile utama per task aktif,
- aktifkan bridge lintas domain hanya saat boundary benar-benar tersentuh,
- biarkan rules hidup di `.cursorrules`, tapi biarkan profile hidup di workflow berpikir dan review.

### Formula Ringkas

`rules = hukum`

`domain profile = lensa kerja`

`tasks + tracker = status aktual`

---

## Lab Praktek

**Skenario: perubahan schema untuk dashboard baru**

- backend saja tidak cukup, karena dampaknya menyentuh data model,
- frontend saja tidak cukup, karena resiko utamanya ada di migration dan consumer,
- maka gunakan `Database AI Profile` untuk fase perubahan data,
- lalu serahkan dampak UI atau API ke domain lain melalui handoff yang jelas.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Domain profile dianggap mode baru** | taxonomy makin bengkak | pertahankan core modes di RAK-02 |
| **Satu task memakai semua profile sekaligus** | AI kehilangan fokus | pilih satu profile dominan per task |
| **Rules dan profile bercampur** | `.cursorrules` menjadi terlalu berat | simpan hukum di RAK-05, simpan lensa di SR-04 |
| **Boundary domain diabaikan** | handoff antar domain kabur | wajib tulis dampak ke domain lain |

---

## Buku Utama

- [BK-01: Database AI Profile](./BK-01-Database-AI-Profile/README.md)
