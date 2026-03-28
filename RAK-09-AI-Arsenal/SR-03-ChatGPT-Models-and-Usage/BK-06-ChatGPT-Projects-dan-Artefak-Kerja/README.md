# BK-06: ChatGPT Projects dan Artefak Kerja

## Gampangnya...

Kalau kamu memakai ChatGPT untuk kerja yang panjang, bertahap, dan sering dilanjutkan di sesi berbeda, jangan hanya mengandalkan chat history atau context window. Untuk kebutuhan seperti itu, pendekatan yang lebih sehat adalah memakai **ChatGPT Projects** lalu menyimpan artefak kerja penting sebagai file terpisah.

Dengan cara ini, ChatGPT tidak menjadi satu-satunya tempat ingatan kerja. Chat hanya menjadi tempat berpikir dan berdiskusi, sementara `blueprint`, `plan`, `tasks`, `tracker`, dan `handover` hidup sebagai artefak yang bisa dibaca ulang dengan rapi.

> Status per 2026-03-28.
> Fitur Projects, memory, file limits, dan perilaku context dapat berubah. Selalu cek dokumen resmi OpenAI bila ada perubahan produk besar.

---

## Konteks & Sejarah

Dalam ChatGPT, banyak user merasa kerja sudah "tersimpan" hanya karena percakapannya masih ada. Masalahnya, chat history bukan artefak kerja yang ideal untuk semua situasi:
- progres susah dibaca ulang,
- keputusan penting tercampur dengan diskusi panjang,
- task aktif mudah tenggelam,
- dan context window tetap punya batas.

OpenAI sekarang menyediakan `Projects` di ChatGPT untuk pekerjaan jangka panjang. Menurut artikel resmi OpenAI, project bisa mengelompokkan chat, file, dan instruksi khusus dalam satu workspace, serta mendukung memory dalam project. Artinya, untuk kerja yang berkembang dari hari ke hari, Projects adalah padanan paling dekat dengan "workspace hidup" di dalam ChatGPT.

Tetapi Projects saja belum cukup. Jika semua hal tetap dibiarkan hanya hidup di obrolan, kamu masih akan mengalami kebingungan yang sama. Karena itu, Projects sebaiknya dipadukan dengan file `.md` yang memegang artefak kerja inti.

---

## Cara Kerja

### Dua Gaya Kerja di ChatGPT

| Gaya | Cocok Untuk | Kekurangan |
|---|---|---|
| **Context-only** | tanya jawab cepat, ide awal, review singkat | progres mudah kabur untuk kerja panjang |
| **Projects + artefak `.md`** | kerja multi-sesi, planning, dokumentasi, riset bertahap | butuh disiplin lebih tinggi |

### Rekomendasi Praktis

- Untuk task pendek atau satu sesi: context window biasa masih cukup.
- Untuk task menengah sampai panjang: gunakan `Project`.
- Untuk task yang punya banyak fase: simpan artefak kerja sebagai file terpisah.

### Peran Chat vs File

| Tempat | Fungsi Utama |
|---|---|
| **Chat** | diskusi, berpikir, bertanya, memutuskan |
| **Project instructions** | aturan perilaku umum di project itu |
| **File `.md`** | sumber kebenaran yang lebih stabil |

### File yang Disarankan

| File | Fungsi |
|---|---|
| `blueprint.md` | mendefinisikan arah solusi |
| `implementation-plan.md` | mendefinisikan urutan fase kerja |
| `tasks.md` | memegang checklist eksekusi |
| `tracker.md` | memegang status aktif saat ini |
| `handover.md` | memegang ringkasan akhir sesi |

### Tentang Memory di Projects

Menurut artikel resmi OpenAI tentang Projects:
- Projects bisa menyimpan chats, files, dan project instructions dalam satu tempat.
- Projects mendukung memory dalam project.
- Ada mode `project-only memory` yang membatasi context ke dalam project itu sendiri.

Ini penting karena jika kamu ingin perilaku yang lebih mirip workspace terisolasi seperti pola Gemini atau repo-based workflow, maka `project-only memory` adalah opsi yang paling dekat. Kalau kamu membiarkan memory lebih terbuka, ChatGPT bisa tetap membawa context dari luar project, tergantung tipe plan dan setting memory.

---

## Kapan Digunakan

Gunakan pendekatan ini saat:
- kamu memakai ChatGPT untuk pekerjaan lebih dari satu sesi,
- kamu sering kehilangan jejak "kita lagi ada di langkah mana",
- kamu punya blueprint dan plan tapi progresnya tetap kacau,
- kamu ingin ChatGPT bekerja lebih mirip workspace daripada obrolan bebas,
- kamu ingin mengurangi bentrok antara diskusi, task, dan laporan.

Jangan memaksa semua chat biasa menjadi workflow artefak lengkap. Untuk pertanyaan ringan, pendekatan context-only tetap lebih cepat.

---

## Cara Pakai

### Workflow yang Disarankan

1. Buat `Project` baru untuk pekerjaan yang panjang.
2. Jika memungkinkan dan cocok untuk use case-mu, pilih `project-only memory` agar konteksnya lebih terisolasi.
3. Tambahkan `project instructions` yang menjelaskan gaya kerja.
4. Upload atau simpan file `.md` inti ke dalam project.
5. Gunakan chat untuk diskusi, tapi jadikan file `.md` sebagai sumber kebenaran.

### Aturan Emas

- jangan jadikan chat history sebagai satu-satunya tracker,
- jangan campur task aktif ke dalam blueprint,
- jangan simpan semua keputusan penting hanya di obrolan,
- gunakan chat untuk berpikir dan file untuk menjaga struktur,
- jika artefak mulai banyak, tambahkan `artifact-map.md` sebagai artifact map.

### Rekomendasi Gaya

Kalau kamu ingin workflow ChatGPT yang paling mirip dengan pola Gemini:
- buat project terpisah,
- gunakan file `.md` terpisah,
- batasi memory ke project jika perlu,
- dan perbarui file-file itu secara sadar setelah loop besar selesai.

### Kapan Context Window Saja Sudah Cukup

Context window saja cukup jika:
- task hanya satu sesi,
- tidak ada kebutuhan handover,
- progres tidak perlu dilacak,
- kamu hanya ingin analisis cepat atau brainstorming.

---

## Lab Praktek

**Skenario: Menulis dan membangun sesuatu dalam beberapa hari**

Kalau kamu hanya membuka satu chat panjang, biasanya gejalanya:
- requirement lama tenggelam,
- task aktif sulit dicari,
- dan keputusan besar tercampur dengan obrolan kecil.

Dengan `Project + file .md`, alurnya berubah:

1. simpan blueprint sebagai file,
2. simpan plan sebagai file,
3. simpan tasks dan tracker sebagai file,
4. gunakan chat hanya untuk mendiskusikan task yang sedang aktif,
5. simpan ringkasan akhir ke handover.

Hasilnya:
- progres lebih mudah diaudit,
- sesi baru tidak mulai dari nol,
- dan ChatGPT tidak perlu menebak state hanya dari history chat.

---

## Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Semua disimpan di chat** | informasi penting tenggelam | pindahkan artefak inti ke file `.md` |
| **Project ada, tapi file tidak ada** | project terasa rapi tapi state tetap kabur | jadikan files sebagai sumber kebenaran |
| **Files ada, tapi tidak diupdate** | chat dan file mulai bertabrakan | update file setelah loop penting |
| **Memory terlalu longgar** | ChatGPT membawa konteks dari luar yang tidak diinginkan | gunakan project-only memory jika perlu isolasi |
| **Workflow terlalu berat untuk task kecil** | user malas memakai project | pakai context-only untuk task pendek |

---

## Referensi Resmi

- OpenAI Help Center: https://help.openai.com/en/articles/10169521
- OpenAI Help Center: https://help.openai.com/en/articles/9309188-add-files-from-connected-apps-in-chatgpt

---

## Materi Selanjutnya

- [BK-07: Template Artefak Workflow untuk ChatGPT Projects](../BK-07-Template-Artefak-Workflow-untuk-ChatGPT-Projects/README.md)
- [RAK-08 / BK-03: Template `artifact-map.md` untuk Artifact Governance](../../../../RAK-08-Matrix-Intersection/SR-01-Consistency-Management/BK-03-Template-Artifact-Map-untuk-Artifact-Governance/README.md)

