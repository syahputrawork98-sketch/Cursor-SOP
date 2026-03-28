# SR-03: Structured Rules Architecture

Sub-rak ini membahas cara menyusun `.cursorrules` sebagai arsitektur bertingkat, bukan sekadar daftar instruksi. Fokusnya adalah membedakan aturan global, aturan lokal, artifact governance, role activation, dan template domain agar rules tidak saling tabrak.

> Status per 2026-03-28.
> Sub-rak ini dibangun untuk melayani workflow multi-repo, workspace gabungan, dan artifact governance yang kini makin kompleks.

---

## Gampangnya...

Kalau `.cursorrules` terlalu datar, lama-lama semua aturan numpuk jadi satu dan AI bingung mana yang hukum dasar, mana yang hanya override lokal. Sub-rak ini dibuat supaya rules punya struktur yang jelas.

Anggap saja ini seperti arsitektur bangunan. Ada pondasi, ada dinding, ada pintu, ada jalur evakuasi. Semua penting, tapi fungsi dan posisinya tidak sama.

---

## Konteks & Sejarah

Di banyak proyek, `.cursorrules` awalnya tumbuh secara organik:
- mulai dari satu dua aturan,
- lalu ditambah anti-offside,
- lalu ditambah stack notes,
- lalu ditambah role review,
- lalu ditambah artifact governance.

Masalahnya, semua itu sering hidup dalam satu layer yang sama. Hasilnya:
- global dan local rules tercampur,
- profile frontend dan backend belum punya tempat yang jelas,
- artifact governance hanya jadi tambahan, bukan sistem,
- dan AI tidak tahu mana aturan yang benar-benar mendasar.

Karena itu, sub-rak ini hadir untuk memberi bentuk yang lebih tertib: `.cursorrules` sebagai sistem bertingkat.

---

## Cara Kerja

### Lapisan Rules yang Dibahas

| Lapisan | Fungsi |
|---|---|
| **Global Rules** | hukum dasar lintas proyek |
| **Local Rules** | override spesifik per repo/workspace |
| **Artifact Governance** | aturan hubungan `.cursorrules`, `artifact-map.md`, dan artefak kerja |
| **Role Activation** | kapan lens builder/reviewer aktif |
| **Review Gates** | quality gate sebelum AI dianggap selesai |
| **Domain Overrides** | penyesuaian untuk frontend, backend, atau workspace gabungan |

### Urutan Baca yang Disarankan

1. Baca [BK-01: Blueprint Standar .cursorrules Bertingkat](./BK-01-Blueprint-Standar-cursorrules-Bertingkat/README.md)
2. Lanjut ke [BK-02: Global Rules vs Local Rules](./BK-02-Global-Rules-vs-Local-Rules/README.md)
3. Lanjut ke [BK-03: Artifact Governance di Dalam .cursorrules](./BK-03-Artifact-Governance-di-Dalam-cursorrules/README.md)
4. Gunakan [BK-04: Activation Rules untuk Role Packs dan Review Lenses](./BK-04-Activation-Rules-untuk-Role-Packs-dan-Review-Lenses/README.md) untuk menata role khusus.
5. Pilih template domain di [BK-05](./BK-05-Template-cursorrules-untuk-Project-Frontend/README.md), [BK-06](./BK-06-Template-cursorrules-untuk-Project-Backend/README.md), [BK-07](./BK-07-Template-cursorrules-untuk-Workspace-Gabungan/README.md), atau [BK-08](./BK-08-Template-cursorrules-untuk-Project-Database/README.md).

---

## Kapan Digunakan

Gunakan sub-rak ini saat:
- `.cursorrules` mulai terasa terlalu ramai,
- kamu ingin membedakan global vs local rules,
- kamu memakai artifact governance seperti `artifact-map.md`,
- kamu ingin AI frontend dan backend punya fokus berbeda tanpa membuat mode inti baru,
- kamu bekerja dengan repo terpisah tetapi workspace lokal yang bertemu.

---

## Cara Pakai

### Prinsip Dasar

- jangan jadikan `.cursorrules` sebagai daftar semua hal,
- pisahkan hukum dasar dari override lokal,
- simpan state kerja di artefak, bukan di rules file,
- aktifkan role packs secara terarah, bukan serentak,
- jadikan review gates sebagai penutup, bukan hiasan.

### Formula Ringkas

`.cursorrules = law`

`artifact-map.md = navigation`

`tasks.md + tracker.md = current execution truth`

### Struktur yang Sehat

```text
.cursorrules
  ├─ Global Rules
  ├─ Local Rules
  ├─ Artifact Governance
  ├─ Role Activation Rules
  ├─ Review Gates
  └─ Domain Overrides
```

---

## Lab Praktek

**Skenario: repo frontend dan backend terpisah, tapi workspace lokal gabungan**

Tanpa rules architecture:
- frontend rules kebawa ke backend,
- backend review terlalu teknis masuk ke task UI,
- dan artifact governance tidak punya tempat resmi.

Dengan sub-rak ini:
- global rules tetap sama,
- template frontend dan backend bisa dibedakan,
- workspace gabungan punya bridge rules sendiri,
- dan `.cursorrules` berhenti menjadi file campur aduk.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Rules flattening** | semua aturan hidup di satu level | pakai pemisahan lapisan |
| **Mode inflation** | frontend/backend dibuat jadi mode inti baru | pertahankan core modes di RAK-02 |
| **Role chaos** | terlalu banyak role aktif sekaligus | atur activation rules |
| **Artifact confusion** | rules dan tracker bercampur | tempatkan artifact governance secara eksplisit |

---

## Buku Utama

- [BK-01: Blueprint Standar .cursorrules Bertingkat](./BK-01-Blueprint-Standar-cursorrules-Bertingkat/README.md)
- [BK-02: Global Rules vs Local Rules](./BK-02-Global-Rules-vs-Local-Rules/README.md)
- [BK-03: Artifact Governance di Dalam .cursorrules](./BK-03-Artifact-Governance-di-Dalam-cursorrules/README.md)
- [BK-04: Activation Rules untuk Role Packs dan Review Lenses](./BK-04-Activation-Rules-untuk-Role-Packs-dan-Review-Lenses/README.md)
- [BK-05: Template .cursorrules untuk Project Frontend](./BK-05-Template-cursorrules-untuk-Project-Frontend/README.md)
- [BK-06: Template .cursorrules untuk Project Backend](./BK-06-Template-cursorrules-untuk-Project-Backend/README.md)
- [BK-07: Template .cursorrules untuk Workspace Gabungan](./BK-07-Template-cursorrules-untuk-Workspace-Gabungan/README.md)
- [BK-08: Template .cursorrules untuk Project Database](./BK-08-Template-cursorrules-untuk-Project-Database/README.md)

