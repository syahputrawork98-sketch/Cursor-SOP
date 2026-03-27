# BK-04: Weekly Quota and Usage Strategy

## Gampangnya...

Kuota mingguan itu bukan untuk ditakuti, tapi untuk diatur dengan cerdas. Tujuannya bukan hemat mati-matian, melainkan memakai model yang tepat untuk pekerjaan yang tepat agar jatahmu tidak habis di tugas receh.

Dokumen ini membahas strategi penggunaan yang tahan lama, bukan sekadar angka limit sesaat.

> Status per 2026-03-28.
> Angka limit dan availability per plan bisa berubah. Prinsip budgeting di dokumen ini jauh lebih stabil daripada angka spesifiknya.

---

## Konteks & Sejarah

Begitu user mulai memakai ChatGPT untuk kerja serius, masalah baru muncul:
- sesi thinking dipakai untuk tugas yang sebenarnya ringan,
- satu masalah sederhana dibuka dalam banyak thread,
- prompt panjang diulang dari nol,
- jatah mingguan terkuras sebelum tugas penting datang.

Masalahnya jarang pada "kuotanya terlalu kecil". Lebih sering, masalahnya ada pada **routing kerja** yang belum disiplin.

---

## Cara Kerja

### Triage Tugas

| Kelas Tugas | Contoh | Strategi |
|---|---|---|
| **Ringan** | Rewrite, summary, tanya cepat | Gunakan model cepat dan selector ringan |
| **Menengah** | Draft dokumen, coding biasa, review ringan | Gunakan default aman |
| **Mahal** | Debug berat, analisis arsitektur, audit final | Simpan model thinking/pro untuk sini |

### Prinsip Budgeting

1. Gunakan tenaga paling besar hanya untuk keputusan yang salahnya mahal.
2. Jangan pakai sesi berat untuk hal yang bisa selesai dengan model cepat.
3. Simpan satu porsi jatah untuk review final atau task dadakan yang benar-benar penting.

### Fakta Resmi yang Berguna

Per dokumen resmi OpenAI saat ini:
- GPT-5.3 adalah default untuk user ChatGPT yang login.
- Plus dan Business dapat memilih GPT-5.4 Thinking manual hingga sekitar `3.000 pesan per minggu`.
- Routing otomatis dari `Auto` ke `Thinking` tidak dihitung ke limit manual mingguan tersebut.

Artinya:
- jangan panik jika limit manual Thinking tercapai,
- `Auto` tetap berguna sebagai alat penghemat.

---

## Kapan Digunakan

Dokumen ini relevan jika kamu mengalami salah satu gejala berikut:
- jatah model utama sering habis terlalu cepat,
- kamu merasa selalu tergoda memakai mode berat,
- kamu belum punya ritme kapan harus berpikir dalam dan kapan cukup cepat.

---

## Cara Pakai

### Strategi Mingguan

**Awal minggu**
- pakai sesi terbaikmu untuk blueprint, keputusan arah, dan analisis inti.

**Tengah minggu**
- gunakan model cepat atau setting default untuk eksekusi, drafting, dan iterasi.

**Akhir minggu**
- simpan satu porsi jatah untuk review, cleanup, dan keputusan final.

### Strategi Per Sesi

- mulai dengan prompt yang ringkas dan tajam,
- jangan ulang semua konteks dari nol jika cukup dengan ringkasan,
- gunakan summary handover saat berpindah thread,
- eskalasi ke model atau selector yang lebih berat hanya jika benar-benar perlu.

### Anti-Boros Pattern

- jangan pakai thinking berat untuk revisi kecil,
- jangan buka tiga chat untuk satu masalah yang sama,
- jangan mengulang prompt panjang tanpa merangkum hasil sebelumnya,
- jangan simpan semua tugas ke model premium jika problemnya sebenarnya rutin.

### Fallback Saat Jatah Menipis

- pindah ke model yang lebih ringan untuk drafting,
- pecah task besar menjadi blueprint dan execute,
- gunakan ChatGPT untuk analisis inti, lalu kerjakan implementasi di alat lain jika perlu,
- manfaatkan `Auto` jika kamu tidak ingin setiap task manual memakan jatah Thinking.

---

## Lab Praktek

**Skenario: satu minggu kerja**

Senin:
- pakai GPT-5.4 Thinking untuk menyusun prioritas dan menganalisis problem inti.

Selasa-Kamis:
- pakai GPT-5.3 Instant atau setting yang lebih ringan untuk drafting, rewrite, dan iterasi.

Jumat:
- pakai sesi terbaik yang tersisa untuk final review.

Hasil yang diincar:
- kualitas tetap tinggi,
- jatah tidak jebol di tengah minggu.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Boros di awal minggu** | Jatah mahal habis terlalu cepat | Gunakan triage tugas sebelum memilih model |
| **Mode berat jadi default** | Semua task terasa lambat | Jadikan Standard atau Instant sebagai baseline |
| **Prompt reset terus-menerus** | Konteks diulang dari nol berkali-kali | Gunakan ringkasan sesi |
| **Tidak punya cadangan** | Saat task penting datang, jatah sudah habis | Selalu sisakan porsi untuk audit final |

---

## Materi Selanjutnya

- [BK-05: When to Use ChatGPT vs Codex vs API](../BK-05-When-to-Use-ChatGPT-vs-Codex-vs-API/README.md)
