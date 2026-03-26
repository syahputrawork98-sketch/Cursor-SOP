# BK-02: Project-Specific Templates — Katalog `.cursorrules` Siap Pakai

## 🌟 Gampangnya...

Setiap jenis proyek butuh "perlakuan" yang berbeda. Proyek website (Frontend) fokus pada tampilan dan komponen, sementara proyek server (API) fokus pada keamanan dan struktur data. Buku ini memberikan **resep instan** `.cursorrules` yang bisa kamu copy-paste sesuai jenis proyek yang sedang kamu kerjakan agar AI langsung paham konteks spesifiknya.

---

## 📖 Konteks & Sejarah

Masalah dengan `.cursorrules` yang terlalu umum adalah AI sering memberikan saran yang tidak relevan (misal: menyarankan library UI di proyek Backend). Dengan memberikan **Contextual Guardrails**, kita membatasi ruang gerak AI hanya pada teknologi yang memang kita gunakan dalam proyek tersebut.

---

## ⚙️ Cara Kerja

### Mekanisme Rule Overriding

Ingat hierarki: **Project Rules > Global Rules**.
Jika kamu memiliki `.cursorrules` di folder root (Global), dan `.cursorrules` lain di folder `src/backend` (Project), maka saat bekerja di dalam folder backend, AI akan menggunakan aturan spesifik backend tersebut.

---

## 🗺️ Kapan Mode Ini Relevan

| Proyek | Mode Dominan | Fokus Rules |
|---|---|---|
| **Frontend** | ⚡ EXECUTE | Komponen UI, Tailwind, State |
| **Backend** | 🔬 ANALYZE | Database, Security, Endpoints |
| **Library** | 🧪 TEST | Unit Testing, Documentation |

---

## 🛠️ Cara Pakai

### 🔵 Template 1: Modern Web App (Next.js/React)

Tempelkan ini di root proyek Next.js kamu:

```markdown
# 🌐 NEXT.JS PROJECT RULES

## 🧱 Stack
- Next.js 14+ (App Router), TypeScript, Tailwind CSS.

## 🎨 UI Standards
- Use Semantic HTML.
- Favor Functional Components over Classes.
- Styling: Only use Tailwind utility classes. No inline styles.

## 🚨 Guardrails
- JANGAN gunakan `use client` kecuali benar-benar butuh interaktivitas.
- ALWAYS use `next/image` for images.
- PLAN FIRST before creating new components.
```

### 🟢 Template 2: Robust API (Node.js/Go/Python)

Tempelkan ini di root proyek API kamu:

```markdown
# ⚙️ API PROJECT RULES

## 🧱 Stack
- [GANTI DENGAN STACKMU], PostgreSQL, JWT Auth.

## 🛡️ Security First
- Never console.log sensitive data.
- Always use environment variables for secrets.
- Every endpoint must have validation (Zod/Pydantic/etc).

## 🚨 Guardrails
- JANGAN ubah schema database tanpa BLUEPRINT.
- DILARANG menghapus migrations yang sudah ada.
- Every function must have documentation comments.
```

---

## 🧪 Lab Praktek

**Skenario: Memaksa AI Mengikuti Standar Styling**

1. Kamu sedang mengerjakan proyek Next.js tapi AI terus-terusan memberi kode CSS biasa.
2. Gunakan Template 1 (Web App).
3. Ketik: *"Buatkan tombol login."*
4. **Hasil**: AI akan membuat komponen dengan Tailwind CSS sesuai rules, bukan CSS biasa.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Stack Mismatch** | Kamu pakai Vue tapi template-nya React | Selalu audit bagian `## 🧱 Stack` sebelum copy-paste. |
| **Conflicting Rules** | Aturan project tabrakan dengan aturan global | Gunakan `[OVERRIDE]` tag di awal section project rules. |
| **Rules Outdated** | AI menyarankan fitur versi lama | Update stack version di rules (misal: "Next.js 15" bukan "Next.js 13"). |

---

### 📖 Materi Selanjutnya
- [BK-03: Anti-Offside Tuning](../BK-03-Anti-Offside-Tuning/README.md)
