# BK-04: GPT-OSS and Economy Models

## Gampangnya...

Model hemat bukan model "kelas dua". Dalam workflow yang sehat, model hemat justru menjaga agar kuota premium tetap hidup untuk pekerjaan yang memang penting.

Di lineup yang kamu gunakan, `GPT-OSS 120B Medium` berperan sebagai alat volume, draft, dan pekerjaan yang tidak mahal kalau salah.

---

## Konteks & Sejarah

User yang mentok kuota biasanya bukan kekurangan model premium. Mereka kekurangan **lapisan hemat** di workflow-nya. Semua task ditaruh ke model mahal, bahkan untuk:
- rewrite sederhana,
- draft awal,
- boilerplate,
- transformasi teks,
- eksperimen kasar.

Model economy hadir untuk menyerap pekerjaan semacam itu.

---

## Cara Kerja

### Posisi GPT-OSS 120B Medium

| Area | Posisi Umum |
|---|---|
| Draft awal | kuat |
| Rewrite | kuat |
| Boilerplate | kuat |
| Transformasi teks | kuat |
| Audit final | lemah |
| Debug kritis | kurang cocok |
| Arsitektur mahal | kurang cocok |

### Prinsip Umum

- model hemat cocok untuk volume,
- model hemat butuh guardrail yang lebih ketat,
- model hemat bukan tempat terbaik untuk keputusan mahal.

---

## Kapan Digunakan

Gunakan `GPT-OSS 120B Medium` ketika:
- kamu sedang drafting,
- kamu butuh rewrite cepat,
- kamu sedang membuat boilerplate,
- kamu ingin eksperimen awal,
- kamu ingin menjaga jatah premium tetap utuh.

Jangan gunakan model ini ketika:
- task sangat ambigu,
- salah sedikit bisa mahal,
- kamu sedang audit final,
- kamu sedang debug yang sensitif.

---

## Cara Pakai

### Aturan Praktis

- pakai untuk pekerjaan volume tinggi,
- beri instruksi lebih eksplisit,
- jangan serahkan keputusan arsitektur kritis ke model economy,
- naikkan hasil draft ke model premium jika perlu review akhir.

### Template Prompt

```text
"Kerjakan ini sebagai draft awal.
Fokus pada kecepatan dan struktur kasar.
Jika ada bagian yang berisiko atau butuh keputusan besar, tandai agar nanti direview di model premium."
```

---

## Lab Praktek

**Skenario: Draft dulu, review belakangan**

Pakai `GPT-OSS 120B Medium` untuk:
- menulis draft awal,
- membuat struktur outline,
- membuat boilerplate.

Setelah itu:
- naikkan ke model premium untuk review, reasoning, atau final polish jika memang perlu.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Model hemat diremehkan** | Tidak pernah dipakai | Jadikan dia lapisan volume kerja |
| **Terlalu percaya model hemat** | Keputusan mahal dibuat di model economy | Batasi ke draft dan task volume |
| **Tidak ada handoff ke premium** | Draft awal dianggap final | Gunakan premium untuk final review jika task penting |

---

## Materi Selanjutnya

- [BK-05: Quota Strategy and Task Routing](../BK-05-Quota-Strategy-and-Task-Routing/README.md)
