# Laporan Praktikum 2: Pemrograman Web - HTML Lanjutan

Nama : Bagas Arya Ramadhan 
Nim : 312510328
Kelas : I251D

---

## Detail Penjelasan Seluruh Kode Program

### 1. Struktur Dokumen Pertama & Tabel Data Mahasiswa

![image alt](https://github.com/Bagas240/Lab2Web./blob/readme/media/Screenshot%202026-10-02%20091700.png?raw=true)
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

![image alt](https://github.com/Bagas240/Lab2Web./blob/readme/media/Screenshot%202026-10-02%20093001.png?raw=true)

- `<caption>Nilai Praktikum</caption>`: Judul resmi yang tampil menempel di atas tabel.
- `<thead>`: Menandai kelompok header tabel.
- `<tbody>`: Menandai kelompok data utama tabel:
  - Baris 1: No `1`, Nama `Andi`, Nilai `85`.
  - Baris 2: No `2`, Nama `Budi`, Nilai `90`.
- `<tfoot>`: Menandai kelompok kaki/footer tabel.
- `colspan="2"`: Atribut untuk menggabungkan 2 kolom menjadi 1 sel horizontal, digunakan pada teks `Rata-rata` agar bersanding rapi dengan nilai `87.5`.

---

### 3. Formulir Registrasi Mahasiswa

![image alt](https://github.com/Bagas240/Lab2Web./blob/readme/media/Screenshot%202026-10-02%20093018.png?raw=true)

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

![image alt](https://github.com/Bagas240/Lab2Web./blob/readme/media/Screenshot%202026-10-02%20093037.png?raw=true)

- `<input type="radio">`: Pilihan opsi tunggal. Atribut `name="jk"` yang bernilai sama mengelompokkan `Laki-laki` (`value="L"`) dan `Perempuan` (`value="P"`), sehingga pengguna hanya bisa memilih salah satu.
- `<input type="checkbox">`: Pilihan opsi ganda. Pengguna dapat mencentang lebih dari satu pilihan keahlian (`HTML`, `CSS`, `JavaScript`) secara bersamaan.

---

### 5. Menu Dropdown (`<select>`) dan Area Teks (`<textarea>`)

![image alt](https://github.com/Bagas240/Lab2Web./blob/readme/media/Screenshot%202026-10-02%20093101.png?raw=true)

- `<select id="prodi" name="prodi">`: Membuat menu pilihan gantung (*dropdown*).
- `<option>`: Menentukan daftar pilihan prodi yang tersedia (`Teknik Komputer` dengan value `si` dan `Sistem Informasi` dengan value `tk`).
- `<textarea>`: Area input teks multi-baris untuk memasukkan alamat lengkap.
  - `rows="5"`: Mengatur tinggi area teks sebesar 5 baris.
  - `cols="40"`: Mengatur lebar area teks sebesar 40 karakter.

---

### 6. Formulir Validasi Dasar HTML5

![image alt](https://github.com/Bagas240/Lab2Web./blob/readme/media/Screenshot%202026-10-02%20093124.png?raw=true)

- `required`: Atribut penanda bahwa input `Nama`, `Email`, dan `Umur` wajib diisi sebelum form dapat dikirim.
- `minlength="3"`: Memvalidasi bahwa jumlah karakter nama yang dimasukkan minimal 3 huruf.
- `type="number"`: Membatasi agar input umur hanya menerima karakter angka.
- `min="17"` & `max="60"`: Membatasi rentang nilai umur yang diizinkan hanya antara 17 hingga 60 tahun.

---

### 7. Structural Semantic HTML5 (Dokumen Kedua)

![image alt](https://github.com/Bagas240/Lab2Web./blob/readme/media/Screenshot%202026-10-02%20093144.png?raw=true)

- `<header>`: Menandai area kepala halaman yang berisi judul utama `Portal Mahasiswa`.
- `<nav>`: Area penampung tautan navigasi situs (`Beranda | Profil | Kontak`).
- `<main>`: Membungkus seluruh konten utama dari halaman portal.
- `<section>`: Membagi konten menjadi kelompok topik tertentu (`Informasi Akademik`).
- `<article>`: Menampung artikel/berita mandiri (`Praktikum HTML Lanjutan`).
- `<aside>`: Menampung informasi sampingan (`Informasi tambahan mahasiswa.`).
- `<footer>`: Area kaki halaman yang berisi pernyataan hak cipta (`© 2026 Tekmik Informatika`).

---

### 8. Elemen Pemutar Multimedia

![iamge alt](https://github.com/Bagas240/Lab2Web./blob/readme/media/Screenshot%202026-10-02%20093157.png?raw=true)

- `<audio controls>`: Menyajikan pemutar media suara untuk memutar berkas `audio.mp3` dengan dukungan format `audio/mpeg`.
- `<video width="320" height="480" controls>`: Menyajikan pemutar video berukuran lebar 320 piksel dan tinggi 480 piksel untuk memutar berkas `video.mp4` (`type="video/mp4"`).
- `controls`: Atribut wajib untuk memunculkan tombol kontrol interaktif bawaan browser (*play*, *pause*, *volume*, *timeline*, dan mode layar penuh).
