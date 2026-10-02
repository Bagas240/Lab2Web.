# Laporan Praktikum 2: Pemrograman Web - HTML Lanjutan

Dokumentasi ini berisi penjelasan menyeluruh dan detail mengenai baris demi baris kode program HTML Lanjutan pada Praktikum 2, mencakup pengolahan Tabel, Formulir Registrasi, Validasi Form, Layout Semantic HTML5, serta Elemen Multimedia.

---

## Detail Penjelasan Seluruh Kode Program

### 1. Struktur Dokumen Pertama & Tabel Data Mahasiswa

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Lanjutan</title>
</head>
<body>

    <h1>Data Mahasiswa</h1>
    <table border="1">
        <tr><th>NIM</th><th>Nama</th><th>Program Studi</th></tr>
        <tr><td>31241001</td><td>Andi</td><td>Teknik Informatika</td></tr>
        <tr><td>31241002</td><td>Budi</td><td>Teknik Informatika</td></tr>
    </table>
```

- `<!DOCTYPE html>`: Deklarasi yang memberi tahu browser bahwa dokumen ini menggunakan standar HTML5.
- `<html lang="en">`: Elemen utama (root) dokumen HTML dengan pengaturan bahasa Inggris.
- `<head>`: Bagian penampung metadata dokumen yang tidak tampil di area konten browser.
- `<meta charset="UTF-8">`: Mengatur pengodean karakter menjadi UTF-8 agar mendukung berbagai simbol standar.
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Mengatur agar tampilan web bersifat responsif pada perangkat seluler.
- `<title>HTML Lanjutan</title>`: Menentukan judul halaman yang muncul pada tab browser.
- `<body>`: Wadah seluruh elemen visual yang ditampilkan kepada pengguna.
- `<h1>Data Mahasiswa</h1>`: Judul utama bagian tabel data mahasiswa.
- `<table border="1">`: Membuat tabel dengan garis batas (*border*) setebal 1 piksel.
- `<tr>`: (*Table Row*) Membuat baris baru di dalam tabel.
- `<th>`: (*Table Header*) Sel header kolom (`NIM`, `Nama`, `Program Studi`). Teks otomatis dicetak tebal (*bold*) dan rata tengah.
- `<td>`: (*Table Data*) Sel penampung data mahasiswa:
  - Baris 1: `31241001`, `Andi`, `Teknik Informatika`.
  - Baris 2: `31241002`, `Budi`, `Teknik Informatika`.

---

### 2. Tabel Nilai Praktikum Berstruktur (`<thead>`, `<tbody>`, `<tfoot>`)

```html
<table border="1">
    <caption>Nilai Praktikum</caption>
    <thead><tr><th>No</th><th>Nilai</th></tr></thead>
    <tbody>
        <tr><td>1</td><td>Andi</td><td>85</td></tr>
        <tr><td>2</td><td>Budi</td><td>90</td></tr>
    </tbody>
    <tfoot><tr><td colspan="2">Rata-rata</td><td>87.5</td></tr></tfoot>
</table>
```

- `<caption>Nilai Praktikum</caption>`: Judul resmi yang tampil menempel di atas tabel.
- `<thead>`: Menandai kelompok header tabel.
- `<tbody>`: Menandai kelompok data utama tabel:
  - Baris 1: No `1`, Nama `Andi`, Nilai `85`.
  - Baris 2: No `2`, Nama `Budi`, Nilai `90`.
- `<tfoot>`: Menandai kelompok kaki/footer tabel.
- `colspan="2"`: Atribut untuk menggabungkan 2 kolom menjadi 1 sel horizontal, digunakan pada teks `Rata-rata` agar bersanding rapi dengan nilai `87.5`.

---

### 3. Formulir Registrasi Mahasiswa

```html
<h1>Form Registrasi Mahasiswa</h1>
<form>
    <label for="nama">Nama Lengkap</label><br>
    <input type="text" id="nama" name="nama"><br><br>
    <label for="email">Email</label><br>
    <input type="email" id="email" name="email"><br><br>
    <label for="password">Password</label><br>
    <input type="password" id="password" name="password"><br><br>
    <label for="tanggal">Tanggal Lahir</label><br>
    <input type="date" id="tanggal" name="tanggal"><br><br>
    <button type="submit">Daftar</button>
    <button type="reset">Reset</button>
</form>
```

- `<form>`: Container utama untuk mengumpulkan masukan dari pengguna.
- `<label for="...">`: Menghubungkan teks keterangan dengan elemen input melalui atribut `id`.
- `<input type="text">`: Kotak pengisian teks nama lengkap.
- `<input type="email">`: Kotak input e-mail yang otomatis memeriksa format penulisan karakter `@`.
- `<input type="password">`: Kotak teks kata sandi yang menyamarkan karakter masukan menjadi titik-titik hitam (`•`).
- `<input type="date">`: Input tanggal lahir yang memunculkan fitur pemilih kalender (*date picker*).
- `<button type="submit">Daftar</button>`: Tombol untuk mengeksekusi pengiriman data form.
- `<button type="reset">Reset</button>`: Tombol untuk mengosongkan seluruh isi formulir ke kondisi semula.

---

### 4. Input Pilihan: Radio Button & Checkbox

```html
<h2>Jenis Kelamin</h2>
<input type="radio" id="laki" name="jk" value="L">
<label for="laki">Laki-laki</label>
<input type="radio" id="perempuan" name="jk" value="P">
<label for="perempuan">Perempuan</label>

<h2>Keahlian</h2>
<input type="checkbox" id="html" name="skill" value="HTML">
<label for="html">HTML</label>
<input type="checkbox" id="css" name="skill" value="CSS">
<label for="css">CSS</label>
<input type="checkbox" id="js" name="skill" value="JavaScript">
<label for="js">JavaScript</label>
```

- `<input type="radio">`: Pilihan opsi tunggal. Atribut `name="jk"` yang bernilai sama mengelompokkan `Laki-laki` (`value="L"`) dan `Perempuan` (`value="P"`), sehingga pengguna hanya bisa memilih salah satu.
- `<input type="checkbox">`: Pilihan opsi ganda. Pengguna dapat mencentang lebih dari satu pilihan keahlian (`HTML`, `CSS`, `JavaScript`) secara bersamaan.

---

### 5. Menu Dropdown (`<select>`) dan Area Teks (`<textarea>`)

```html
<label for="prodi">Program Studi</label>
<select id="prodi" name="prodi">
    <option value="">>-- Pilih Prodi --<</option>
    <option value="si">Teknik Komputer</option>
    <option value="tk">Sistem Informasi</option>
</select>

<br><br>
<label for="alamat">Alamat</label><br>
<textarea id="alamat" name="alamat" rows="5" cols="40"></textarea>
```

- `<select id="prodi" name="prodi">`: Membuat menu pilihan gantung (*dropdown*).
- `<option>`: Menentukan daftar pilihan prodi yang tersedia (`Teknik Komputer` dengan value `si` dan `Sistem Informasi` dengan value `tk`).
- `<textarea>`: Area input teks multi-baris untuk memasukkan alamat lengkap.
  - `rows="5"`: Mengatur tinggi area teks sebesar 5 baris.
  - `cols="40"`: Mengatur lebar area teks sebesar 40 karakter.

---

### 6. Formulir Validasi Dasar HTML5

```html
<form>
    <label for="nama">Nama</label>
    <input type="text" id="nama" name="nama" required minlength="3">

    <label for="email">Email</label>
    <input type="email" id="email" name="email" required>

    <label for="umur">Umur</label>
    <input type="number" id="umur" name="umur" min="17" max="60" required>

    <button type="submit">Kirim</button>
</form>
```

- `required`: Atribut penanda bahwa input `Nama`, `Email`, dan `Umur` wajib diisi sebelum form dapat dikirim.
- `minlength="3"`: Memvalidasi bahwa jumlah karakter nama yang dimasukkan minimal 3 huruf.
- `type="number"`: Membatasi agar input umur hanya menerima karakter angka.
- `min="17"` & `max="60"`: Membatasi rentang nilai umur yang diizinkan hanya antara 17 hingga 60 tahun.

---

### 7. Structural Semantic HTML5 (Dokumen Kedua)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portal Mahasiswa</title>
</head>
<body>
    <header><h1>Portal Mahasiswa</h1></header>
    <nav>
        <a href="#">Beranda</a> |
        <a href="#">Profil</a> |
        <a href="#">Kontak</a>
    </nav>
<main>
    <section>
        <h2>Informasi Akademik</h2>
        <article>
            <h3>Praktikum HTML Lanjutan</h3>
            <p>Mahasiswa mempelajari tabel. form, semantic HTML, multimedia, dan validasi.</p>
        </article>
    </section>
    <aside>Informasi tambahan mahasiswa.</aside>
</main>
<footer><p>&copy; 2026 Tekmik Informatika</p></footer>
```

- `<header>`: Menandai area kepala halaman yang berisi judul utama `Portal Mahasiswa`.
- `<nav>`: Area penampung tautan navigasi situs (`Beranda | Profil | Kontak`).
- `<main>`: Membungkus seluruh konten utama dari halaman portal.
- `<section>`: Membagi konten menjadi kelompok topik tertentu (`Informasi Akademik`).
- `<article>`: Menampung artikel/berita mandiri (`Praktikum HTML Lanjutan`).
- `<aside>`: Menampung informasi sampingan (`Informasi tambahan mahasiswa.`).
- `<footer>`: Area kaki halaman yang berisi pernyataan hak cipta (`© 2026 Tekmik Informatika`).

---

### 8. Elemen Pemutar Multimedia

```html
<h2>Audio</h2>
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    Browser tidak mendukung audio.
</audio>

<h2>Video</h2>
<video width="320" height="480" controls>
    <source src="video.mp4" type="video/mp4">
    Browser tidak mendukung video.  
</video>
</body>
</html>
```

- `<audio controls>`: Menyajikan pemutar media suara untuk memutar berkas `audio.mp3` dengan dukungan format `audio/mpeg`.
- `<video width="320" height="480" controls>`: Menyajikan pemutar video berukuran lebar 320 piksel dan tinggi 480 piksel untuk memutar berkas `video.mp4` (`type="video/mp4"`).
- `controls`: Atribut wajib untuk memunculkan tombol kontrol interaktif bawaan browser (*play*, *pause*, *volume*, *timeline*, dan mode layar penuh).
- *Fallback text*: Pesan teks yang hanya muncul jika browser pengguna tidak mendukung pemutaran media HTML5.

---

## Ringkasan Perubahan & Tampilan Penting pada Browser

1. **Tabel Data & Nilai**: Tampil sebagai kisi-kisi berdinding tebal 1px. Judul kolom berformat tebal di tengah, serta terdapat sel gabungan `colspan` di bagian footer rata-rata.
2. **Form Registrasi & Pilihan**: Teks password tersembunyi sebagai titik hitam, tanggal lahir memiliki pemilih kalender interaktif, radio button hanya bisa dipilih salah satu, dan checkbox bisa dicentang ganda.
3. **Hasil Uji Validasi**: Jika tombol *Kirim* diklik saat form kosong atau saat umur diisi kurang dari 17, browser otomatis menolak pengiriman data dan memunculkan *pop-up* balok pesan peringatan.
4. **Layout Semantic**: Struktur web tersusun secara hirarki rapi dari atas ke bawah (Header, Navigasi, Konten Utama, Sidebar, dan Footer).
5. **Kontrol Multimedia**: Menampilkan pemutar audio dan video interaktif yang siap diputar langsung dari halaman web.
