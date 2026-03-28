# BK-07: Template `.cursorrules` untuk Workspace Gabungan

## Gampangnya...

Kadang repo frontend dan backend terpisah di GitHub, tapi bertemu di satu workspace lokal. Template ini dibuat untuk konteks itu: AI harus bisa fokus per domain, tapi tetap tahu kapan perlu menyambungkan dua sisi.

---

## Konteks & Sejarah

Workspace gabungan sering memunculkan masalah:
- AI frontend ikut terlalu jauh ke backend,
- AI backend terlalu sibuk menilai UI,
- kontrak FE-BE tidak sinkron,
- artifact governance pecah antar repo.

Template ini menata aturan jembatannya.

---

## Cara Kerja

### Isi Minimal

- base persona
- discuss-first
- artifact governance lintas repo
- focus-first rule
- bridge rule untuk contract sync
- handoff antar domain

### Skeleton Ringkas

```text
# .cursorrules

## Focus Rule
Jika task frontend, fokus frontend dulu.
Jika task backend, fokus backend dulu.

## Bridge Rule
Jika perubahan menyentuh contract FE-BE, jelaskan dua sisi dampaknya.

## Artifact Governance
Gunakan artifact-map.md sebagai peta lintas artefak kerja.
```

---

## Kapan Digunakan

Gunakan template ini untuk workspace lokal yang menggabungkan lebih dari satu repo/domain.

---

## Cara Pakai

### Aturan Kunci

- satu task, satu fokus domain dulu
- bridge mode hanya aktif saat boundary benar-benar tersentuh
- handoff harus menyebut dampak ke domain lain

### Example Pack

Contoh yang lebih konkret ada di folder:
- [examples/example-cursorrules.md](./examples/example-cursorrules.md)
- [examples/example-artifact-map.md](./examples/example-artifact-map.md)
- [examples/example-tasks.md](./examples/example-tasks.md)
- [examples/example-tracker.md](./examples/example-tracker.md)

---

## Lab Praktek

**Skenario: frontend butuh field baru dari backend**

AI harus:
- fokus dulu ke contract change,
- menjelaskan dampak FE dan BE,
- lalu menyarankan urutan kerja yang aman.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Semua dibahas sekaligus** | AI kehilangan fokus | aktifkan focus-first rule |
| **Boundary tidak dijelaskan** | contract drift | tulis bridge rule eksplisit |
| **Handoff satu sisi saja** | domain lain tertinggal | wajib tulis dampak lintas repo |

---

## Materi Sebelumnya

- [BK-05: Template .cursorrules untuk Project Frontend](../BK-05-Template-cursorrules-untuk-Project-Frontend/README.md)
- [BK-06: Template .cursorrules untuk Project Backend](../BK-06-Template-cursorrules-untuk-Project-Backend/README.md)

