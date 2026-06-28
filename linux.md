# Pelatihan Linux dan Git

## Tujuan Pelatihan
Setelah mengikuti pelatihan ini, peserta diharapkan mampu:
- Memahami konsep dasar sistem operasi Linux.
- Menggunakan terminal Linux untuk kebutuhan sehari-hari.
- Menghubungkan repository lokal dengan GitHub.

---

# Materi 1: Pengenalan Linux

## 1. Apa itu Linux?
Secara umum, Linux adalah sistem operasi yang digunakan untuk mengelola perangkat keras dan menjalankan aplikasi. Linux termasuk sistem operasi open-source yang banyak dipakai karena stabil, aman, dan fleksibel. Sistem ini sering digunakan pada server, laptop, komputer desktop, hingga perangkat embedded.

Contoh sederhana:
- Saat membuka aplikasi di komputer, Linux membantu sistem menjalankan program tersebut.
- Banyak website besar memakai Linux karena handal dan aman.

Beberapa hal penting tentang Linux:
- Pengertian Linux: sistem operasi berbasis kernel Linux.
- Sejarah singkat Linux: berkembang dari sistem Unix dan diperkenalkan secara luas oleh Linus Torvalds.
- Distribusi Linux: Ubuntu, Debian, Fedora, dan Arch adalah contoh distribusi yang berbeda sesuai kebutuhan pengguna.
- Kelebihan Linux:
  - Open Source
  - Stabil
  - Aman
  - Banyak digunakan pada server, HPC, AI, dan penelitian

---

## 2. Struktur Direktori Linux
Secara umum, Linux memiliki struktur folder yang terorganisir untuk menyimpan file sistem, konfigurasi, dan data pengguna.

| Direktori | Fungsi |
|-----------|--------|
| `/` | Root Directory, bagian paling atas dari sistem |
| `/home` | Folder pengguna, tempat file pribadi |
| `/bin` | Program dasar yang penting untuk sistem |
| `/etc` | Konfigurasi sistem |
| `/usr` | Program tambahan dan pustaka |
| `/tmp` | File sementara |
| `/var` | Log dan data aplikasi |
| `/opt` | Software pihak ketiga |

Contoh: file dokumentasi pengguna biasanya ada di `/home/nama_pengguna`.

---

## 3. Terminal Linux
Terminal adalah antarmuka untuk menjalankan perintah pada Linux. Biasanya pengguna mengakses sistem melalui shell seperti Bash atau Zsh.

Contoh aktivitas di terminal:
- Melihat isi folder
- Membuat file baru
- Menginstall aplikasi
- Mengelola sistem

---

## 4. Perintah Dasar Linux

### Navigasi
Perintah navigasi digunakan untuk berpindah dan melihat posisi folder serta isi folder di Linux.

```bash
pwd
ls
ls -l
ls -a
cd
cd ..
cd ~
```

Penjelasan perintah:
- `pwd` : menampilkan lokasi direktori saat ini.
- `ls` : melihat isi folder saat ini.
- `ls -l` : melihat isi folder dalam format lengkap, termasuk hak akses, pemilik, dan tanggal modifikasi.
- `ls -a` : melihat semua file termasuk file tersembunyi.
- `cd` : masuk ke home directory pengguna.
- `cd ..` : kembali ke folder satu tingkat di atas.
- `cd ~` : kembali ke direktori home pengguna.

Contoh:
```bash
pwd
# Menampilkan direktori saat ini

ls
# Melihat isi folder

cd Documents
# Masuk ke folder Documents

cd ..
# Kembali ke folder sebelumnya
```

### Manajemen Folder

```bash
mkdir folder
```

Contoh:
```bash
mkdir latihan
# Membuat folder bernama latihan
```

### Membuat File

```bash
touch file.txt
```

Contoh:
```bash
touch catatan.txt
# Membuat file kosong bernama catatan.txt
```

### Menyalin

```bash
cp sumber tujuan
```

Contoh:
```bash
cp catatan.txt /home/user/Documents/
```

### Memindahkan

```bash
mv file tujuan
```

Contoh:
```bash
mv catatan.txt latihan/
```

### Menghapus

```bash
rm file
rm -r folder
```

Contoh:
```bash
rm catatan.txt
rm -r latihan
```

### Melihat Isi File

```bash
cat
head
tail
```

Contoh:
```bash
cat file.txt
head -10 file.txt
tail -10 file.txt
```

### Mencari File

```bash
find . -name "*.txt"
```

Contoh:
```bash
find . -name "*.md"
# Mencari semua file berakhiran .md di direktori saat ini
```

### Editor

```bash
nano
vim
```

Contoh:
```bash
nano catatan.txt
```

---

## 5. Permission Linux
Linux menggunakan sistem izin untuk mengatur siapa yang boleh membaca, menulis, atau mengeksekusi file.

Konsep:

```
rwxr-xr-x
```

Arti tiap bagian:
- `r` = read (bisa membaca)
- `w` = write (bisa menulis/merubah)
- `x` = execute (bisa dijalankan)

Hak akses:
- Owner : pemilik file
- Group : pengguna dalam kelompok yang sama
- Others : pengguna lain di sistem

Perintah:

```bash
chmod
chown
```

Penjelasan angka pada `chmod`:
- Angka pertama untuk owner
- Angka kedua untuk group
- Angka ketiga untuk others

Nilai masing-masing:
- `4` = read
- `2` = write
- `1` = execute
- `0` = tidak ada hak

Contoh kombinasi:
- `755` = owner mendapat `7` (`4+2+1`), group `5` (`4+1`), others `5` (`4+1`)
- `644` = owner `6` (`4+2`), group `4`, others `4`
- `700` = owner penuh akses, group dan others tidak punya akses

Contoh:
```bash
chmod 755 file.txt
# Memberi hak akses penuh kepada owner, dan hanya read/execute untuk group serta others
```

Contoh lain:
```bash
chmod 644 file.txt
# Biasanya dipakai untuk file biasa yang tidak dieksekusi
```

---

## 6. Package Manager
Package manager digunakan untuk menginstall dan mengelola perangkat lunak.

Ubuntu:

```bash
sudo apt update
sudo apt install git
```

Contoh:
```bash
sudo apt install nginx
# Menginstall web server nginx
```

---

## 7. Environment Variable
Environment variable adalah variabel yang menyimpan informasi sistem, seperti lokasi program yang dapat dijalankan.

```bash
echo $PATH
export
```

Penjelasan:
- `echo` digunakan untuk menampilkan nilai dari sebuah variabel atau teks ke terminal.
- `export` digunakan untuk membuat variabel menjadi tersedia untuk proses atau shell lain dalam sesi yang sedang berjalan.

Contoh:
```bash
echo $PATH
# Menampilkan daftar lokasi program yang bisa dijalankan

export MY_NAME="Farhan"
# Membuat variabel MY_NAME dengan nilai Deni

echo $MY_NAME
# Menampilkan nilai variabel MY_NAME
```

---