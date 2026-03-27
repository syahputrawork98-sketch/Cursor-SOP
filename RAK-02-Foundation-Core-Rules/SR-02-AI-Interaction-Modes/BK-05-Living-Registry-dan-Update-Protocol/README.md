# BK-05: Living Registry dan Update Protocol

Buku ini adalah mesin evolusi untuk sistem mode AI di repo ini. Tujuannya agar daftar mode tidak kaku, tetapi juga tidak liar. Kita ingin sistem yang bisa berkembang saat praktik internet berubah, namun tetap terkurasi dan stabil untuk dipakai.

> Status per 2026-03-28.
> Daftar mode di internet cepat berubah. Karena itu update harus berbasis sumber dan evaluasi, bukan hanya mengikuti istilah baru yang sedang ramai.

---

## Gampangnya...

Sistem mode yang baik itu hidup, tapi tidak reaktif. Ia bisa menerima pengetahuan baru, tetapi punya gerbang sebelum mengubah aturan kerja harian.

Buku ini menjawab pertanyaan:
- mode mana yang dianggap inti,
- mode mana yang hanya wawasan tambahan,
- kapan mode baru boleh masuk,
- dan apa yang harus dilakukan saat user meminta "update".

---

## Konteks & Sejarah

Karena ekosistem agent modern cepat berubah, istilah baru sering bermunculan. Hari ini orang bicara `tool use`, besok `reasoning effort`, lalu muncul `handoff`, `reflection`, `memory`, `guardrails`, atau istilah lain. Jika semua istilah baru langsung masuk ke sistem inti, repo akan cepat gemuk dan kehilangan konsistensi.

Karena itu kita butuh registry hidup:
- cukup terbuka untuk belajar,
- cukup ketat untuk menjaga kualitas.

---

## Cara Kerja

### Status Kategori Mode

| Status | Makna | Contoh |
|---|---|---|
| `Core` | Dipakai resmi dalam repo | `DISCUSS`, `PLAN`, `EXECUTE` |
| `Extended` | Diakui dan dijelaskan, tapi belum wajib | `RESEARCH`, `TOOL USE`, `HANDOFF` |
| `Experimental` | Menarik, tapi masih niche atau belum stabil | istilah baru yang belum sering dipakai |
| `Deprecated` | Pernah dipakai, tapi tidak lagi direkomendasikan | mode atau istilah lama yang ditinggalkan |

### Aturan Menambah Mode Baru

Mode baru layak masuk registry jika:
- muncul berulang di praktik internet atau sumber resmi,
- punya fungsi yang cukup berbeda dari mode yang sudah ada,
- tidak sekadar sinonim,
- dan terbukti berguna dalam workflow nyata.

### Aturan Promosi `Extended -> Core`

Sebuah mode extended layak dipromosikan jadi core jika:
- digunakan sering dalam repo,
- benar-benar membantu keputusan kerja harian,
- perannya tidak bisa dijelaskan cukup dengan core mode lama,
- dan seluruh struktur repo tetap lebih jelas setelah promosi itu terjadi.

### Aturan Menolak Mode Baru

Mode baru sebaiknya ditolak jika:
- hanya nama baru untuk hal lama,
- hanya tren sesaat,
- atau lebih tepat diperlakukan sebagai mekanisme, bukan mode.

---

## Kapan Digunakan

Gunakan buku ini saat:
- kamu ingin menambah mode baru ke sistem repo,
- kamu menemukan istilah baru dari internet dan ingin menilainya,
- kamu ingin tahu apakah suatu istilah harus jadi `core`, `extended`, atau cukup dicatat saja,
- kamu ingin melakukan refresh pengetahuan mode secara berkala.

---

## Cara Pakai

### Format Evaluasi Mode Baru

Sebelum menambah mode, jawab dulu:

1. Apa nama mode ini?
2. Fungsi utamanya apa?
3. Apakah ia benar-benar berbeda dari mode yang sudah ada?
4. Di sumber resmi atau praktik luas, seberapa sering ia muncul?
5. Lebih cocok jadi `core`, `extended`, `experimental`, atau ditolak?
6. Apa contoh task yang menunjukkan nilainya?

### Format Entry Update

Gunakan format seperti ini:

```text
Nama Mode:
Status:
Tanggal Update:
Sumber Acuan:
Alasan Penambahan/Perubahan:
Hubungan ke Core Modes:
Contoh Pemakaian:
Keputusan:
```

### Protocol Saat User Meminta `update`

1. Cek sumber resmi yang relevan.
2. Bedakan antara pola kerja umum dan istilah marketing.
3. Peta istilah baru ke core modes yang sudah ada.
4. Putuskan statusnya:
   - `core`,
   - `extended`,
   - `experimental`,
   - atau `rejected`.
5. Catat tanggal dan alasan perubahan.

### Sumber Acuan Utama

- OpenAI untuk design foundations, tools, orchestration, and handoffs.
- Anthropic untuk tool use, memory, context management, and agent loop.
- Google untuk planning, execution, synthesis, background execution, and context tooling.

---

## Lab Praktek

**Contoh: menilai `TOOL USE`**

Apakah sering muncul di sumber resmi?
- ya

Apakah berbeda dari `EXECUTE`?
- ya, tapi sering menjadi mekanisme di dalam `ANALYZE`, `DEBUG`, atau `EXECUTE`

Apakah harus dipromosikan jadi core?
- belum tentu

Keputusan sehat:
- masukkan sebagai `Extended`

**Contoh: menilai `HANDOFF`**

Apakah penting di praktik multi-agent?
- ya

Apakah sudah wajib untuk workflow repo sehari-hari?
- belum tentu

Keputusan sehat:
- masukkan sebagai `Extended`, lalu lihat apakah nanti cukup sering dipakai untuk dipromosikan.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Semua istilah baru langsung diadopsi** | Sistem mode jadi gemuk | Lewatkan semua penambahan lewat registry |
| **Tidak ada status kategori** | Semua mode terasa sama penting | Gunakan label `core`, `extended`, `experimental`, `deprecated` |
| **Update tanpa sumber** | Sistem mengikuti rumor | Wajib catat sumber dan tanggal |
| **Sinonim dianggap mode baru** | Daftar membengkak tanpa nilai tambah | Cek apakah fungsi dasarnya sudah ditutup mode lama |
