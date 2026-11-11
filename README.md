<img width="2400" height="820" alt="image" src="https://github.com/user-attachments/assets/f8f2059a-58df-40e3-a579-0d6d5e3ea3fe" />
# Kenali Mens by Fronstellar v2.3

Aplikasi web interaktif berbahasa Indonesia untuk belajar fisiologi siklus menstruasi, termasuk:

- **Header v1.7:** layout dua kolom yang rapi, animasi judul lebih terkendali, dekorasi tidak mengganggu teks, kartu kondisi siklus dengan angka hari lebih jelas, responsif untuk layar kecil
- **Anatomi v1.6:** uterus, tuba uterina, ovarium, serviks, vagina, dan perjalanan oosit secara skematis

- Pengaturan tema **gelap/terang** dan font **Poppins, Inter, DM Sans, Outfit** dari header; pilihan otomatis disimpan di browser (localStorage)
- Slider hari, kontrol autoplay, pilihan kecepatan animasi (0,75×, 1×, 1,5×), dan panjang siklus 24–38 hari
- Linimasa ovarium dan uterus yang saling tersinkronisasi
- Grafik relatif FSH, LH, estradiol, dan progesteron, dengan kurva yang dapat disembunyikan
- Ilustrasi folikel ovarium, ovulasi oosit sekunder, pembentukan dan regresi korpus luteum
- Visual potongan uterus dan skema histologi endometrium (lapisan functionale, basale, kelenjar, dan arteri spiralis)
- Simulasi perdarahan menstruasi H1–H5: aliran darah dan fragmen lapisan functionale melalui kavum uteri dan serviks dengan gerak kontinu tanpa restart antarhari, indikator intensitas skematis, tombol H1–H5, serta replay simulasi otomatis
- Transisi mulus lapisan endometrium, ilustrasi ovarium, indikator hormon, dan penunjuk grafik tanpa kedipan saat hari berubah
- Aksis hipotalamus–hipofisis–ovarium dan referensi ilmiah (tanpa kuis atau rangkuman konsep)

## Pembaruan v2.3: Floating Cycle Controller

Kontrol siklus akan muncul mengambang setelah panel navigasi utama dilewati ketika halaman digulir. Kontrol ini tetap sinkron dengan grafik hormon, siklus ovarium, dan visualisasi uterus/endometrium.

- Geser slider untuk mengubah hari, putar atau jeda, maju/mundur satu hari, serta ubah kecepatan simulasi.
- Klik **⤢** pada kontrol mengambang untuk mengatur lebar dan posisi.
- Pilih preset **kiri bawah, tengah bawah, kanan bawah, kiri atas, tengah atas, kanan atas**, atau **manual**.
- Seret handle **⠿** untuk memilih posisi manual; tekan tombol reset untuk mengembalikan posisi.
- Ukuran, posisi, dan mode ringkas disimpan di penyimpanan lokal browser.
- Fitur kuis, rangkuman konsep, panel validasi oogenesis, dan simulasi perjalanan oosit telah dihapus pada versi sebelumnya.

## Header interaktif v1.4

Judul hero kini muncul per kata dengan gradien bergerak, underline animasi, partikel dekoratif, dan spotlight yang mengikuti kursor. Tombol **Putar ulang judul** dapat mengulang transisi. Semua efek tunduk pada pengaturan **Efek aktif/mati** serta `prefers-reduced-motion`. Tampilan diuji pada desktop, tablet, dan ponsel.

## Pembaruan v1.3: font & motion design

- **15 pilihan font**: Poppins, Inter, DM Sans, Outfit, Plus Jakarta Sans, Manrope, Nunito Sans, Montserrat, Rubik, Lato, Space Grotesk, Source Sans 3, IBM Plex Sans, Quicksand, dan Merriweather (serif).
- **Efek interaktif**: empat kartu navigasi fase, progres siklus, progres scroll, orb animasi, pergerakan gradien, respons hover dan klik, transisi saat menggulir.
- **Tombol efek** di header untuk menonaktifkan animasi dekoratif, menghormati preferensi reduced-motion.
- Tema, font dan preferensi efek tersimpan lokal melalui localStorage, saat izin penyimpanan browser tersedia.
- Tetap satu file `index.html`, tanpa backend. Font Google membutuhkan koneksi internet, jika offline tersedia fallback sistem.

## Pengaturan tampilan

Di header, klik tombol ikon matahari/bulan untuk mengganti tema gelap dan terang. Gunakan menu **Font** untuk memilih tampilan huruf dari 15 pilihan, serta tombol **Efek** untuk mengatur animasi dekoratif. Kedua pengaturan tetap tersimpan ketika halaman dibuka kembali, selama penyimpanan lokal browser diizinkan. Font Google memakai koneksi internet; jika offline, digunakan font pengganti sistem.

## Simulasi perdarahan

Buka bagian **Uterus & lapisan endometrium → Simulasi aliran menstruasi**. Klik **H1, H2, H3, H4, H5** untuk melihat contoh perubahan intensitas, atau klik **Simulasikan H1–H5** untuk memutar seluruh fase. Aliran mereda secara bertahap pada transisi ke hari nonmenstruasi, dan partikel yang terlihat selalu terus bergerak tanpa mulai ulang saat hari diganti. Efek animasi dikurangi saat sistem mengaktifkan *reduced motion*.

Perhatian: grafik intensitas merupakan ilustrasi kualitatif, bukan estimasi jumlah darah atau durasi menstruasi per individu. Pola hari ke-2/3 yang lebih banyak bukan aturan biologis universal.

## Menjalankan

Buka `index.html` di browser modern (Chrome, Edge, atau Firefox). Semua grafik dan ilustrasi menggunakan SVG dan JavaScript native tanpa dependensi runtime. Font Google bersifat opsional; jika offline, browser menggunakan font sistem.

## Publikasi GitHub Pages

1. Gunakan repository `kazadarojat/Kenalimens` yang sudah berisi `index.html`.
2. Buka **Settings → Pages → Build and deployment → Deploy from a branch**.
3. Pilih `main` dan folder `/(root)`, kemudian simpan.

## Publikasi Vercel

Import repository yang memiliki `index.html`, lalu deploy sebagai static site (tanpa build command).

## Catatan ilmiah

Visualisasi menggambarkan pola *rata-rata* siklus ovulatorik tanpa hamil, dan **bukan** kurva laboratorium pada individu. Sumbu hormon menggunakan kadar relatif yang dinormalisasi per hormon; tidak bermakna konsentrasi darah absolut. Model ovulasi kira-kira 14 hari sebelum menstruasi berikutnya, namun waktu ovulasi dan panjang fase luteal dapat bervariasi. Animasi endometrium adalah skema didaktik, bukan estimasi USG atau histopatologi. Jangan digunakan untuk diagnosis, memprediksi masa subur pribadi, atau menentukan kontrasepsi.

### Referensi

- Reed BG, Carr BR. The Normal Menstrual Cycle and the Control of Ovulation. Endotext. https://www.ncbi.nlm.nih.gov/books/NBK279054/
- StatPearls. Physiology, Menstrual Cycle. https://www.ncbi.nlm.nih.gov/books/NBK500020/
- MSD Manual. Menstrual Cycle. https://www.msdmanuals.com/home/women-s-health-issues/biology-of-the-female-reproductive-system/menstrual-cycle
- ACOG. Fertility Awareness-Based Methods of Family Planning. https://www.acog.org/womens-health/faqs/fertility-awareness-based-methods-of-family-planning
