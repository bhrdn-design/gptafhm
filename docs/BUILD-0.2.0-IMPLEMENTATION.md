# Tashil al-Afham Digital — Build 0.2.0

## Delivered in this build
- Existing 0.1.0 web application retained as the base.
- Formula Registry with IDs, source page references, implementation versions, variables, statuses and test notes.
- Calculation Comparison for available independent calculations: Gregorian vs Julian calendar convention in JD, and Mode Kitab vs spherical bearing for Qibla.
- Smart Export: PNG, JPG, print-to-PDF, TXT, CSV and JSON; report snapshot, selectable content and preview.
- Imported 1,050 named numeric coordinate rows from the uploaded workbook sheet `KOTA` into `data/cities-workbook.json`. These are imported source values, not certified verified coordinates.
- PWA manifest and service worker for basic offline caching when served over HTTPS/localhost.
- Branding remains TASHIL AL-AFHAM.

## Source workbook audit
The legacy XLS was opened and converted with LibreOffice for inspection. It contains 21 worksheets, including `input`, `HAROKAT_HAKIKI`, multiple ijtima calculation sheets, `ارشاد المريد`, `Data Taqribi`, `KOTA`, `Takdil Hakiki`, and logarithm tables. Formula cells and cross-sheet references are present. The original XLS is retained in `reference/`. The workbook has not been migrated wholesale into production calculation engines; that requires sheet-by-sheet formula mapping and regression cases.

## Not yet production-verified
- The existing JD, solar, prayer, qibla and rashdul engines retain their prior experimental status.
- Hijri, Ajisaka, Pranoto Mongso and ijtima calculation engines are not yet activated.
- Khulashoh, Irsyad al-Murid and Kasyful Qomarain are not yet complete independently selectable production engines.
- No claim of expert approval, 100% accuracy, or official calendar/prayer-time status is made.
- Authentication, cloud database/sync, multi-user roles, automated E2E tests and deployment configuration remain future work.

## Run
Serve this folder via localhost or HTTPS (recommended for GPS and PWA). Opening `index.html` directly works for most local calculations, but browser restrictions may prevent GPS and service-worker features.
