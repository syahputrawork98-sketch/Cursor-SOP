# BK-04: Mode vs Curator Workflow

Buku ini meluruskan satu kebingungan yang sangat umum: mode dasar dan curator workflow itu bukan hal yang sama. Mode adalah alat dasar. Curator adalah rangkaian alat yang dipilih berdasarkan jenis kerja.

---

## Gampangnya...

Kalau mode itu seperti obeng, tang, dan kunci pas, maka curator adalah kotak alat yang kamu ambil untuk pekerjaan tertentu. Kamu tidak membawa semua alat dengan urutan acak. Kamu memilih kombinasi alat yang pas untuk membangun, memperbaiki, merapikan, atau mendokumentasikan.

Jadi `Creation`, `Repair`, `Refactor`, dan `Documentation` bukan mode baru. Mereka adalah paket workflow yang dirakit dari mode-mode dasar.

---

## Konteks & Sejarah

Begitu user mulai memahami mode dasar, biasanya muncul keinginan untuk membuat template kerja yang lebih siap pakai. Dari situ lahir konsep kurator workflow:
- tidak semua task perlu urutan mode yang sama,
- bugfix tidak boleh diperlakukan seperti project baru,
- refactor tidak boleh bercampur dengan diagnosis bug,
- dokumentasi tidak boleh selalu tertinggal.

Maka muncullah layer di atas mode: **curator workflow**.

---

## Cara Kerja

### Definisi yang Harus Dipisahkan

| Istilah | Makna | Contoh |
|---|---|---|
| **Mode** | Posisi kerja dasar AI | `DISCUSS`, `PLAN`, `EXECUTE` |
| **Workflow** | Urutan kerja dari beberapa langkah | `DISCUSS -> PLAN -> EXECUTE -> REVIEW` |
| **Curator** | Workflow terkurasi untuk jenis kerja tertentu | `Creation Curator`, `Repair Curator` |

### Empat Curator Utama

| Curator | Fungsi | Rangkaian Mode |
|---|---|---|
| `Creation` | Membangun hal baru | `DISCUSS -> BLUEPRINT -> PLAN -> ANALYZE -> EXECUTE -> REVIEW` |
| `Repair` | Memperbaiki yang rusak | `DISCUSS -> ANALYZE -> DEBUG -> TEST -> EXECUTE -> REVIEW` |
| `Refactor` | Merapikan tanpa ubah behavior | `DISCUSS -> ANALYZE -> REFACTOR -> TEST -> REVIEW -> DOCUMENT` |
| `Documentation` | Menangkap pengetahuan dan handover | `DISCUSS -> ANALYZE -> DOCUMENT -> REVIEW` |

### Cara Membuat Curator Baru

Sebuah curator baru layak dibuat jika:
- ada pola kerja yang berulang,
- urutan modenya cukup stabil,
- ada nilai praktis saat workflow itu diberi nama,
- dan dia tidak hanya menduplikasi curator yang sudah ada.

### Rumah Utama Curator

Penjelasan lengkap tentang curator workflow hidup di:
- [SR-03: Curator Workflows](/i:/Workspace/Workspace-Syahputrawork/08-AI-Orchestration-Hubs/Cursor-SOP/RAK-07-Specialization/SR-03-Curator-Workflows/README.md)

Buku ini berfungsi sebagai jembatan konsep. Rumah operasional curator tetap berada di `RAK-07`.

---

## Kapan Digunakan

Pakai buku ini saat:
- kamu bingung apakah butuh mode baru atau cukup workflow baru,
- kamu ingin membuat kurator untuk website, backend, atau project tertentu,
- kamu ingin tahu bagaimana mode dasar dirangkai menjadi operasi kerja yang bisa dipakai ulang.

Kalau kamu hanya ingin tahu definisi mode, balik ke `BK-01`. Kalau kamu ingin tahu kapan memakai mode, baca `BK-03`.
Kalau kamu ingin mendalami template dan pola curator yang sudah jadi, lanjut ke [SR-03: Curator Workflows](/i:/Workspace/Workspace-Syahputrawork/08-AI-Orchestration-Hubs/Cursor-SOP/RAK-07-Specialization/SR-03-Curator-Workflows/README.md).

---

## Cara Pakai

### Aturan Emas

- Jika yang berubah hanya **urutan pemakaian mode**, biasanya kamu butuh curator, bukan mode baru.
- Jika yang muncul adalah **jenis kerja yang betul-betul berbeda**, curator layak dibuat.
- Jika istilah baru hanya menjelaskan mekanisme, misalnya `tool use`, mungkin kamu belum butuh mode atau curator baru.

### Contoh 1: Curator untuk Website Baru

Bukan mode baru, melainkan varian dari `Creation Curator`.

Rangkaian sehat:
`DISCUSS -> BLUEPRINT -> PLAN -> ANALYZE -> EXECUTE -> REVIEW -> DOCUMENT`

### Contoh 2: Curator untuk Pembenahan Website Lama

Bukan mode baru, melainkan varian dari `Repair` atau `Refactor`, tergantung tujuan dominan.

Kalau fokusnya memulihkan bug:
`Repair Curator`

Kalau fokusnya merapikan struktur:
`Refactor Curator`

### Kapan Tidak Perlu Curator Baru

Tidak perlu membuat curator baru jika:
- perbedaannya hanya kosmetik,
- urutan modenya sama dengan curator lama,
- atau ia hanya menyalin satu curator lama dengan nama domain berbeda.

---

## Lab Praktek

**Task: "Saya ingin membuat workflow AI khusus untuk website baru."**

Analisis:
- ini bukan mode baru,
- ini adalah bentuk domain-specific dari `Creation Curator`.

**Task: "Saya ingin mode `Website Build`."**

Koreksi:
- kemungkinan besar yang kamu butuhkan bukan mode baru,
- melainkan **curator atau template workflow** berbasis mode yang sudah ada.

**Task: "Saya ingin mode untuk mengelola konteks panjang lintas sesi."**

Analisis:
- ini bisa jadi bukan curator,
- tetapi kandidat `extended mode` seperti `MEMORY / CONTEXT MANAGEMENT`.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Curator dianggap mode baru** | Daftar mode membengkak tanpa perlu | Pisahkan level mode dan workflow |
| **Semua domain dibuat curator baru** | Muncul banyak duplikasi | Gunakan curator generik, lalu turunkan ke contoh domain |
| **Mode baru dibuat padahal hanya urutan** | Sistem jadi kacau | Jika inti masalahnya urutan, buat workflow, bukan mode |
| **Curator baru tidak punya alasan kuat** | Sulit dibedakan dari curator lama | Pastikan ada perbedaan tujuan dan rangkaian mode |
