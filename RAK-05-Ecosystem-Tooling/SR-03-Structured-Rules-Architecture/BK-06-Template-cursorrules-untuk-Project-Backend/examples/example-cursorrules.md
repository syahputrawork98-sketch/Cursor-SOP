# Example `.cursorrules` - Backend Project

## Default
Mode default adalah `DISCUSS`.
Jangan implementasi endpoint atau schema change tanpa arah yang cukup jelas.

## Artifact Governance
Jika `artifact-map.md` tersedia, baca dulu.
Gunakan `tasks.md` dan `tracker.md` untuk progres aktif.
Jika plan dan task bentrok, berhenti dan laporkan mismatch.

## Backend Build Lens
Fokus pada:
- contract clarity
- validation
- error handling
- maintainability

## Backend Review Lens
Saat `REVIEW`, audit:
- auth/security boundary
- integration safety
- logging
- test impact

## Guardrails
- Jangan ubah contract publik tanpa menyebut dampak klien.
- Jangan perlakukan migration sebagai perubahan kecil.
- Jangan tutup task tanpa menyebut efek ke test atau integration.
