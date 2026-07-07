---
name: stop-slop-id
description: Hilangkan pola tulisan AI (AI slop) dari prosa berbahasa Indonesia dan buat teks terdengar ditulis manusia. Gunakan setiap kali menulis, menyunting, menerjemahkan ke, atau mereview teks berbahasa Indonesia apa pun (artikel, esai, caption, naskah, email, laporan, copywriting), meski pengguna tidak menyebut "slop" — termasuk permintaan "humanize", "biar gak kedengaran kayak AI", "bikin lebih natural", atau meniru gaya dari sampel tulisan pengguna. Menangkap frasa klise ("tidak hanya... tetapi juga", "di era digital"), terjemahan kaku, pasif tanpa pelaku, atribusi kabur ("para ahli sepakat"), signifikansi menggelembung ("menandai babak baru"), bahasa promosi, angka/sumber karangan, residu chatbot ("Semoga membantu!"), sinonim redundan, jargon bisnis, struktur formulaik, dan dekorasi kosong (emoji beruntun, label bold, heading formulaik, penutup TLDR). Remove AI writing patterns from Indonesian prose and humanize AI-sounding text; use when drafting, editing, or reviewing any Indonesian text.
metadata:
  version: 2.0.0
  trigger: Menulis prosa, menyunting draf, atau mereview tulisan berbahasa Indonesia
  language: id
  adapted_from: stop-slop oleh Hardik Pandya (https://hvpandya.com); sebagian pola dari humanizer oleh Siqi Chen (https://github.com/blader/humanizer) yang berbasis Wikipedia "Signs of AI writing"
---

# Stop Slop (Bahasa Indonesia)

Hilangkan pola tulisan AI yang mudah ditebak dari prosa berbahasa Indonesia.

Skill ini adaptasi dari stop-slop versi Inggris, bukan terjemahan mentah. Slop berbahasa Indonesia punya penyakit sendiri: terjemahan kaku dari bahasa Inggris, pasif birokratis yang menyembunyikan pelaku, pasangan sinonim redundan, dan penutup blog klise. Aturan di bawah menangani keduanya, pola universal dan pola khas Indonesia.

## Cara Kerja

Tentukan dulu mode dari permintaan pengguna:

1. **Menulis baru** — terapkan semua aturan sejak draf pertama. Panjang mengikuti kebutuhan isi.
2. **Menyunting draf** — buang slopnya, pertahankan cakupannya. Kalau draf aslinya lima paragraf berisi lima gagasan, hasil suntingan tetap membawa kelima gagasan itu; boleh lebih padat, tapi tidak boleh ada isi yang hilang. Menyunting berarti membuang lemak, bukan memotong daging. Ikuti suara penulisnya: kalau pengguna memberi sampel tulisannya, baca dan tiru gayanya. Lihat [references/suara.md](references/suara.md).
3. **Mereview** — laporkan pola yang ditemukan beserta lokasinya. Jangan menulis ulang kecuali diminta.

Untuk teks yang panjang atau penting, kerjakan dua putaran: tulis draf, lalu tanya diri sendiri "apa yang masih bikin teks ini kedengaran seperti AI?", dan bereskan sisa temuannya sebelum diserahkan.

## Batas Keras: Spesifik ≠ Mengarang

Aturan "ganti klaim kabur dengan angka" bukan izin menciptakan angka. Kalau data, nama, kutipan, atau sumber tidak tersedia dari pengguna atau bahan yang diberikan:

- Jangan tulis angka fiktif ("naik 40%") atau sumber fiktif ("menurut studi Harvard 2023"). Tulisan bebas slop tapi berisi fakta palsu lebih buruk daripada slop.
- Pilih salah satu: tanya pengguna, pakai penanda `[angka]` / `[butuh sumber]`, atau tulis klaim jujur tanpa angka ("penjualan turun" jujur; "penjualan turun 18%" yang dikarang adalah kebohongan).
- Angka pada [references/contoh.md](references/contoh.md) hanya ilustrasi teknik, bukan ajakan mengarang.

## Aturan Inti

1. **Buang basa-basi pembuka.** Hapus pembuka pengumuman ("Berikut adalah", "Perlu diketahui bahwa"), pembuka zaman ("Di era digital yang serba cepat ini"), penegas kosong, serta penguat dan pelemah hampa ("sangat", "benar-benar", "cukup", "secara signifikan"). Lihat [references/frasa.md](references/frasa.md).

2. **Bongkar struktur formulaik.** Hindari kontras biner ("tidak hanya X, tetapi juga Y"), daftar negatif, fragmentasi dramatis, setup retoris ("Pernahkah Anda...?"), dan agensi palsu. Lihat [references/struktur.md](references/struktur.md).

3. **Tunjuk pelakunya.** Kalimat pasif di- itu sah dalam bahasa Indonesia; jangan diberantas membabi buta. Yang harus dibongkar: pasif yang dipakai untuk bersembunyi. "Dapat disimpulkan bahwa": siapa yang menyimpulkan? "Perlu dilakukan kajian": oleh siapa? Sebut pelakunya. Lihat [references/terjemahan-kaku.md](references/terjemahan-kaku.md).

4. **Tulis bahasa Indonesia, bukan terjemahan.** Buang jiplakan struktur Inggris: "sebuah" di mana-mana, "yang mana", "di mana" bukan untuk tempat, "memiliki kemampuan untuk", "ketika berbicara tentang", "melakukan analisis". Lihat [references/terjemahan-kaku.md](references/terjemahan-kaku.md).

5. **Spesifik.** Deklaratif kabur ("Dampaknya sangat besar") diganti isi konkret: sebutkan dampaknya. Kata ekstrem malas ("semua orang", "selalu", "tidak pernah") diganti angka atau contoh. Pasangan sinonim redundan ("efektif dan efisien", "aman dan nyaman") dipangkas: pilih satu, atau ganti dengan fakta.

6. **Ajak pembaca masuk.** "Kamu" atau "Anda" mengalahkan "orang-orang", "masyarakat", "para pengguna". Pilih satu register dan konsisten sepanjang teks. Detail konkret mengalahkan abstraksi.

7. **Variasikan ritme.** Campur panjang kalimat. Dua butir lebih kuat daripada tiga. Jangan buka setiap paragraf dengan konektor ("Selain itu", "Di sisi lain", "Dengan demikian"). Akhiri paragraf dengan cara berbeda-beda. Tanpa em-dash.

8. **Percayai pembaca.** Nyatakan fakta langsung. Buang pelunak, pembenaran, dan bimbingan berlebihan. Tanpa "Semoga bermanfaat!", tanpa "Jadi, tunggu apa lagi?", tanpa kesimpulan yang cuma mengulang isi.

9. **Coret kalimat pajangan.** Kalau bunyinya seperti kutipan motivasi untuk diunggah ke media sosial, tulis ulang jadi kalimat kerja biasa.

10. **Buang dekorasi kosong.** Emoji beruntun, label `**Kesimpulan:**` / `**Catatan:**` / `**Tips:**` di depan kalimat, transisi kosong ("Hal ini menunjukkan bahwa...", "Artinya, ..."), heading formulaik ("Pentingnya X", "Apa Itu X?"), dan penutup TLDR yang cuma meringkas ulang tidak menambah makna. Hapus, atau ganti dengan isinya. Untuk konektor pembuka paragraf seperti "Dengan demikian", lihat aturan #7. Selengkapnya di [references/frasa.md](references/frasa.md) dan [references/struktur.md](references/struktur.md).

11. **Sebut sumbernya.** Atribusi kabur ("para ahli sepakat", "banyak penelitian menunjukkan", "menurut sejumlah sumber") diganti sumber bernama: siapa, kapan. Signifikansi menggelembung ("menandai babak baru", "memainkan peran krusial") diganti kejadiannya. Tidak punya sumber? Turunkan klaim atau tandai `[butuh sumber]` — jangan karang (lihat Batas Keras). Lihat [references/frasa.md](references/frasa.md).

12. **Hidupkan, jangan cuma sterilkan.** Teks yang lolos semua aturan di atas masih bisa mati: semua kalimat seragam, tanpa pendirian, tanpa penulis di baliknya. Untuk esai, blog, dan opini, beri sudut pandang dan biarkan sedikit berantakan; untuk dokumentasi, berita lugas, dan teks hukum, netral memang suara yang benar. Jangan pula overkoreksi tulisan manusia yang sehat: cari gugusan ciri, bukan satu ciri. Lihat [references/suara.md](references/suara.md).

## Pemeriksaan Cepat

Sebelum menyerahkan tulisan:

- Ada "tidak hanya... tetapi juga"? Nyatakan keduanya langsung, atau pilih yang penting.
- Ada "sangat", "benar-benar", atau "secara [sifat]"? Hapus, atau ganti dengan kata yang memang kuat.
- Ada "sebuah"/"seorang"/"para" yang bisa dihapus tanpa mengubah makna? Hapus.
- Ada "yang mana", atau "di mana" bukan untuk tempat? Tulis ulang kalimatnya.
- Pasif tanpa pelaku ("dapat disimpulkan", "perlu dilakukan", "diharapkan agar")? Sebut siapa.
- Pembuka "Di era...", "Dalam dunia...", "Seiring perkembangan..."? Potong, mulai dari inti.
- "Berikut adalah"? Langsung sebutkan isinya.
- Pasangan sinonim ("efektif dan efisien")? Pilih satu.
- Tiga kalimat berturut-turut sama panjang? Pecah salah satunya.
- Setiap paragraf dibuka konektor? Variasikan atau hapus konektornya.
- Ada em-dash? Ganti koma atau titik.
- Semua paragraf ditutup kalimat pamungkas? Variasikan.
- Deklaratif kabur ("Implikasinya luas")? Sebutkan implikasinya.
- "Hal ini"/"hal tersebut" beruntun? Sebut bendanya langsung.
- Penutup "Semoga bermanfaat", "Selamat mencoba", "tunggu apa lagi"? Hapus.
- Register campur ("Anda" + "kamu" + "lo" dalam satu teks)? Pilih satu.
- "Hal ini menunjukkan bahwa..." / "Artinya, ..." / "Dengan kata lain, ..." (yang cuma mengulang)? Hapus atau gabung kalimat.
- Kata Inggris dalam tanda kutip ("trust", "impact")? Hapus kutipnya; ganti padanan hanya jika memang ada yang jelas.
- Atribusi kabur ("para ahli", "banyak studi menunjukkan")? Sebut siapa dan kapan, atau turunkan klaimnya.
- Ada angka, nama, atau sumber yang tidak ada di bahan? Hapus atau tandai `[butuh sumber]`. Jangan karang.
- "Menandai babak baru" / "memainkan peran krusial" / "menjadi bukti komitmen"? Ganti kejadian konkretnya.
- "Hadir sebagai" / "berdiri sebagai" / "menjelma menjadi"? Ganti "adalah", atau sebut fungsinya.
- "Mulai dari X hingga Y" yang bukan skala nyata? Sebut daftarnya langsung.
- Satu benda dipanggil tiga nama berbeda (pengguna/pemakai/konsumen)? Pilih satu, ulangi saja.
- Residu chatbot ("Tentu! Berikut...", "Semoga membantu!", "Beri tahu saya jika...")? Hapus.
- Nada brosur di teks non-iklan ("memukau", "wajib dikunjungi", "surga tersembunyi")? Ganti fakta.
- Kalau menyunting: ada gagasan dari draf asli yang hilang? Kembalikan.

**Format:**

- Emoji beruntun atau sebagai bullet? Hapus.
- Label bold di depan kalimat (`**Kesimpulan:**`, `**Catatan:**`, `**Tips:**`)? Ganti kalimat biasa.
- Heading gaya "Apa Itu X?" / "Pentingnya X" / "5 Tips X"? Pertimbangkan hindari (kecuali untuk SEO, lihat aturan #10 dan catatan di [references/struktur.md](references/struktur.md)).
- Heading diikuti satu kalimat pemanas yang cuma mengulang heading? Hapus kalimatnya.
- Penutup "TLDR:" / "Kesimpulan:" yang cuma mengulang isi? Hapus.
- Daftar bullet yang tiap butirnya satu kata sifat atau bisa digabung jadi satu kalimat? Tulis paragraf.

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

## Contoh

Lihat [references/contoh.md](references/contoh.md) untuk transformasi sebelum/sesudah.

## Lisensi

MIT. Adaptasi dari [stop-slop](https://github.com/hvpandya/stop-slop) karya Hardik Pandya. Sebagian pola (atribusi kabur, signifikansi menggelembung, bahasa promosi, rentang palsu, sinonim bergilir, residu chatbot, kalibrasi suara, panduan anti-overkoreksi) diadaptasi dari [humanizer](https://github.com/blader/humanizer) karya Siqi Chen, yang berbasis halaman Wikipedia "Signs of AI writing".
