# Build 0.2.0

- Menambahkan Formula Registry dengan identitas rumus, sumber halaman, versi implementasi, variabel, status, dan catatan pengujian.
- Menambahkan Calculation Comparison untuk dua jenis perbandingan yang memang tersedia pada mesin saat ini.
- Menambahkan Smart Export: pratinjau, PNG, JPG, PDF melalui print-to-PDF, TXT, CSV, dan JSON.
- Mengimpor 1.050 entri koordinat numerik bernama dari sheet `KOTA` workbook XLS. Entri tetap diberi catatan perlu verifikasi sumber.
- Menambahkan PWA manifest dan service worker untuk cache offline dasar.
- Mempertahankan mesin kalkulasi build 0.1.0 dengan status eksperimen/audit; tidak menaikkan status akurasi secara otomatis.
- Menyimpan workbook asli, hasil konversi untuk audit, dan sumber PDF/HTML yang relevan di folder `reference/`.
