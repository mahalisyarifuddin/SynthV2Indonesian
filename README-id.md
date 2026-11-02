[English](README.md) | **Bahasa Indonesia**

# SynthV2Indonesian
Berkreasi dengan vokal bahasa Indonesia jadi lebih mudah.

## Pengantar
SynthV2Indonesian menambahkan dukungan pelafalan bahasa Indonesia dan terjemahan antarmuka bahasa Indonesia untuk Synthesizer V Studio 2 Pro.

Sebelumnya, membuat vokal bahasa Indonesia memerlukan pemecahan not dan pencampuran pengaturan bahasa antar-not untuk mendapatkan bunyi yang sesuai. Sejak [Synthesizer V Studio 2 Pro 2.3.0](https://dreamtonics.com/synthesizer-v-studio-2-pro-2-3-0-update-and-improvements/), editor mendukung X-SAMPA lintas bahasa secara langsung. Kamus ini memakai sistem tersebut untuk menentukan pelafalan bahasa Indonesia tanpa perlu lagi mencampur pengaturan bahasa.

Dukungan ini dibuat oleh komunitas, bukan mode bahasa Indonesia atau basis data suara resmi yang baru. Kamus ditempatkan di folder bahasa Spanyol, tetapi pelafalannya memakai X-SAMPA.

Repositori ini berisi:
- **`SynthV2Indonesian.json`**: Kamus pelafalan bahasa Indonesia dengan 6.473 entri.
- **`id-id.txt`**: Terjemahan antarmuka bahasa Indonesia.

Repositori ini akan terus hidup dan berkembang mengikuti pembaruan Synthesizer V, dengan perbaikan kamus, perubahan terjemahan, dan penyesuaian kompatibilitas.

## Mulai Cepat / Penggunaan

### Persyaratan
Gunakan **Synthesizer V Studio 2 Pro 2.3.0 atau yang lebih baru**. Menurut Dreamtonics, banyak fitur 2.3.0 memerlukan **suara versi 205**. Perbarui suara yang didukung melalui Product Manager dan periksa ketersediaan pembaruan dari penyedia suara Anda.

### Memasang kamus
1. Unduh [`SynthV2Indonesian.json`](SynthV2Indonesian.json).
2. Tutup Synthesizer V Studio 2, lalu salin berkas ke folder kamus bahasa Spanyol berikut. Buat folder tersebut jika belum ada.

**Windows**
```text
C:\Users\<username>\AppData\Roaming\Dreamtonics\Synthesizer V Studio 2\dicts\spanish
```

**macOS**
```text
/Users/<username>/Library/Application Support/Dreamtonics/Synthesizer V Studio 2/dicts/spanish
```

Ganti `<username>` dengan nama akun Anda.

3. Buka kembali Synthesizer V Studio 2. Atur bahasa not yang akan digunakan ke **Spanish** (bahasa Spanyol), lalu pilih kamus bahasa Indonesia yang sudah dipasang pada panel Dictionary.
4. Aktifkan **Use X-SAMPA symbols** pada panel Dictionary agar entri dibaca sebagai X-SAMPA, bukan fonem sederhana bahasa Spanyol. Opsi yang sama tersedia pada panel Notes untuk melihat dan menyunting fonem not.
5. Masukkan lirik bahasa Indonesia. Periksa fonem yang dihasilkan dan dengarkan hasilnya. Sesuaikan entri kamus atau fonem not jika perlu.

Kamus ini berisi pasangan kata dan pelafalannya, bukan mesin konversi ejaan ke bunyi bahasa Indonesia yang lengkap. Untuk kata yang belum tercakup, tambahkan entri pada panel Dictionary atau masukkan fonem X-SAMPA secara manual. Pemisahan suku kata tetap berguna ketika satu kata dinyanyikan pada beberapa not. Bedanya, Anda tidak perlu lagi memecah not hanya untuk meminjam bunyi dari bahasa lain.

### Memasang terjemahan antarmuka (Windows)
1. Unduh [`id-id.txt`](id-id.txt).
2. Tutup Synthesizer V Studio 2, lalu salin berkas ke:

```text
C:\ProgramData\Dreamtonics\Synthesizer V Studio 2\translations
```

3. Buka kembali editor dan pilih **Bahasa Indonesia** pada pengaturan bahasa antarmuka. Mulai ulang jika diminta. Menyalin berkas ke `ProgramData` mungkin memerlukan izin administrator.

Terjemahan antarmuka dan kamus pelafalan berdiri sendiri. Anda bisa memakai salah satunya tanpa memasang yang lain. Lokasi terjemahan antarmuka di atas berlaku untuk Windows; lokasi macOS dalam README ini hanya mencakup kamus.

## Inventaris Fonem dan Contoh
Kamus yang disertakan memakai **32 token X-SAMPA yang berbeda**. Tabel berikut menggambarkan entri yang ada, termasuk semivokal, hentian glotal, dan varian konsonan letup tanpa pelepasan. Huruf besar dan kecil dibedakan: `j` dan `J` mewakili bunyi yang berbeda. Pisahkan setiap token dengan spasi.

### Vokal
| Token | Bunyi | Contoh dalam kamus | Pelafalan tersimpan |
| --- | --- | --- | --- |
| `a` | a | aku | `a k u` |
| `i` | i | ibu | `i b u` |
| `u` | u | aku | `a k u` |
| `e_o` | e madya (e taling) | enak | `e_o n a k}` |
| `@` | Schwa (e pepet) | empat | `@ m p a t}` |
| `o_o` | o madya | obat | `o_o b a t}` |

Gunakan `e_o` dan `o_o` persis seperti yang tertulis di berkas. Jangan menyingkatnya menjadi `e` dan `o` saat menyalin pelafalan ini.

### Konsonan dan semivokal
| Token | Bunyi / petunjuk ejaan | Contoh dalam kamus | Pelafalan tersimpan |
| --- | --- | --- | --- |
| `p` | p | apa | `a p a` |
| `b` | b | batu | `b a t u` |
| `t` | t | satu | `s a t u` |
| `d` | d | dua | `d u a` |
| `k` | k | kaki | `k a k i` |
| `g` | g | gigi | `g i g i` |
| `tS` | c | cinta | `tS i n t a` |
| `dZ` | j | ajak | `a dZ a k}` |
| `m` | m | mata | `m a t a` |
| `n` | n | nama | `n a m a` |
| `J` | ny | nyanyi | `J a J i` |
| `N` | ng | bunga | `b u N a` |
| `f` | f | afdal | `a f d a l` |
| `s` | s | satu | `s a t u` |
| `z` | z | zaman | `z a m a n` |
| `S` | sy | syukur | `S u k u 4` |
| `x` | kh | khusus | `x u s u s` |
| `h` | h | hari | `h a 4 i` |
| `l` | l | lama | `l a m a` |
| `4` | r ketuk | rasa | `4 a s a` |
| `w` | w / semivokal | waktu | `w a k} t u` |
| `j` | y / semivokal | yakin | `j a k i n` |

### Hentian glotal dan konsonan letup tanpa pelepasan
| Token | Bunyi | Contoh dalam kamus | Pelafalan tersimpan |
| --- | --- | --- | --- |
| `?` | Hentian glotal | berdoa | `b @ 4 d o_o ? a` |
| `p}` | p tanpa pelepasan | atap | `a t a p}` |
| `t}` | t tanpa pelepasan | alat | `a l a t}` |
| `k}` | k tanpa pelepasan | adik | `a d i k}` |

Pelafalan ini merupakan pilihan dalam kamus, bukan pernyataan bahwa semua penutur bahasa Indonesia memakai bunyi yang sama. Konsonan letup di akhir suku kata, vokal, dan kata serapan mungkin perlu disesuaikan dengan pelafalan yang dituju dan suara yang digunakan.

### Coba satu frasa
Kamus memuat setiap kata dalam **aku cinta indonesia**:

| Kata | X-SAMPA |
| --- | --- |
| aku | `a k u` |
| cinta | `tS i n t a` |
| indonesia | `i n d o_o n e_o s i a` |

Untuk memperbaiki atau menambahkan kata, ikuti format kamus yang sudah ada:

```json
{
  "w": "nyanyi",
  "p": "J a J i"
  "phoneset": "xsampa"
}
```

Tempatkan entri di dalam larik `data` pada tingkat teratas berkas JSON. Pastikan JSON tetap valid, termasuk penggunaan koma antar-entri.

## Lisensi
Berkas dukungan bahasa Indonesia dalam repositori ini dilisensikan dengan [Lisensi MIT](LICENSE).

**Synthesizer V © Dreamtonics.** Synthesizer V Studio dan basis data suaranya merupakan produk terpisah yang tunduk pada lisensi masing-masing. Repositori ini tidak memberikan hak atas produk tersebut dan bukan rilis resmi Dreamtonics.

## Kontribusi
Koreksi pelafalan, perbaikan terjemahan, dan pull request dipersilakan. Untuk perubahan kamus, sertakan kata, usulan pelafalan X-SAMPA, dan alasan koreksinya. Untuk laporan kompatibilitas, sertakan versi Synthesizer V dan versi basis data suara yang digunakan.
