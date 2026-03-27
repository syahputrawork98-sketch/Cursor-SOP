# BK-01: Peta Core Modes

Buku ini menjelaskan 10 mode inti yang resmi dipakai di repo Cursor-SOP. Tujuannya bukan sekadar menghafal nama, tetapi memahami arti praktisnya: mode ini dipakai kapan, kenapa dipakai, kapan jangan dipakai, dan apa risikonya kalau salah pilih.

---

## Gampangnya...

Core modes adalah toolbelt resmi repo ini. Mereka dipilih karena cukup ringkas untuk dipakai sehari-hari, tapi cukup kuat untuk menutup siklus kerja nyata dari diskusi sampai dokumentasi.

Kalau kamu memahami 10 mode ini dengan baik, kamu sudah punya fondasi kuat untuk membangun workflow sendiri tanpa harus tenggelam dalam ratusan istilah agentic yang tersebar di internet.

---

## Konteks & Sejarah

Repo ini tidak berangkat dari ide bahwa semua istilah di internet harus diadopsi mentah-mentah. Justru sebaliknya: daftar mode dipilih agar tetap operasional untuk kerja harian manusia + AI di proyek nyata.

Mode-mode seperti `DISCUSS`, `BLUEPRINT`, `PLAN`, dan `EXECUTE` muncul karena kebutuhan praktis:
- menahan AI agar tidak langsung koding,
- memaksa ada rancangan dulu,
- memecah kerja besar,
- dan menjaga ada audit serta dokumentasi setelah perubahan terjadi.

---

## Cara Kerja

### Peta 10 Core Modes

| Mode | Fungsi Inti | Fokus Utama |
|---|---|---|
| `DISCUSS` | Mematangkan arah | Klarifikasi dan pemahaman |
| `BLUEPRINT` | Merancang solusi | Bentuk dan struktur |
| `PLAN` | Memecah langkah | Urutan kerja |
| `ANALYZE` | Menyelidiki | Risiko, logika, trade-off |
| `EXECUTE` | Melakukan perubahan | Aksi nyata |
| `REVIEW` | Memeriksa hasil | Kualitas dan integritas |
| `DEBUG` | Menelusuri masalah | Root cause |
| `TEST` | Membuktikan kebenaran | Validasi |
| `REFACTOR` | Merapikan | Struktur tanpa ubah behavior inti |
| `DOCUMENT` | Menangkap pengetahuan | Warisan konteks |

### Penjelasan Detail per Mode

#### `DISCUSS`

Apa itu:
mode untuk berdiskusi, memperjelas tujuan, dan menyamakan pemahaman.

Kapan digunakan:
- saat ide masih mentah,
- saat requirement belum jelas,
- saat kamu ingin melihat opsi dan trade-off dulu.

Kapan jangan digunakan:
- saat arah sudah disetujui dan kamu benar-benar siap eksekusi,
- saat bug sudah jelas akar masalahnya dan kamu tinggal menerapkan fix kecil.

Kenapa penting:
karena AI yang terlalu cepat membantu sering justru salah arah.

Prompt contoh:
`Jangan coding dulu. Kita DISCUSS dulu. Jelaskan arah paling masuk akal untuk task ini.`

Mode tetangga:
sering menjadi pintu masuk ke `BLUEPRINT`, `PLAN`, atau `ANALYZE`.

#### `BLUEPRINT`

Apa itu:
mode untuk membuat rancangan solusi tanpa menulis implementasi nyata.

Kapan digunakan:
- saat membangun fitur baru,
- saat ingin merombak struktur besar,
- saat ingin melihat gambaran file/folder, arsitektur, atau alur.

Kapan jangan digunakan:
- saat bug kecil sudah jelas dan tidak butuh rancangan besar,
- saat task terlalu receh untuk dibuat blueprint formal.

Kenapa penting:
karena blueprint memisahkan ide solusi dari aksi implementasi.

Prompt contoh:
`Masuk ke BLUEPRINT. Rancang struktur solusi ini tanpa menulis kode.`

Mode tetangga:
sering diikuti `PLAN` atau langsung ke `EXECUTE` jika rancangan sudah disetujui.

#### `PLAN`

Apa itu:
mode untuk memecah pekerjaan menjadi langkah-langkah.

Kapan digunakan:
- saat task besar,
- saat banyak file akan terdampak,
- saat kamu ingin urutan kerja aman dan bertahap.

Kapan jangan digunakan:
- saat task sangat kecil,
- saat kamu hanya perlu klarifikasi ide, bukan daftar langkah.

Kenapa penting:
karena AI bisa sangat kuat di ide besar, tapi mudah liar saat urutan kerjanya tidak dibatasi.

Prompt contoh:
`Buat PLAN bertahap untuk task ini. Jangan coding dulu.`

Mode tetangga:
sering datang setelah `BLUEPRINT` dan sebelum `EXECUTE`.

#### `ANALYZE`

Apa itu:
mode untuk investigasi mendalam, audit logika, dan pembacaan trade-off.

Kapan digunakan:
- saat ada banyak risiko,
- saat keputusan desain mahal kalau salah,
- saat perlu memahami codebase atau sistem yang rumit.

Kapan jangan digunakan:
- saat kamu hanya perlu langkah praktis cepat,
- saat analisis sudah cukup dan hanya menunda kerja nyata.

Kenapa penting:
karena banyak kesalahan besar lahir dari keputusan yang diambil terlalu dangkal.

Prompt contoh:
`ANALYZE task ini secara mendalam. Fokus pada risiko, dependency, dan trade-off.`

Mode tetangga:
sering mendahului `EXECUTE`, `DEBUG`, atau `REFACTOR`.

#### `EXECUTE`

Apa itu:
mode untuk melakukan perubahan nyata.

Kapan digunakan:
- saat arah sudah disetujui,
- saat blueprint atau plan sudah cukup,
- saat kamu ingin AI benar-benar menulis atau mengubah artefak kerja.

Kapan jangan digunakan:
- saat requirement masih kabur,
- saat belum ada batasan scope,
- saat belum ada izin dari user.

Kenapa penting:
karena ini titik di mana biaya kesalahan menjadi nyata.

Prompt contoh:
`Baik, EXECUTE sekarang. Kerjakan satu tahap dulu dan laporkan hasilnya.`

Mode tetangga:
hampir selalu perlu ditutup dengan `REVIEW`, dan sering ditemani `TEST`.

#### `REVIEW`

Apa itu:
mode untuk memeriksa hasil kerja dan mencari kelemahan.

Kapan digunakan:
- setelah `EXECUTE`,
- saat audit,
- saat ingin mengecek bug, regresi, atau kualitas solusi.

Kapan jangan digunakan:
- saat belum ada artefak atau hasil yang mau diperiksa.

Kenapa penting:
karena kerja tanpa review mudah menghasilkan confident blunder.

Prompt contoh:
`Masuk ke REVIEW. Cari bug, regresi, dan area yang masih lemah.`

Mode tetangga:
sering menjadi gerbang kembali ke `DISCUSS`, `DEBUG`, atau `REFACTOR`.

#### `DEBUG`

Apa itu:
mode untuk menelusuri akar masalah.

Kapan digunakan:
- saat ada error,
- saat perilaku sistem aneh,
- saat perlu reproduksi dan root cause.

Kapan jangan digunakan:
- saat sebenarnya kamu sedang merancang solusi baru,
- saat kamu belum punya gejala yang jelas.

Kenapa penting:
karena tanpa debug, AI sering menebak penyebab lalu memperluas perubahan secara liar.

Prompt contoh:
`Masuk ke DEBUG. Reproduksi gejala, telusuri akar masalah, jangan tebak-tebakan.`

Mode tetangga:
sering berjalan bersama `TEST`, lalu baru `EXECUTE`.

#### `TEST`

Apa itu:
mode untuk membuktikan bahwa sesuatu benar atau tetap benar.

Kapan digunakan:
- setelah bugfix,
- setelah refactor,
- saat fitur penting butuh validasi,
- saat ingin punya bukti, bukan asumsi.

Kapan jangan digunakan:
- saat perubahan terlalu kecil dan tidak ada bentuk validasi yang masuk akal,
- saat sistem memang belum siap diuji.

Kenapa penting:
karena perasaan benar tidak sama dengan hasil yang tervalidasi.

Prompt contoh:
`Masuk ke TEST. Tentukan validasi minimum yang membuktikan solusi ini aman.`

Mode tetangga:
sering mendampingi `DEBUG`, `EXECUTE`, dan `REFACTOR`.

#### `REFACTOR`

Apa itu:
mode untuk merapikan atau membenahi struktur tanpa mengubah behavior inti.

Kapan digunakan:
- saat code smell berat,
- saat struktur kacau,
- saat ada technical debt.

Kapan jangan digunakan:
- saat kamu sebenarnya ingin mengubah fitur atau perilaku,
- saat bug utama belum dipulihkan.

Kenapa penting:
karena sistem yang jalan tapi tidak rapi akan mahal dirawat.

Prompt contoh:
`Masuk ke REFACTOR. Rapikan struktur ini tanpa mengubah behavior intinya.`

Mode tetangga:
sering didahului `ANALYZE` dan diakhiri `TEST`, `REVIEW`, serta `DOCUMENT`.

#### `DOCUMENT`

Apa itu:
mode untuk menulis pengetahuan agar tidak hilang.

Kapan digunakan:
- setelah task besar selesai,
- saat handover,
- saat update README, changelog, atau catatan keputusan.

Kapan jangan digunakan:
- saat pekerjaan inti belum jelas dan dokumentasi hanya akan mengabadikan kekacauan.

Kenapa penting:
karena AI sangat cepat menghasilkan kerja, tapi konteksnya juga cepat hilang kalau tidak ditangkap.

Prompt contoh:
`Masuk ke DOCUMENT. Ringkas perubahan, keputusan, dan next step untuk sesi berikutnya.`

Mode tetangga:
sering menjadi penutup setelah `REVIEW`, `REFACTOR`, atau workflow kurator.

---

## Kapan Digunakan

Pakai buku ini ketika kamu ingin benar-benar paham:
- arti detail tiap mode,
- beda antara mode yang kelihatannya mirip,
- alasan kenapa repo ini memakai 10 mode ini sebagai sistem inti,
- mode mana yang menjadi pintu masuk untuk jenis task tertentu.

Kalau kamu masih bingung "task saya harus masuk mode apa?", lanjutkan ke `BK-03`.

---

## Cara Pakai

### Ritual Belajar yang Disarankan

1. Pilih satu mode yang paling sering kamu pakai.
2. Baca tiga halnya dulu:
   - kapan dipakai,
   - kapan jangan dipakai,
   - prompt contohnya.
3. Cocokkan dengan task kamu sendiri minggu ini.
4. Baru bandingkan dengan mode tetangganya agar perbedaannya terasa.

### Aturan Emas

- `DISCUSS` bukan `ANALYZE`.
- `BLUEPRINT` bukan `PLAN`.
- `EXECUTE` bukan "sekadar lanjut".
- `REVIEW` bukan opsional.
- `DOCUMENT` bukan hiasan di akhir.

---

## Lab Praktek

**Task 1: "Saya mau bikin dashboard admin baru."**

Mode sehat:
`DISCUSS -> BLUEPRINT -> PLAN -> ANALYZE -> EXECUTE -> REVIEW -> DOCUMENT`

**Task 2: "Kenapa upload file sering gagal?"**

Mode sehat:
`DISCUSS -> ANALYZE -> DEBUG -> TEST -> EXECUTE -> REVIEW`

**Task 3: "Rapikan struktur folder fitur ini."**

Mode sehat:
`DISCUSS -> ANALYZE -> REFACTOR -> TEST -> REVIEW -> DOCUMENT`

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **`DISCUSS` dan `ANALYZE` tercampur** | Semua percakapan disebut analisis | Anggap `DISCUSS` untuk penyamaan arah, `ANALYZE` untuk investigasi dalam |
| **`BLUEPRINT` dan `PLAN` tertukar** | Rancangan struktur berubah jadi daftar langkah | Gunakan `BLUEPRINT` untuk bentuk solusi, `PLAN` untuk urutan kerja |
| **`EXECUTE` terlalu dini** | AI langsung mengubah banyak hal | Pastikan scope dan arah sudah disetujui |
| **`REVIEW` dilewati** | Perubahan selesai tapi kualitas tidak pernah diaudit | Jadikan `REVIEW` sebagai quality gate wajib |
| **`DOCUMENT` selalu ditunda** | Konteks hilang saat sesi berikutnya | Tutup task besar dengan dokumentasi minimum |
