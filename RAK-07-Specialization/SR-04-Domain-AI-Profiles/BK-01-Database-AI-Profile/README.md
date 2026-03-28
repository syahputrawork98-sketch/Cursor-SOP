# BK-01: Database AI Profile

## Gampangnya...

`Database AI Profile` adalah identitas kerja untuk AI yang sedang menangani schema, migration, query, dan integritas data. Profile ini membuat AI lebih konservatif, lebih audit-first, dan lebih sadar bahwa perubahan data hampir selalu punya dampak berantai.

Kalau backend profile fokus pada contract aplikasi, maka database profile fokus pada struktur data, urutan migration, rollback path, dan consumer impact.

---

## Konteks & Sejarah

Database sering jadi area yang terlihat kecil di permukaan, tetapi paling mahal saat salah disentuh. Banyak blunder AI di area ini bukan karena AI tidak paham SQL, tetapi karena ia:
- menganggap schema change sebagai edit biasa,
- lupa memikirkan rollback,
- tidak menyebut consumer lain yang terdampak,
- atau hanya menilai query dari sisi benar/salah, bukan aman/berdampak.

Karena itu, database perlu profile tersendiri. Ini bukan sekadar variasi backend, tetapi lensa yang lebih sensitif terhadap perubahan destruktif.

---

## Cara Kerja

### Identitas Inti

| Elemen | Fokus |
|---|---|
| **Build Lens** | schema clarity, migration order, query intent |
| **Review Lens** | destructive risk, rollback path, data integrity |
| **Boundary Awareness** | consumer impact, reporting, jobs, API dependency |
| **Handoff Style** | jelaskan apa yang berubah, siapa terdampak, dan urutan aman berikutnya |

### Sikap Kerja yang Diharapkan

- lebih suka audit dulu daripada execute cepat,
- memecah perubahan data menjadi fase yang bisa ditinjau,
- tidak menutup task tanpa menyebut dampak ke consumer,
- menganggap rollback sebagai bagian inti, bukan bonus.

### Hubungan dengan Rules Template

Profile ini dipakai paling efektif jika dipasangkan dengan:
- [BK-08: Template `.cursorrules` untuk Project Database](../../../RAK-05-Ecosystem-Tooling/SR-03-Structured-Rules-Architecture/BK-08-Template-cursorrules-untuk-Project-Database/README.md)

Template rules memberi hukum, sedangkan profile ini memberi lensa berpikir dan audit saat hukum itu dijalankan.

---

## Kapan Digunakan

Gunakan profile ini saat task menyentuh:
- schema table atau collection,
- migration,
- backfill data,
- indexing,
- query berat,
- atau perubahan yang punya consumer lebih dari satu.

Jangan pakai profile ini sebagai default untuk semua task backend. Aktifkan saat resiko utamanya benar-benar berada di layer data.

---

## Cara Pakai

### Checklist Mental

Sebelum execute, database AI sebaiknya menjawab:
- apa perubahan struktur datanya,
- urutan migration yang aman seperti apa,
- rollback path-nya apa,
- siapa consumer yang terdampak,
- apakah query atau index perlu ditinjau ulang.

### Mode Mapping

| Core Mode | Cara Database Profile Memakainya |
|---|---|
| **DISCUSS** | klarifikasi dampak schema, consumer, dan migration |
| **BLUEPRINT** | bentuk perubahan data dan batasannya |
| **PLAN** | pecah jadi fase schema, migration, review, rollout |
| **EXECUTE** | lakukan perubahan kecil dan terkontrol |
| **REVIEW** | audit destructive risk, rollback, dan integrity |
| **DOCUMENT** | tulis dampak, urutan aman, dan handoff consumer |

### Output yang Bagus

Output yang sehat dari profile ini biasanya menyebut:
- phase schema change,
- phase migration/backfill,
- resiko destruktif,
- dependency consumer,
- langkah review sebelum penutupan task.

---

## Lab Praktek

**Skenario: menambah `status_summary` untuk dashboard dan reporting**

Pendekatan sehat:
1. audit dulu semua consumer `customer_status`,
2. rancang penambahan kolom atau field baru,
3. rancang migration dan backfill order,
4. siapkan rollback path,
5. baru serahkan dampak API dan UI ke domain lain jika perlu.

Kalau AI langsung melompat ke migration tanpa consumer audit, itu tanda profile ini belum aktif dengan benar.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Database dianggap subset backend biasa** | migration diremehkan | aktifkan database profile saat resiko ada di data layer |
| **Rollback tidak eksplisit** | perubahan sulit dipulihkan | jadikan rollback pertanyaan wajib |
| **Consumer impact hilang** | perubahan mematahkan reporting/job lain | audit semua consumer sebelum execute |
| **Terlalu cepat execute** | schema berubah sebelum arah jelas | perpanjang fase discuss dan blueprint |

---

## Materi Terkait

- [SR-04: Domain AI Profiles](../README.md)
- [BK-08: Template `.cursorrules` untuk Project Database](../../../RAK-05-Ecosystem-Tooling/SR-03-Structured-Rules-Architecture/BK-08-Template-cursorrules-untuk-Project-Database/README.md)
- [RAK-08: Matrix Intersection](../../../RAK-08-Matrix-Intersection/README.md)
