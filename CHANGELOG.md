# Changelog

## 2026-07-06 — 1.2.0

Penyempurnaan aturan yang sudah ada: deduplikasi, pengecualian, dan nuansa. Bukan penambahan pola baru, melainkan memperhalus yang sudah ada supaya tidak over-edit tulisan yang sebenarnya baik.

### Diubah

- `SKILL.md`
  - **Frontmatter description** ditambah klausa "serta dekorasi kosong seperti emoji berlebihan, label bold di depan kalimat, heading formulaik, dan penutup TLDR yang cuma mengulang isi"
  - **Aturan #10**: contoh "Dengan demikian" dihapus (sudah ada di aturan #7), diganti cross-reference "(lihat aturan #7 soal pembuka paragraf konektor)"
  - **Pemeriksaan Cepat** dirapikan: poin format (emoji, bold+colon, heading, TLDR, bullet) dipisah ke sub-grup bawah dengan mini-title **Format:**; poin non-format tetap di atas
- `references/frasa.md`
  - **Transisi Kosong**: sub-bagian baru "Kapan Transisi Masih Sah" — nuansa untuk "Dengan kata lain", "Artinya", "Pada intinya", "Dengan demikian" dengan uji hapus-kalimat
- `references/struktur.md`
  - **Heading Formulaik**: catatan SEO — heading tanya ("Apa Itu X?") boleh dipakai untuk artikel yang menarget pencarian Google, bukan tanda AI
- `references/terjemahan-kaku.md`
  - **Kata Asing dalam Tanda Kutip**: penjelasan baru "Yang jadi masalah adalah tanda kutipnya, bukan kata asingnya" + uji hapus-kutip; istilah lazim (engagement, retention, deployment) cukup hapus kutipnya, jangan paksa diganti
- `references/contoh.md`
  - **Contoh 11**: em-dash di versi "Sesudah" diganti koma (konsisten dengan aturan #7); ditambah catatan soal "retention" tanpa kutip
  - **Contoh 12**: daftar tiga butir di versi "Sesudah" dipangkas jadi dua butir (konsisten dengan aturan #7 dan Pola Ritme)

## 2026-07-06 — 1.1.0

Tambahan pola yang sebelumnya luput: dekorasi kosong, heading formulaik, dan kata asing dalam tanda kutip. Ini pembaruan quick-win, bukan rilis mayor.

### Ditambahkan

- `references/frasa.md`
  - **Hiasan Tipografi**: emoji beruntun, emoji sebagai bullet, heading dengan emoji, label bold+colon formatter (`**Kesimpulan:**`, `**Catatan:**`, `**Tips:**`)
  - **Transisi Kosong**: "Hal ini menunjukkan bahwa...", "Dengan demikian, ...", "Artinya, ...", "Dengan kata lain, ..." (saat kata-katanya tidak lain), "Yang dimaksud dengan X adalah..."
  - **Penutup Ringkasan**: "TLDR:", "Kesimpulan:" yang cuma restatement, "Takeaway:", "Pesan moral:", "Sebagai penutup, ..."
- `references/struktur.md`
  - **Heading Formulaik**: "Pentingnya X dalam Y", "Apa Itu X?", "5 Tips X", "X untuk Pemula", "X vs Y: Mana yang Lebih Baik?", "Bagaimana X Mengubah Y"
  - **Heading Berlebihan**: heading untuk satu paragraf, heading untuk daftar dua butir, heading tanpa sub-bagian nyata
  - **Daftar Bullet Berlebihan**: bullet untuk hal yang seharusnya paragraf, bullet yang tiap butirnya satu kata sifat
  - **Daftar Tiga Butir + Bold**: penguatan pola tiga butir dengan bold per item
- `references/terjemahan-kaku.md`
  - **Kata Asing dalam Tanda Kutip**: kata Inggris dikutip untuk menandai "konsep asing" ("trust", "impact", "engagement", "traction", "mindset")
- `SKILL.md`: aturan inti #10 ("Buang dekorasi kosong"), delapan pemeriksaan cepat baru
- `references/contoh.md`: Contoh 11 (transisi kosong + penutup TLDR + bold colon) dan Contoh 12 (heading formulaik + bullet pendek + bold tiga butir)

## 2026-07-06 — 1.0.0

Rilis awal. Adaptasi bahasa Indonesia dari [stop-slop](https://github.com/hvpandya/stop-slop) karya Hardik Pandya.

### Diadaptasi dari versi Inggris

- Aturan inti, pemeriksaan cepat, dan rubrik penilaian lima dimensi
- Struktur: kontras biner, daftar negatif, fragmentasi dramatis, setup retoris, agensi palsu, narator dari kejauhan, pola ritme, kata ekstrem malas
- Frasa: pembuka basa-basi, penegas kosong, jargon bisnis, meta-komentar, deklaratif kabur, menyatakan alih-alih menunjukkan

### Baru untuk bahasa Indonesia

- `references/terjemahan-kaku.md`: artikel tak perlu ("sebuah/seorang/para"), "yang mana" dan "di mana" non-lokatif, jiplakan idiom Inggris, "melakukan/memberikan + nomina", redundansi gramatikal ("adalah merupakan"), "hal/tersebut" beruntun, konsistensi register
- Aturan pasif yang diadaptasi: pasif wajar dipertahankan, pasif penghindar dibongkar
- Pembuka zaman ("di era digital"), penutup klise ("Semoga bermanfaat!"), pasangan sinonim redundan ("efektif dan efisien"), bahasa birokrat ("dalam rangka"), konstruksi "secara [sifat]", pembuka paragraf konektor
- 10 contoh sebelum/sesudah berbahasa Indonesia
