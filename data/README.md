# Dataset Construction

The final dataset used by the application is `quran_complete.json`.

## Data Preparation Pipeline
Multiple source datasets containing Arabic text, translations,
and Tafsir were used during preprocessing. These datasets were
cleaned, aligned at the verse level, and merged into a single
normalized JSON structure.

## Final Dataset
- quran_complete.json
  - Arabic Quran text
  - English translation (Sahih International)
  - Urdu translation
  - Tafsir Ibn Kathir (English & Urdu)
  - Surah and Ayah metadata

## Source Datasets
The `sources/` directory contains the original datasets used
only during preprocessing and is not accessed at runtime.
