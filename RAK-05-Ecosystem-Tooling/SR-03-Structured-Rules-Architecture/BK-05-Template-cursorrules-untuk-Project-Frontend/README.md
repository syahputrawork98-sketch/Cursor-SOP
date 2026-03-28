# BK-05: Template `.cursorrules` untuk Project Frontend

## Gampangnya...

Project frontend butuh AI yang peka ke tampilan, struktur komponen, responsiveness, dan polish. Template ini menata itu tanpa menjadikan frontend sebagai mode inti baru.

---

## Konteks & Sejarah

Tanpa template frontend yang jelas, AI sering:
- terlalu fokus ke logika tapi lupa polish,
- terlalu cepat coding tanpa blueprint visual,
- atau mereview UI dengan lensa backend.

---

## Cara Kerja

### Isi Minimal

- base persona
- discuss-first
- artifact governance
- `UI Builder`
- `UI Reviewer`
- accessibility and responsiveness gates

### Skeleton Ringkas

```text
# .cursorrules

## Default
Mode default adalah DISCUSS.

## Artifact Governance
Jika artifact-map.md tersedia, baca dulu.

## Frontend Build Lens
Fokus pada layout, hierarchy, responsiveness, dan component clarity.

## Frontend Review Lens
Periksa visual consistency, accessibility, polish, dan mobile behavior.
```

---

## Kapan Digunakan

Gunakan template ini untuk repo frontend atau workspace yang sedang fokus penuh di UI.

---

## Cara Pakai

### Review Gates

- cek hierarchy visual
- cek mobile responsiveness
- cek consistency spacing
- cek accessibility minimum

### Example Pack

Contoh yang lebih konkret ada di folder:
- [examples/example-cursorrules.md](./examples/example-cursorrules.md)
- [examples/example-artifact-map.md](./examples/example-artifact-map.md)
- [examples/example-tasks.md](./examples/example-tasks.md)
- [examples/example-tracker.md](./examples/example-tracker.md)

---

## Lab Praktek

**Skenario: dashboard admin baru**

Gunakan builder lens saat implementasi, lalu aktifkan reviewer lens saat audit visual dan usability.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **UI dikerjakan seperti backend** | tampilan terasa kaku | aktifkan frontend lens |
| **Review visual tidak ada** | UI selesai tapi belum halus | tambahkan reviewer gates |
| **Mobile diabaikan** | layout pecah di layar kecil | jadikan responsiveness gate wajib |

---

## Materi Selanjutnya

- [BK-06: Template .cursorrules untuk Project Backend](../BK-06-Template-cursorrules-untuk-Project-Backend/README.md)

