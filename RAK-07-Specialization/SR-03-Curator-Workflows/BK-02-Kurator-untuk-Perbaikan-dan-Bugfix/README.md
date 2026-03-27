# BK-02: Kurator untuk Perbaikan dan Bugfix

## Gampangnya...

Kurator ini adalah **montir diagnosis dan perbaikan**. Tujuannya bukan membuat sesuatu yang baru, tapi mengembalikan sistem ke perilaku yang seharusnya.

Kalau ada bug, error, atau perilaku yang aneh, kurator ini membantu AI fokus pada gejala, reproduksi, akar masalah, dan fix paling kecil yang aman.

---

## Konteks & Sejarah

Bugfix sering gagal bukan karena AI tidak pintar, tapi karena workflow-nya salah. AI sering:
- menebak akar masalah,
- memperbaiki area yang salah,
- membongkar terlalu luas,
- mengubah behavior lain tanpa sadar.

Repair Curator lahir untuk mencegah bugfix berubah menjadi eksperimen liar.

---

## Cara Kerja

### Alur Repair Curator

```mermaid
graph LR
    A[DISCUSS] --> B[ANALYZE]
    B --> C[DEBUG]
    C --> D[TEST]
    D --> E[EXECUTE]
    E --> F[REVIEW]
```

### Mode Utama

- `DISCUSS` untuk merumuskan gejala
- `ANALYZE` untuk memahami konteks teknis
- `DEBUG` untuk menelusuri akar masalah
- `TEST` untuk mereproduksi dan memvalidasi
- `EXECUTE` untuk menerapkan fix
- `REVIEW` untuk memeriksa efek samping

Mode pendukung:
- `DOCUMENT`

---

## Kapan Digunakan

Gunakan kurator ini ketika:
- ada error runtime,
- fitur yang tadinya jalan sekarang gagal,
- ada regresi,
- ada integrasi yang rusak,
- output tidak sesuai ekspektasi.

Jangan pakai kurator ini ketika:
- tugas utamanya membangun fitur baru,
- kamu sedang bersih-bersih struktur,
- yang dibutuhkan hanyalah rangkuman atau dokumentasi.

---

## Cara Pakai

### Template Prompt

```text
"Ada bug pada [fitur].
Gunakan Repair Curator.
Langkahmu:
1. Ringkas gejalanya
2. Jelaskan cara mereproduksi
3. Analisis root cause paling mungkin
4. Usulkan fix paling kecil yang aman
5. Sebutkan test/check yang harus dijalankan
Baru setelah itu eksekusi."
```

### Checklist Kurator

1. Gejalanya apa persis?
2. Bisa direproduksi atau tidak?
3. Root cause paling mungkin ada di mana?
4. Fix paling kecil yang aman apa?
5. Apa yang berisiko ikut rusak?
6. Setelah fix, test apa yang wajib dijalankan?

### Aturan Praktis

- jangan tebak bug tanpa reproduksi,
- utamakan fix minimal,
- hindari refactor besar saat kondisi sedang darurat,
- review efek samping sebelum menutup task.

### Kapan Harus Serahkan ke Kurator Lain

- Serahkan ke `Refactor Curator` jika bug sudah pulih dan pekerjaan berikutnya adalah merapikan struktur yang memang buruk.
- Serahkan ke `Documentation Curator` jika akar masalah, fix, dan efek samping perlu diarsipkan untuk sesi berikutnya.
- Jangan memaksa `Repair Curator` menangani pembersihan jangka panjang jika tujuan utamanya sudah bukan pemulihan.

---

## Lab Praktek

**Skenario: Login sering gagal**

Task:
"Kenapa login error saat traffic tinggi?"

Dengan Repair Curator, AI seharusnya:
- memperjelas gejala,
- mencari pola reproduksi,
- menganalisis bottleneck atau race condition,
- mengusulkan fix yang fokus pada akar masalah.

**Skenario: Endpoint 500**

Task:
"Endpoint checkout mengembalikan 500."

Kurator yang benar tidak langsung rewrite controller, tapi:
- menelusuri error,
- mencari titik pecah,
- lalu memberi fix seminimal mungkin.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **AI menebak bug** | Root cause disebut tanpa bukti | Minta reproduksi dan jejak analisis |
| **Fix terlalu besar** | Bug kecil berujung bongkar modul | Paksa fix minimal lebih dulu |
| **Repair berubah jadi refactor** | Sambil bugfix, AI ingin rapikan semuanya | Batasi scope pada pemulihan |
| **Tidak test sesudah fix** | Bug pindah tempat atau muncul efek samping | Jadikan `TEST` bagian wajib |

---

## Materi Selanjutnya

- [BK-03: Kurator untuk Refactor dan Pembenahan](../BK-03-Kurator-untuk-Refactor-dan-Pembenahan/README.md)
