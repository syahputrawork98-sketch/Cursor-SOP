# BK-03: Artifact Governance di Dalam `.cursorrules`

## Gampangnya...

`.cursorrules` tidak boleh menyimpan semua progres kerja. Tugasnya adalah memberi hukum dan arah baca. Sementara `artifact-map.md`, `tasks.md`, dan `tracker.md` memegang struktur kerja yang hidup.

---

## Konteks & Sejarah

Begitu artifact governance masuk ke workflow, banyak user mulai bingung:
- apa tugas `.cursorrules`?
- apa tugas `artifact-map.md`?
- apa tugas `tracker.md`?

Kalau ini tidak dibedakan, AI akan membaca semua file sebagai otoritas setara.

---

## Cara Kerja

| File | Peran |
|---|---|
| **`.cursorrules`** | hukum perilaku |
| **`artifact-map.md`** | peta sumber kebenaran |
| **`blueprint.md`** | arah solusi |
| **`implementation-plan.md`** | urutan fase |
| **`tasks.md`** | checklist kerja |
| **`tracker.md`** | status aktif |
| **`handover.md`** | ringkasan sesi |

### Formula

`.cursorrules = law`

`artifact-map.md = navigation`

`tasks.md + tracker.md = current execution state`

---

## Kapan Digunakan

Gunakan buku ini saat:
- proyekmu sudah memakai artefak terpisah,
- AI mulai bingung mana file yang authoritative,
- kamu ingin `.cursorrules` memerintah tanpa menampung semua isi kerja.

---

## Cara Pakai

### Aturan Minimal di `.cursorrules`

- baca `artifact-map.md` jika tersedia
- gunakan `tracker.md` dan `tasks.md` untuk progres aktif
- jangan pakai `handover.md` sebagai penentu task aktif
- jika file bentrok, laporkan mismatch dulu

### Yang Tidak Boleh

- checklist hidup di `.cursorrules`
- progres harian ditaruh di rules
- handover ditulis di rules

---

## Lab Praktek

**Skenario: AI membaca chat history dan tracker sekaligus**

Dengan artifact governance yang baik, `.cursorrules` akan memerintahkan AI untuk mempercayai `artifact-map.md`, lalu `tracker.md`, bukan obrolan terakhir secara buta.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Rules jadi gudang progres** | `.cursorrules` makin panjang | pindahkan state ke artefak |
| **Artifact map diabaikan** | AI balik baca chat history | tulis reading order secara eksplisit |
| **Tracker tidak dianggap authoritative** | progres melompat | kaitkan tracker ke conflict rules |

---

## Materi Selanjutnya

- [BK-04: Activation Rules untuk Role Packs dan Review Lenses](../BK-04-Activation-Rules-untuk-Role-Packs-dan-Review-Lenses/README.md)
