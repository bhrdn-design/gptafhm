# Formula Specification & Verification — Tashil al-Afham

## Source inventory (initial)
| Modul | Halaman PDF | Status build |
|---|---:|---|
| Fungsi hitung dasar | 4 | Catatan implementasi |
| Kalender Urfi Jawa/Ajisaka | 5–10 | Belum diaktifkan |
| Kalender Masehi | 11–14 | Belum diaktifkan |
| Kalender Hijriyah | 15–18 | Belum diaktifkan |
| Pranoto Mongso | 19 | Belum diaktifkan |
| Waktu salat & input markaz | 24–26 | Implementasi awal |
| Julian Day | 27–28 | Implementasi awal; contoh perlu audit |
| Data Matahari | 29–31 | Implementasi awal |
| Waktu salat | 32–36 | Implementasi awal; audit wajib |
| Arah Kiblat | 37–40 | Mode Kitab + pembanding bearing |
| Roshdul Kiblat | 41–43 | Implementasi awal; audit wajib |
| Ijtima' & Imkan al-Rukyah | 44 | Tidak dihitung; rumus tidak tersedia |
| Koordinat kota | 45–55 | Belum diimpor; 689 baris perlu verifikasi |

## Temuan audit penting
1. Halaman 28 memuat ketidakkonsistenan angka pada contoh Julian Day. Nilai JDa, JDc, JD, dan T yang tercetak tidak seluruhnya konsisten satu sama lain. Jangan mengubah kalkulasi hanya untuk meniru angka contoh.
2. Halaman 27 menyebut waktu 10:23 GMT dalam langkah JD. Waktu ini harus menjadi input kontekstual, bukan konstanta untuk semua tanggal.
3. Halaman 31–33 perlu rekonsiliasi antara rumus, tabel ringkasan, dan contoh tanggal 22 Oktober 2026.
4. Halaman 39 menuliskan rumus arah kiblat kitab; formula spherical initial bearing disediakan sebagai pembanding terpisah.
5. Halaman 39 menyatakan Roshdul Kiblat tidak memakai ihtiyath demi ketelitian observasi.
6. Halaman 44 hanya memuat daftar judul subbagian, tanpa rumus maupun contoh hitungan.
7. Tabel kota pada halaman 45–55 memuat 689 entri. Beberapa karakter OCR berpotensi salah (contoh nama kota yang mengandung karakter tidak terbaca); seluruh tabel harus diperiksa pada citra halaman sebelum dipakai.

## Release gate
- [ ] Verifikasi rumus dengan ahli falak
- [ ] Reproduksi contoh kitab tanpa memaksa hasil cocok
- [ ] Independent test vectors
- [ ] OCR + visual QA 689 koordinat
- [ ] Unit/integration/E2E tests
- [ ] Accessibility WCAG 2.2 AA
- [ ] Security & privacy review
- [ ] PWA/offline & deployment
