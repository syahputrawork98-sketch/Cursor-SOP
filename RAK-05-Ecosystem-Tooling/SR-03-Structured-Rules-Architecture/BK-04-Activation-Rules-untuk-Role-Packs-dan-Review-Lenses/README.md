# BK-04: Activation Rules untuk Role Packs dan Review Lenses

## Gampangnya...

Role pack itu berguna, tapi kalau semuanya aktif sekaligus hasilnya malah kacau. Buku ini menjelaskan kapan lens builder, reviewer, atau domain lens sebaiknya aktif.

---

## Konteks & Sejarah

Begitu workflow makin matang, user ingin AI bisa:
- membangun,
- mereview,
- mengaudit,
- dan memakai lensa frontend/backend yang berbeda.

Masalahnya, kalau semua peran dipasang sekaligus di rules, AI kehilangan fokus.

---

## Cara Kerja

| Elemen | Fungsi |
|---|---|
| **Base Persona** | karakter umum AI |
| **Role Pack** | lensa kerja spesifik |
| **Review Lens** | kriteria audit spesifik |

### Aktivasi yang Sehat

- `BUILD` phase: aktifkan builder lens
- `REVIEW` phase: aktifkan reviewer lens
- `DEBUG` phase: aktifkan integrity lens

### Larangan

- jangan aktifkan semua reviewer sekaligus untuk task ringan
- jangan campur builder dan reviewer tanpa alasan

---

## Kapan Digunakan

Gunakan buku ini saat:
- ingin membedakan AI builder vs reviewer,
- ingin frontend dan backend punya lensa berbeda,
- takut role pack berubah jadi multi-agent chaos.

---

## Cara Pakai

### Contoh Pairing

- frontend execute: `UI Builder`
- frontend review: `UI Reviewer` + `Accessibility Lens`
- backend execute: `API Builder`
- backend review: `Backend Integrity Reviewer`

### Formula

`persona = default attitude`

`role pack = active specialization`

`review lens = quality filter`

---

## Lab Praktek

**Skenario: task UI baru**

Jangan langsung aktifkan builder, UI reviewer, UX reviewer, accessibility reviewer, dan performance lens bersama-sama. Mulai dari `UI Builder`, lalu pindah ke `UI Reviewer` dan `Accessibility Lens` saat review.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Role overload** | AI bingung dan verbose | aktifkan role seperlunya |
| **Builder dan reviewer bercampur** | output ragu-ragu | pisahkan activation by mode |
| **Role tidak terkait mode** | AI pakai lens yang salah | kaitkan role ke workflow phase |

---

## Materi Selanjutnya

- [BK-05: Template .cursorrules untuk Project Frontend](../BK-05-Template-cursorrules-untuk-Project-Frontend/README.md)
