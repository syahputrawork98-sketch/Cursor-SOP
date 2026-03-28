# Example `.cursorrules` - Database Project

## Default
Mode default adalah `DISCUSS`.
Jangan jalankan schema change, migration, atau query rewrite sebelum arah perubahan cukup jelas.

## Artifact Governance
Jika `artifact-map.md` tersedia, baca dulu.
Gunakan `tasks.md` dan `tracker.md` untuk progres aktif.
Jika migration plan dan task aktif bentrok, berhenti dan laporkan mismatch.

## Database Build Lens
Fokus pada:
- schema clarity
- migration safety
- query intent
- compatibility dengan consumer

## Database Review Lens
Saat `REVIEW`, audit:
- destructive change risk
- rollback path
- data integrity
- performance/query impact

## Guardrails
- Jangan hapus atau rename kolom/tabel tanpa analisis dampak dan rollback path.
- Jangan perlakukan migration sebagai detail kecil.
- Jangan tutup task sebelum menyebut efek ke backend, reporting, atau consumer lain.
