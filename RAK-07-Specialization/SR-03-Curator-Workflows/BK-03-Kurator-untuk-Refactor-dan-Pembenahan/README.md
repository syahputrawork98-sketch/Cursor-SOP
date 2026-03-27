# BK-03: Kurator untuk Refactor dan Pembenahan

## Gampangnya...

Kurator ini adalah **tukang rapikan mesin tanpa mengubah fungsi mobilnya**. Fokusnya bukan menciptakan sesuatu yang baru dan bukan memulihkan bug akut, tetapi membenahi struktur supaya sistem lebih sehat dirawat.

Kalau kode mulai penuh duplikasi, nama file membingungkan, dan struktur makin susah dipelihara, kurator inilah yang paling tepat dipakai.

---

## Konteks & Sejarah

Refactor yang buruk sering menyamar sebagai "rapi-rapi". Padahal, tanpa batas yang jelas, refactor bisa:
- mengubah behavior diam-diam,
- membuka bug baru,
- meluas ke seluruh proyek,
- membuat user kehilangan jejak keputusan.

Refactor Curator dibuat agar pembenahan tetap disiplin: rapi, tapi tidak liar.

---

## Cara Kerja

### Alur Refactor Curator

```mermaid
graph LR
    A[DISCUSS] --> B[ANALYZE]
    B --> C[PLAN]
    C --> D[REFACTOR]
    D --> E[TEST]
    E --> F[REVIEW]
    F --> G[DOCUMENT]
```

### Mode Utama

- `DISCUSS` untuk menyepakati tujuan pembenahan
- `ANALYZE` untuk memetakan kekacauan
- `PLAN` untuk membagi refactor menjadi tahap aman
- `REFACTOR` untuk melakukan pembenahan
- `TEST` untuk menjaga perilaku tetap sama
- `REVIEW` untuk memeriksa kualitas hasil
- `DOCUMENT` untuk mencatat struktur baru

---

## Kapan Digunakan

Gunakan kurator ini ketika:
- ada code smell,
- banyak duplikasi,
- struktur folder kacau,
- penamaan tidak konsisten,
- satu file terlalu besar,
- technical debt mulai menghambat.

Jangan pakai kurator ini ketika:
- ada bug kritis yang harus dipulihkan cepat,
- sistem baru bahkan belum punya bentuk,
- tugasmu cuma butuh handover atau dokumentasi.

---

## Cara Pakai

### Template Prompt

```text
"Saya ingin merapikan [bagian sistem] tanpa mengubah perilakunya.
Gunakan Refactor Curator.
Sebelum mulai:
1. Identifikasi masalah struktur saat ini
2. Jelaskan apa yang tidak boleh berubah
3. Buat rencana refactor bertahap
4. Tentukan test/check yang harus dipakai
Baru setelah itu lakukan refactor."
```

### Checklist Kurator

1. Apa yang jelek sekarang?
2. Apa target rapinya?
3. Behavior apa yang tidak boleh berubah?
4. Tahap refactor paling aman apa?
5. Bukti apa yang menunjukkan perilaku tetap sama?
6. Apa yang harus didokumentasikan setelah refactor?

### Aturan Praktis

- nyatakan batas refactor sejak awal,
- refactor bertahap, jangan borong semuanya sekaligus,
- selalu sertakan pembuktian behavior tidak berubah,
- dokumentasikan struktur baru agar tidak hilang maknanya.

### Kapan Harus Serahkan ke Kurator Lain

- Serahkan ke `Repair Curator` jika selama refactor ternyata ditemukan bug aktif yang harus dipulihkan lebih dulu.
- Serahkan ke `Documentation Curator` saat hasil pembenahan sudah final dan perlu dibuat handover.
- Jangan menyamarkan rewrite fitur baru sebagai refactor jika perilakunya memang ikut berubah.

---

## Lab Praktek

**Skenario: Struktur feature berantakan**

Task:
"Rapikan folder feature ini tanpa mengubah behavior."

Dengan Refactor Curator, AI seharusnya:
- mengidentifikasi duplikasi dan kekacauan,
- menentukan target struktur yang lebih bersih,
- memecah perubahan menjadi tahap kecil,
- memastikan behavior tetap sama.

**Skenario: File terlalu besar**

Task:
"Pecah file ini jadi modul-modul kecil tanpa ubah flow."

Kurator yang benar akan menjaga batas: pembenahan struktur iya, perubahan logika tidak.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Refactor diam-diam ubah behavior** | Output berubah padahal niatnya hanya rapi-rapi | Tegaskan apa yang tidak boleh berubah |
| **Ruang refactor terlalu luas** | Satu task merembet ke mana-mana | Batasi scope dan buat tahap |
| **Tidak ada test pembanding** | Sulit membuktikan behavior tetap sama | Wajib tentukan check sebelum refactor |
| **Dokumentasi hilang** | Struktur baru rapi tapi orang lain bingung | Tutup workflow dengan `DOCUMENT` |

---

## Materi Selanjutnya

- [BK-04: Kurator untuk Dokumentasi dan Handover](../BK-04-Kurator-untuk-Dokumentasi-dan-Handover/README.md)
