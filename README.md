# Stop Slop (Bahasa Indonesia)

Skill untuk menghapus ciri khas tulisan AI dari prosa berbahasa Indonesia.

## Apa Ini

Tulisan AI punya pola: frasa yang itu-itu saja, struktur yang tertebak, ritme metronom. Skill ini mengajari Claude (atau LLM lain) menangkap dan membuang pola tersebut dari teks berbahasa Indonesia.

Ini adaptasi dari [stop-slop](https://github.com/hvpandya/stop-slop) karya Hardik Pandya, bukan terjemahan mentah. Slop berbahasa Indonesia berbeda dari slop berbahasa Inggris, jadi isinya pun berbeda.

## Kenapa Bukan Sekadar Terjemahan

1. **Terjemahan kaku adalah slop terbesar dalam bahasa Indonesia.** AI sering berpikir dalam bahasa Inggris lalu menuliskannya dengan kata Indonesia: "sebuah kesempatan", "yang mana", "situasi di mana", "memiliki kemampuan untuk". Versi Inggris tidak mengenal masalah ini; versi ini menaruhnya di file referensi tersendiri.

2. **Aturan pasif harus diadaptasi.** Versi Inggris melarang kalimat pasif total. Dalam bahasa Indonesia, pasif di- adalah tata bahasa inti dan sering jadi pilihan paling wajar ("Jembatan itu dibangun tahun 1912"). Yang dilarang di sini hanya pasif penghindar: "dapat disimpulkan bahwa", "perlu dilakukan kajian", "telah terjadi kesalahan".

3. **Bahasa Indonesia punya klisenya sendiri.** "Di era digital yang serba cepat ini", "tidak hanya... tetapi juga", "efektif dan efisien", "Semoga artikel ini bermanfaat!". Semuanya terdokumentasi di file referensi.

4. **Aturan adverbia diterjemahkan konsepnya, bukan katanya.** Bahasa Indonesia tidak punya akhiran -ly, tapi punya padanannya: penguat kosong ("sangat", "benar-benar"), pelemah ragu-ragu ("cukup", "agak"), dan konstruksi "secara [sifat]".

## Struktur Skill

```
stop-slop-id/
├── SKILL.md                    # Instruksi inti
├── references/
│   ├── frasa.md                # Frasa yang harus dihapus
│   ├── struktur.md             # Pola struktural yang harus dihindari
│   ├── terjemahan-kaku.md      # Anglicisme, aturan pasif, register
│   └── contoh.md               # 10 transformasi sebelum/sesudah
├── README.md
├── CHANGELOG.md
└── LICENSE
```

## Cara Pakai

**Claude.ai:** unggah file `stop-slop-id.skill` ke percakapan, lalu klik tombol **Save skill** pada kartu file (tersedia jika akunmu mengizinkan pembuatan skill). Setelah terpasang, Claude memakainya otomatis saat menulis atau menyunting teks berbahasa Indonesia.

**Claude Code:** salin folder ini ke direktori skill, misalnya `~/.claude/skills/stop-slop-id/`.

**Claude Projects:** unggah `SKILL.md` beserta isi folder `references/` ke project knowledge.

**Custom instructions / API:** salin bagian "Aturan Inti" dari `SKILL.md` ke system prompt. File referensi dimuat sesuai kebutuhan.

## Yang Ditangkap

**Frasa terlarang** (`references/frasa.md`): pembuka basa-basi ("Berikut adalah", "Perlu diketahui bahwa"), pembuka zaman ("Di era digital saat ini"), penegas kosong ("Camkan itu"), penguat dan pelemah hampa ("sangat", "benar-benar", "cukup"), konstruksi "secara [sifat]", jargon bisnis ("menavigasi", "sinergi", "holistik"), bahasa birokrat ("dalam rangka", "adapun"), meta-komentar ("Yuk, simak penjelasannya!"), penutup klise ("Semoga bermanfaat!"), deklaratif kabur ("Dampaknya sangat besar"), dekorasi kosong (emoji beruntun, label `**Kesimpulan:**`, transisi "Hal ini menunjukkan bahwa..."), penutup TLDR yang cuma meringkas ulang.

**Klise struktural** (`references/struktur.md`): kontras biner ("tidak hanya... tetapi juga"), daftar negatif, fragmentasi dramatis, setup retoris ("Pernahkah Anda...?"), agensi palsu ("keputusan itu muncul dengan sendirinya"), narator dari kejauhan ("Orang-orang cenderung..."), paragraf yang selalu dibuka konektor, pola ritme (daftar tiga butir, em-dash, daftar tiga butir + bold), kata ekstrem malas, pasangan sinonim redundan, heading formulaik ("Pentingnya X", "Apa Itu X?"), heading berlebihan, daftar bullet untuk hal yang seharusnya paragraf.

**Penyakit khas Indonesia** (`references/terjemahan-kaku.md`): "sebuah/seorang/para" berlebihan, "yang mana" dan "di mana" non-lokatif, pasif penghindar vs. pasif wajar, jiplakan idiom Inggris ("ketika berbicara tentang", "memainkan peran penting"), "melakukan/memberikan + nomina" ("melakukan analisis" → "menganalisis"), redundansi gramatikal ("adalah merupakan", "agar supaya"), "hal/tersebut" beruntun, kata asing dalam tanda kutip ("trust", "impact", "engagement"), konsistensi register (Anda/kamu/lo).

## Penilaian

Nilai 1-10 untuk tiap dimensi:

| Dimensi | Pertanyaan |
|---------|------------|
| Kelugasan | Pernyataan atau pengumuman? |
| Ritme | Bervariasi atau monoton? |
| Kepercayaan | Menghargai kecerdasan pembaca? |
| Kealamian | Terdengar seperti manusia, dan seperti bahasa Indonesia (bukan terjemahan)? |
| Kepadatan | Masih ada yang bisa dipangkas? |

Di bawah 35/50: revisi.

## Contoh Singkat

**Sebelum:**
> "Di era digital yang serba cepat ini, tidak dapat dipungkiri bahwa media sosial memainkan peran yang sangat penting dalam kehidupan sehari-hari kita."

**Sesudah:**
> "Rata-rata orang Indonesia membuka media sosial lebih dari tiga jam sehari."

Sebelas contoh lain ada di `references/contoh.md`.

## Kredit

Adaptasi bahasa Indonesia dari [stop-slop](https://github.com/hvpandya/stop-slop) karya [Hardik Pandya](https://hvpandya.com).

## Lisensi

MIT. Pakai bebas, sebarkan luas.
