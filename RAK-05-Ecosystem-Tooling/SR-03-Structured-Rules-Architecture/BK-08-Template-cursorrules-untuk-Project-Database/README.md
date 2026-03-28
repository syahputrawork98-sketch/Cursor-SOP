# BK-08: Template `.cursorrules` untuk Project Database

## Gampangnya...

Project database butuh AI yang lebih hati-hati daripada backend biasa. Template ini dibuat untuk menajamkan disiplin pada schema, migration, data integrity, rollback thinking, dan query safety.

---

## Konteks & Sejarah

Tanpa template database yang jelas, AI sering:
- menganggap perubahan schema sebagai edit biasa,
- meremehkan dampak migration,
- fokus ke query tapi lupa rollback,
- atau mengubah struktur data tanpa audit consumer.

Karena itu, database tidak cukup hanya dianggap bagian kecil dari backend. Ia butuh guardrails sendiri.

---

## Cara Kerja

### Isi Minimal

- base persona
- discuss-first
- artifact governance
- `Schema Builder`
- `Database Integrity Reviewer`
- migration, rollback, destructive change, dan query safety gates

### Skeleton Ringkas

```text
# .cursorrules

## Default
Mode default adalah DISCUSS.

## Artifact Governance
Jika artifact-map.md tersedia, baca dulu.

## Database Build Lens
Fokus pada schema clarity, migration safety, dan query intent.

## Database Review Lens
Periksa destructive risk, rollback path, data integrity, dan consumer impact.
```

---

## Kapan Digunakan

Gunakan template ini untuk repo atau folder kerja yang fokus pada:
- schema database,
- migration,
- query layer,
- atau sinkronisasi data model dengan aplikasi.

---

## Cara Pakai

### Review Gates

- cek destructive change risk
- cek migration order
- cek rollback path
- cek data integrity dan consumer impact

### Example Pack

Contoh yang lebih konkret ada di folder:
- [examples/example-cursorrules.md](./examples/example-cursorrules.md)
- [examples/example-artifact-map.md](./examples/example-artifact-map.md)
- [examples/example-tasks.md](./examples/example-tasks.md)
- [examples/example-tracker.md](./examples/example-tracker.md)

---

## Lab Praktek

**Skenario: menambah kolom baru dan backfill data**

Gunakan build lens saat merancang schema change dan migration order, lalu reviewer lens saat audit rollback path, consumer impact, dan query compatibility.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Schema change dianggap ringan** | migration dibuat tanpa audit | jadikan migration gate wajib |
| **Rollback tidak dipikirkan** | perubahan sulit dibatalkan | tulis rollback path sebelum execute |
| **Consumer impact tidak dicatat** | aplikasi lain tiba-tiba rusak | audit consumer sebelum tutup task |
| **Query diubah tanpa integrity check** | data salah atau lambat | aktifkan integrity reviewer dan query safety gate |

---

## Materi Sebelumnya

- [BK-06: Template .cursorrules untuk Project Backend](../BK-06-Template-cursorrules-untuk-Project-Backend/README.md)
- [BK-07: Template .cursorrules untuk Workspace Gabungan](../BK-07-Template-cursorrules-untuk-Workspace-Gabungan/README.md)
