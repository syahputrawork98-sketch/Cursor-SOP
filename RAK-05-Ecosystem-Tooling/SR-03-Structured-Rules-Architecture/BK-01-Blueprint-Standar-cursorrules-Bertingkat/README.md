# BK-01: Blueprint Standar `.cursorrules` Bertingkat

## Gampangnya...

`.cursorrules` yang sehat bukan sekadar kumpulan larangan dan pengingat. Ia sebaiknya disusun bertingkat agar AI tahu mana hukum dasar, mana aturan proyek, dan mana penyesuaian domain.

---

## Konteks & Sejarah

Saat rules masih sedikit, satu layer sering cukup. Tapi ketika rules bertambah, file yang sama mulai menampung:
- persona,
- mode,
- stack,
- batas eksekusi,
- artifact governance,
- role review,
- dan override domain.

Tanpa struktur bertingkat, rules itu cepat berubah jadi kabut.

---

## Cara Kerja

### Blueprint Lapisan

| Lapisan | Isi Umum |
|---|---|
| **Base Persona** | karakter dan sikap default AI |
| **Core Workflow Rules** | discuss-first, mode discipline, anti-offside |
| **Artifact Governance** | hubungan rules dengan `artifact-map.md` dan artefak kerja |
| **Role Activation** | kapan builder/reviewer lens aktif |
| **Review Gates** | syarat sebelum dianggap selesai |
| **Local Overrides** | penyesuaian repo atau workspace |

### Diagram Sederhana

```text
Base Persona
  -> Core Workflow Rules
    -> Artifact Governance
      -> Role Activation
        -> Review Gates
          -> Local Overrides
```

---

## Kapan Digunakan

Gunakan blueprint ini saat:
- mulai membuat `.cursorrules` baru,
- merasa rules lama makin penuh,
- ingin membuat standar global yang bisa diwariskan ke banyak proyek.

---

## Cara Pakai

### Aturan Praktis

1. Tulis persona dasar terlebih dulu.
2. Tulis aturan workflow universal.
3. Tambahkan artifact governance.
4. Baru masukkan role activation dan review gates.
5. Simpan override spesifik di bagian paling bawah.

### Pola Ringkas

```text
1. Who am I?
2. How do I work?
3. What files are authoritative?
4. What roles can activate?
5. What quality gates must pass?
6. What local overrides apply here?
```

---

## Lab Praktek

**Skenario: membuat rules baru untuk repo frontend**

Kalau kamu langsung menulis larangan per file tanpa pondasi persona dan workflow, rules akan terasa random. Dengan blueprint ini, kamu menulis fondasi dulu, baru detailnya.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Mulai dari larangan kecil** | rules terasa reaktif | mulai dari lapisan besar dulu |
| **Override terlalu atas** | local rules merusak hukum dasar | letakkan override di bawah |
| **Role masuk terlalu dini** | file rules jadi ramai | aktifkan role setelah fondasi jelas |

---

## Materi Selanjutnya

- [BK-02: Global Rules vs Local Rules](../BK-02-Global-Rules-vs-Local-Rules/README.md)
