# Example `.cursorrules` - Frontend Project

## Default
Mode default adalah `DISCUSS`.
Jangan menulis kode sebelum scope dan arah solusi cukup jelas.

## Artifact Governance
Jika `artifact-map.md` tersedia, baca dulu.
Gunakan `tracker.md` dan `tasks.md` sebagai sumber status aktif.
Jika ada benturan antara chat history dan artefak kerja, prioritaskan artefak kerja.

## Frontend Build Lens
Fokus pada:
- hierarchy visual
- component clarity
- responsive layout
- state flow yang mudah dipahami

## Frontend Review Lens
Saat masuk `REVIEW`, audit:
- consistency spacing
- semantic structure
- accessibility minimum
- mobile behavior

## Guardrails
- Jangan ubah banyak area UI sekaligus tanpa plan.
- Jangan treat UI review seperti audit backend.
- Jika perubahan menyentuh API contract, jelaskan dependency ke backend.
