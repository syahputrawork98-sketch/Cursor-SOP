# BK-04: Kurator untuk Dokumentasi dan Handover

## Gampangnya...

Kurator ini adalah **penulis buku servis proyek**. Tugasnya menangkap hasil kerja, keputusan penting, file yang berubah, dan hal yang masih menggantung agar sesi berikutnya tidak mulai dari nol lagi.

Kalau semua pekerjaan selesai tapi tidak ada catatan yang berguna, maka pengetahuan itu praktis hilang. Documentation Curator ada untuk mencegah kebocoran memori kerja seperti itu.

---

## Konteks & Sejarah

Dalam kerja bareng AI, banyak nilai hilang bukan karena implementasinya buruk, tetapi karena:
- keputusan penting tidak dicatat,
- perubahan tidak diringkas,
- sesi panjang berakhir tanpa handover,
- dokumen hidup tidak pernah diperbarui.

Documentation Curator lahir untuk mengubah hasil kerja menjadi aset jangka panjang.

---

## Cara Kerja

### Alur Documentation Curator

```mermaid
graph LR
    A[DISCUSS] --> B[ANALYZE]
    B --> C[DOCUMENT]
    C --> D[REVIEW]
```

### Mode Utama

- `DISCUSS` untuk memahami tujuan dokumentasi
- `ANALYZE` untuk memilih hal yang benar-benar penting
- `DOCUMENT` untuk menulis ringkasan atau artefak pengetahuan
- `REVIEW` untuk mengecek kejelasan dan kegunaan

Mode pendukung:
- `PLAN`

---

## Kapan Digunakan

Gunakan kurator ini ketika:
- menutup sesi kerja,
- membuat handover,
- memperbarui changelog,
- menulis session notes,
- meringkas keputusan arsitektural,
- memperbarui README atau SOP.

Jangan pakai kurator ini ketika:
- bug bahkan belum dipahami,
- arsitektur fitur baru belum jelas,
- refactor belum selesai,
- task inti masih berada di creation, repair, atau refactor.

---

## Cara Pakai

### Template Prompt

```text
"Gunakan Documentation Curator.
Ringkas sesi kerja ini dalam format:
1. Apa yang dikerjakan
2. File yang berubah
3. Keputusan penting
4. Masalah yang belum selesai
5. Hal yang harus diingat sesi berikutnya"
```

### Checklist Kurator

1. Apa yang berubah?
2. Kenapa perubahan itu dilakukan?
3. File apa saja yang tersentuh?
4. Apa keputusan pentingnya?
5. Apa yang belum selesai?
6. Siapa pembaca dokumen ini?

### Aturan Praktis

- tulis untuk pembaca sesi berikutnya, bukan untuk pamer,
- utamakan keputusan dan konsekuensi,
- ringkas tapi jangan kabur,
- selalu sebutkan hal yang belum selesai.

### Kapan Harus Serahkan ke Kurator Lain

- Serahkan kembali ke `Creation`, `Repair`, atau `Refactor` jika dokumentasi membuka fakta bahwa pekerjaan inti sebenarnya belum selesai.
- `Documentation Curator` seharusnya datang di akhir workflow utama, bukan menggantikannya terlalu dini.

---

## Lab Praktek

**Skenario: Menutup sesi debug panjang**

Task:
"Ringkas hasil debugging hari ini agar besok tidak mulai dari nol."

Dengan Documentation Curator, AI seharusnya:
- merangkum gejala awal,
- menjelaskan fix yang dicoba,
- menulis hasil final,
- mencatat sisa masalah jika ada.

**Skenario: Setelah refactor**

Task:
"Buat handover setelah struktur folder berubah."

Kurator yang benar akan menangkap:
- alasan refactor,
- area yang berubah,
- struktur baru,
- hal yang perlu diperhatikan di sesi berikutnya.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Dokumentasi terlalu panjang** | Banyak teks, sedikit nilai | Fokus pada keputusan, perubahan, dan next step |
| **Dokumentasi terlalu kabur** | Ringkas tapi tidak bisa dipakai ulang | Sebutkan file, alasan, dan status |
| **Handover tanpa sisa masalah** | Sesi berikutnya tetap bingung harus mulai dari mana | Selalu tulis unresolved items |
| **Dokumentasi ditunda terus** | Pengetahuan hilang setelah sesi tutup | Jadikan dokumentasi sebagai penutup standar |

---

## Materi Sebelumnya

- [BK-01: Kurator untuk Project Baru](../BK-01-Kurator-untuk-Project-Baru/README.md)
