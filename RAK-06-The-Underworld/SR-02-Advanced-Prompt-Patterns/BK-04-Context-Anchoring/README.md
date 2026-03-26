# BK-01: Context Anchoring — Teknik "Melempar Jangkar" Konteks

## 🌟 Gampangnya...

Pernahkah kamu bekerja lama dengan AI (sesi chat panjang), lalu tiba-tiba di tengah jalan AI mulai lupa aturan awal, cara kodingmu berubah, atau dia melakukan kesalahan yang sudah dilarang? Itu karena **Jendela Konteks**-nya mulai tergeser. **Context Anchoring** adalah cara melempar "jangkar" secara berkala agar AI tetap ingat identitas, aturan, dan tujuan awal proyekmu meski sesi sudah sangat panjang.

---

## 📖 Konteks & Sejarah

Setiap sesi chat dengan AI memiliki kuota memori terbatas (*Context Window*). Saat chat menjadi sangat panjang, bagian paling atas (awal diskusi) akan "didorong keluar" agar ada ruang untuk pertanyaan barumu. Masalahnya, di bagian atas itulah biasanya instruksi terpenting berada. Untuk mencegah ini, kita menggunakan teknik **Anchoring**.

---

## ⚙️ Cara Kerja

### Mekanisme "Memory Refresh"

Kita memasukkan kembali poin-poin krusial ke dalam chat secara periodik atau menggunakan link file yang statis (`@session-notes.md`). Dengan cara ini, instruksi kunci selalu berada dalam jendela memori aktif AI dan tidak pernah "terdorong keluar".

---

## 🗺️ Kapan Mode Ini Relevan

| Durasi Sesi | Gejala | Tindakan |
|---|---|---|
| **Awal Sesi** | Fresh context | Ritual "Briefing" awal. |
| **Sesi Menengah** (10-15 Turn) | Mulai muncul typo/blunder | **Throw Anchor!** (Lakukan Anchoring). |
| **Sesi Panjang** (30+ Turn) | AI mulai berhalusinasi | **Reset & Restore Anchor.** |

---

## 🛠️ Cara Pakai

### Teknik 1: Manual Anchor (Setiap 10 Menit)

Ketikkan mantra ini saat kamu merasa AI mulai "lelah":

```markdown
"Sebelum kita lanjut, baca kembali @.cursorrules dan ringkas 
 pemahamanmu tentang: 1. Mode saat ini, 2. Batasan koding saya."
```

### Teknik 2: The Anchor File (`session-notes.md`)

Jangan simpan semua instruksi di dalam chat. Simpan di file fisik:
1. Buat file `docs/session-notes.md`.
2. Setiap kali ada keputusan penting, suruh AI catat di sana.
3. Gunakan prompt: *"Gunakan @session-notes.md sebagai referensi utama setiap kali saya memberi instruksi baru."*

### Teknik 3: Identity Anchor (Status Check)

Minta AI melaporkan "siapa dia" sekarang:
```markdown
"Status check: Kamu sedang di mode apa? Apakah ada file yang 
 sedang kamu kunci statusnya? Apa tujuan besar kita di sesi ini?"
```

---

## 🧪 Lab Praktek

**Skenario: AI mulai mengerjakan secara "Dangkal"**

Kamu menyadari AI tidak lagi menggunakan detail teknik yang kamu minta di awal.

**Solusi — Throw Anchor:**
1. Hentikan task.
2. Ketik: *"Kamu mulai kehilangan presisi. Lempar jangkar: Baca kembali @RAK-06 dan @instruksi-awal.md. Jelaskan bagian mana yang kamu lupakan."*
3. AI akan me-recall dan memperbaiki gaya responsnya.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Anchor Terlalu Berat** | AI menghabiskan quota token hanya untuk baca anchor terus | Hanya melempar anchor saat diindikasikan ada penurunan kualitas respons. |
| **Anchor Statis** | File anchor tidak pernah diupdate | Jadikan pengerjaan file anchor sebagai bagian dari ritual `REVIEW`. |
| **Total Context Loss** | Sesi sudah terlalu berat sampai anchor pun tidak membantu | Save `session-notes.md`, lalu buka sesi chat baru (Fresh Start). |

---

### 📖 Materi Selanjutnya
- [BK-02: Chain-of-Thought Execution](../BK-02-Chain-of-Thought/README.md)
