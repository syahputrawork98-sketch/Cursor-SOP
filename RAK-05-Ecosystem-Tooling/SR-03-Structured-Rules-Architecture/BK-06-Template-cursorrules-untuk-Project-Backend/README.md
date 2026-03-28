# BK-06: Template `.cursorrules` untuk Project Backend

## Gampangnya...

Project backend butuh AI yang disiplin di validation, contract, security, logging, dan test safety. Template ini menajamkan fokus itu.

---

## Konteks & Sejarah

Tanpa template backend yang jelas, AI sering:
- terlalu fokus cepat implementasi,
- kurang hati-hati pada validation,
- lupa audit contract dan side effect.

---

## Cara Kerja

### Isi Minimal

- base persona
- discuss-first
- artifact governance
- `API Builder`
- `Backend Integrity Reviewer`
- validation, error handling, test, dan security gates

### Skeleton Ringkas

```text
# .cursorrules

## Default
Mode default adalah DISCUSS.

## Artifact Governance
Jika artifact-map.md tersedia, baca dulu.

## Backend Build Lens
Fokus pada contract, flow data, validation, dan maintainability.

## Backend Review Lens
Periksa auth, error handling, logging, integration safety, dan test impact.
```

---

## Kapan Digunakan

Gunakan template ini untuk repo backend atau workspace yang sedang fokus di API/service logic.

---

## Cara Pakai

### Review Gates

- cek validation
- cek auth/security boundary
- cek error handling
- cek integration/test impact

### Example Pack

Contoh yang lebih konkret ada di folder:
- [examples/example-cursorrules.md](./examples/example-cursorrules.md)
- [examples/example-artifact-map.md](./examples/example-artifact-map.md)
- [examples/example-tasks.md](./examples/example-tasks.md)
- [examples/example-tracker.md](./examples/example-tracker.md)

---

## Lab Praktek

**Skenario: menambah endpoint baru**

Gunakan build lens saat merancang contract dan flow, lalu reviewer lens saat audit validation, auth, dan test effect.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Backend direview seperti UI** | audit terlalu dangkal | aktifkan backend integrity lens |
| **Validation tidak eksplisit** | bug muncul di edge case | jadikan validation gate wajib |
| **Contract drift** | FE dan BE tidak sinkron | pakai artifact governance dan review gate |

---

## Materi Selanjutnya

- [BK-07: Template .cursorrules untuk Workspace Gabungan](../BK-07-Template-cursorrules-untuk-Workspace-Gabungan/README.md)

