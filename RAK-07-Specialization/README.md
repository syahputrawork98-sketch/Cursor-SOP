# RAK-07: Specialization - Workflow Spesialis, Audit Berlapis, dan Kurator Kerja

## Gampangnya...

Kalau rak-rak sebelumnya mengajari hukum dasar dan cara kerja umum, maka `RAK-07` mengajari cara membuat AI bekerja seperti **spesialis**. Di sini AI tidak lagi diperlakukan sebagai satu tukang serba bisa, tetapi sebagai sistem kerja yang bisa dibagi per peran, per ritual, per jenis operasi, dan per domain kerja.

Makanya isi rak ini sekarang punya tiga wajah yang saling melengkapi:
- pola kerja **multi-agent dan reviewer**,
- pola kerja **kurator workflow** untuk creation, repair, refactor, dan documentation,
- pola **domain AI profiles** untuk frontend, backend, database, dan workspace lintas domain.

---

## Konteks & Sejarah

Begitu user mulai serius memakai AI untuk kerja teknis, masalahnya berubah. Bukan lagi sekadar "AI bisa bantu atau tidak", tetapi:
- siapa yang mengeksekusi,
- siapa yang mengkritik,
- workflow mana yang dipakai,
- kapan task harus diperlakukan sebagai pembangunan baru,
- kapan ia harus diperlakukan sebagai pemulihan, pembenahan, atau dokumentasi,
- dan domain spesialis apa yang harus aktif agar AI tidak memakai lensa yang salah.

Tanpa spesialisasi seperti ini, satu AI cenderung:
- menilai karyanya sendiri terlalu lunak,
- bugfix melebar menjadi refactor,
- refactor menyamar sebagai rewrite,
- dokumentasi tertinggal dan pengetahuan sesi hilang,
- atau schema change database diperlakukan seperti edit backend biasa.

---

## Cara Kerja

### Tiga Pilar Specialization

```mermaid
graph TD
    A[Task] --> B{Butuh spesialisasi apa?}
    B --> C[Role Specialization\nExecutor Reviewer Critic]
    B --> D[Workflow Specialization\nCreation Repair Refactor Documentation]
    B --> E[Domain Profiles\nFrontend Backend Database Workspace]
    C --> F[Audit Berlapis]
    D --> G[Kurator yang Tepat]
    E --> H[Lensa yang Tepat]
    F --> I[Hasil Lebih Aman]
    G --> I
    H --> I
```

### Peta Isi Rak

| Pilar | Fungsi |
|---|---|
| **Multi-Agent Patterns** | Membagi kerja berdasarkan peran seperti executor, critic, reviewer |
| **Review Rituals** | Memastikan hasil eksekusi diaudit sebelum dianggap selesai |
| **Curator Workflows** | Memilih workflow yang tepat berdasarkan jenis operasi terhadap proyek |
| **Domain AI Profiles** | Memberi lensa spesialis berdasarkan domain kerja seperti database |

---

## Kapan Digunakan

RAK ini relevan ketika kamu mulai menghadapi pertanyaan seperti:
- "Apakah saya butuh reviewer terpisah?"
- "Task ini creation, repair, refactor, atau documentation?"
- "Bagaimana caranya agar AI tidak memeriksa pekerjaannya sendiri dengan terlalu lunak?"
- "Kapan saya harus mengganti workflow, bukan cuma mengganti prompt?"
- "Kapan saya harus mengaktifkan lensa database, bukan backend biasa?"

Kalau masalahmu sudah naik dari level aturan dasar ke level **orkestrasi spesialis**, maka ini rak yang tepat.

---

## Cara Pakai

### Jika Masalahmu Soal Peran

Masuk ke:
- `SR-01: Multi-Agent Patterns`

Gunakan saat kamu ingin membedakan:
- executor,
- critic,
- reviewer,
- atau role switching dalam satu sesi.

### Jika Masalahmu Soal Audit

Masuk ke:
- `SR-02: Review Rituals`

Gunakan saat kamu ingin menutup eksekusi dengan:
- audit,
- test,
- handover,
- evaluasi kualitas hasil.

### Jika Masalahmu Soal Jenis Workflow

Masuk ke:
- `SR-03: Curator Workflows`

Gunakan saat kamu perlu menentukan apakah task ini:
- `Creation`
- `Repair`
- `Refactor`
- `Documentation`

### Jika Masalahmu Soal Domain Spesialis

Masuk ke:
- `SR-04: Domain AI Profiles`

Gunakan saat kamu ingin membedakan lensa kerja frontend, backend, database, atau workspace lintas domain.

### Aturan Praktis

- jangan pakai satu workflow untuk semua jenis tugas,
- jangan biarkan executor menjadi hakim tunggal pekerjaannya sendiri,
- jangan jadikan domain profile sebagai `core mode` baru,
- jika task berubah tujuan di tengah jalan, klasifikasikan ulang secara sadar,
- jika resiko utamanya ada di layer data, aktifkan profile database secara eksplisit.

---

## Lab Praktek

**Skenario 1: Feature baru besar**

Task:
"Saya ingin membangun dashboard admin baru."

Pendekatan yang tepat:
- pakai `Curator Workflow: Creation`
- lalu gunakan reviewer di akhir fase implementasi.

**Skenario 2: Bug sulit**

Task:
"Login sering gagal saat traffic tinggi."

Pendekatan yang tepat:
- pakai `Curator Workflow: Repair`
- jika fix sudah stabil, tutup dengan ritual review dan documentation.

**Skenario 3: Perubahan schema penting**

Task:
"Tambahkan field baru yang dipakai dashboard dan reporting."

Pendekatan yang tepat:
- aktifkan `Database AI Profile`
- audit consumer, migration, dan rollback dulu,
- baru handoff ke backend atau frontend jika ada dampak lanjutan.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Satu AI, semua peran** | Executor sekaligus reviewer sekaligus critic tanpa batas | Pisahkan peran atau pakai role switching yang eksplisit |
| **Satu workflow untuk semua task** | Task creation diperlakukan seperti bugfix atau sebaliknya | Klasifikasikan task sebelum eksekusi |
| **Audit terlambat** | Review baru dilakukan saat semuanya sudah telanjur besar | Jadikan review sebagai ritual per fase |
| **Kurator tidak dikenali** | AI masuk workflow yang salah sejak awal | Gunakan template klasifikasi task di SR-03 |
| **Domain lens terlalu umum** | database dinilai seperti backend biasa | aktifkan profile domain yang tepat |

---

### Sub-Rak & Buku
- **SR-01: Multi-Agent Patterns**
  - [BK-01: Role Switching Patterns](./SR-01-Multi-Agent-Patterns/BK-01-Role-Switching-Patterns/README.md)
  - [BK-02: The Critic Pattern](./SR-01-Multi-Agent-Patterns/BK-02-The-Critic-Pattern/README.md)
- **SR-02: Review Rituals**
  - [BK-01: Post-Execute Audit Ritual](./SR-02-Review-Rituals/BK-01-Post-Execute-Audit-Ritual/README.md)
- **SR-03: Curator Workflows**
  - [BK-01: Kurator untuk Project Baru](./SR-03-Curator-Workflows/BK-01-Kurator-untuk-Project-Baru/README.md)
  - [BK-02: Kurator untuk Perbaikan dan Bugfix](./SR-03-Curator-Workflows/BK-02-Kurator-untuk-Perbaikan-dan-Bugfix/README.md)
  - [BK-03: Kurator untuk Refactor dan Pembenahan](./SR-03-Curator-Workflows/BK-03-Kurator-untuk-Refactor-dan-Pembenahan/README.md)
  - [BK-04: Kurator untuk Dokumentasi dan Handover](./SR-03-Curator-Workflows/BK-04-Kurator-untuk-Dokumentasi-dan-Handover/README.md)
- **SR-04: Domain AI Profiles**
  - [BK-01: Database AI Profile](./SR-04-Domain-AI-Profiles/BK-01-Database-AI-Profile/README.md)
