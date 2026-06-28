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

```bash
pwd
ls
ls -l
ls -a
cd
cd ..
cd ~
```

Contoh:
```bash
pwd
# Menampilkan direktori saat ini

ls
# Melihat isi folder
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
less
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

Hak akses:
- Owner
- Group
- Others

Perintah:

```bash
chmod
chown
```

Contoh:
```bash
chmod 755 file.txt
# Memberi hak akses eksekusi kepada owner dan membaca ke semua pengguna
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

Contoh:
```bash
echo $PATH
export MY_NAME="Deni"
echo $MY_NAME
```

---