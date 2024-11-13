# Forum

> Proyek dibuat oleh Nicky Jonathan Purba

## Daftar Isi
- Struktur Proyek
- Persiapan
- Menjalankan Server

## Struktur Proyek

/
	server/                     Server terdapat di sini
		server.go
	static/                     File HTML terdapat di sini
		assets/                 Memuat semua gambar atau file lainnya
			profile/            Memuat semua gambar profil termasuk gambar default
				default.png
		css/                    File CSS
			admin/              File CSS untuk halaman admin
			user/               File CSS untuk halaman pengguna dan autentikasi
			...
		error/                  Halaman error 404
			/404.html
		js/                     Memuat semua file JavaScript
			user/               JS untuk halaman pengguna dan autentikasi
			...
		layout/                 File layout, bertindak sebagai template untuk setiap halaman
			base.html
		pages/                  Memuat semua halaman HTML
			admin/              Halaman untuk admin
			user/               Halaman untuk pengguna dan autentikasi
			...
	handler.go                  File Golang untuk menangani dan merender setiap halaman
	structures.go               File Golang untuk menyimpan struktur (digunakan untuk mengirim atau menerima data ke halaman)
	utils.go                    Semua fungsi yang berguna

## Persiapan
Untuk mempersiapkan forum, pertama-tama Anda perlu mengkloning repository ini.
Kemudian, instal sqlite3 dan jalankan file `forum.sql` di terminal.
Ini akan membuat semua tabel pada basis data Anda.

## Menjalankan Server
Untuk menjalankan server, buka terminal dan arahkan ke direktori root proyek.
Kemudian jalankan perintah `go run ./server/server.go`.
