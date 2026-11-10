# TASHIL AL-AFHAM — Digital Falak Platform

Build 0.2.0 · Indonesian interface · local-first web app

## Menjalankan aplikasi

1. Ekstrak `TASHIL_AL_AFHAM_WEB_BUILD_0.2.0.zip`.
2. Masuk ke folder `tashil-al-afham-digital`.
3. Jalankan server lokal, misalnya:

   ```bash
   python -m http.server 8000
   ```

4. Buka `http://localhost:8000` di browser.

Server lokal/HTTPS disarankan untuk fitur GPS dan PWA. Sebagian perhitungan dapat dibuka langsung melalui `index.html`, tetapi browser dapat membatasi GPS dan service worker pada `file://`.

## Fitur pada build 0.2.0

- Dashboard, lokasi manual/GPS, riwayat lokal.
- Julian Day, Data Matahari, Waktu Salat, Arah Kiblat, Roshdul Kiblat (mesin warisan build 0.1.0; status eksperimental/audit).
- Database koordinat dari sheet `KOTA` workbook lama: 1.050 baris bernama dengan koordinat numerik. Data perlu diverifikasi terhadap sumber sebelum dipakai sebagai data otoritatif.
- Formula Registry.
- Calculation Comparison untuk pembanding yang tersedia.
- Smart Export: PNG, JPG, PDF melalui dialog cetak, TXT, CSV, JSON.
- PWA manifest dan cache offline dasar.

## Batasan penting

Build ini adalah fondasi aplikasi yang berjalan, belum seluruh MASTER PROMPT selesai. Mesin multi-kitab Khulashoh, Irsyad al-Murid, Kasyful Qomarain, kalender Hijriyah/Ajisaka, Pranoto Mongso, dan Ijtima' belum seluruhnya diimplementasikan sebagai calculation engine independen. Jangan menggunakan hasil eksperimental sebagai jadwal salat/kalender resmi tanpa verifikasi. Lihat `docs/BUILD-0.2.0-IMPLEMENTATION.md` dan `docs/formula-audit.md`.

## Struktur penting

- `index.html` — aplikasi web.
- `data/cities-workbook.json` — data koordinat hasil ekstraksi sheet KOTA.
- `reference/` — workbook asli, hasil konversi untuk audit, dan dokumen sumber relevan.
- `docs/` — catatan audit dan implementasi.
- `manifest.webmanifest`, `sw.js` — dukungan PWA/offline dasar.
