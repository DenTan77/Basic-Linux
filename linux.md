# Pelatihan Linux dan Git

## Tujuan Pelatihan
Setelah mengikuti pelatihan ini, peserta diharapkan mampu:
- Memahami konsep dasar sistem operasi Linux.
- Menggunakan terminal Linux untuk kebutuhan sehari-hari.
- Memahami konsep Version Control System (VCS).
- Menggunakan Git untuk mengelola proyek secara mandiri maupun kolaboratif.
- Menghubungkan repository lokal dengan GitHub.

---

# Materi 1: Pengenalan Linux

## 1. Apa itu Linux?
- Pengertian Linux
- Sejarah singkat Linux
- Distribusi Linux (Ubuntu, Debian, Fedora, Arch)
- Kelebihan Linux
  - Open Source
  - Stabil
  - Aman
  - Banyak digunakan pada server, HPC, AI, dan penelitian

---

## 2. Struktur Direktori Linux

| Direktori | Fungsi |
|-----------|--------|
| `/` | Root Directory |
| `/home` | Folder pengguna |
| `/bin` | Program dasar |
| `/etc` | Konfigurasi sistem |
| `/usr` | Program tambahan |
| `/tmp` | File sementara |
| `/var` | Log dan data aplikasi |
| `/opt` | Software pihak ketiga |

---

## 3. Terminal Linux

- Shell
- Bash
- Zsh
- Perintah dijalankan melalui Terminal

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

### Manajemen Folder

```bash
mkdir folder
```

### Membuat File

```bash
touch file.txt
```

### Menyalin

```bash
cp sumber tujuan
```

### Memindahkan

```bash
mv file tujuan
```

### Menghapus

```bash
rm file
rm -r folder
```

### Melihat Isi File

```bash
cat
less
head
tail
```

### Mencari File

```bash
find . -name "*.txt"
```

### Editor

```bash
nano
vim
```

---

## 5. Permission Linux

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

---

## 6. Package Manager

Ubuntu:

```bash
sudo apt update
sudo apt install git
```

---

## 7. Environment Variable

```bash
echo $PATH
export
```

---

## 8. Latihan Linux

Peserta diminta:
- Membuat folder
- Membuat file
- Mengedit file
- Menyalin file
- Memindahkan file
- Menghapus file

---

# Materi 2: Git

## 1. Apa itu Version Control?

Permasalahan:

```
laporan.docx
laporan_fix.docx
laporan_fix2.docx
laporan_final.docx
```

Git digunakan untuk mengelola perubahan file secara sistematis.

---

## 2. Apa itu Git?

Git adalah Version Control System yang digunakan untuk:
- Menyimpan riwayat perubahan
- Kolaborasi
- Rollback
- Branching

---

## 3. Instalasi Git

```bash
git --version
```

---

## 4. Konfigurasi Git

```bash
git config --global user.name "Nama"
git config --global user.email "email@gmail.com"
git config --list
```

---

## 5. Membuat Repository

```bash
mkdir latihan_git
cd latihan_git
git init
```

---

## 6. Siklus Kerja Git

```
Working Directory
        │
        ▼
    git add
        │
        ▼
   Staging Area
        │
        ▼
   git commit
        │
        ▼
    Repository
```

---

## 7. Menambahkan File

```bash
touch hello.py
git status
```

---

## 8. Staging

```bash
git add hello.py
```

atau

```bash
git add .
```

---

## 9. Commit

```bash
git commit -m "Pesan Commit"
```

---

## 10. Riwayat Commit

```bash
git log
git log --oneline
```

---

## 11. Branch

Membuat branch

```bash
git branch feature
```

Berpindah branch

```bash
git switch feature
```

atau

```bash
git checkout feature
```

---

## 12. Merge

```bash
git merge feature
```

---

## 13. GitHub

Perbedaan:

- Git → Version Control
- GitHub → Hosting Repository
- GitLab → Alternatif GitHub

---

## 14. Clone Repository

```bash
git clone URL
```

---

## 15. Remote Repository

```bash
git remote add origin URL
git remote -v
```

---

## 16. Push

```bash
git push origin main
```

---

## 17. Pull

```bash
git pull origin main
```

---

## 18. Merge Conflict

Contoh:

```text
<<<<<<< HEAD
Hello
=======
Halo
>>>>>>> feature
```

Langkah penyelesaian:
1. Edit konflik.
2. Simpan file.
3. `git add`
4. `git commit`

---

# Mini Project

Peserta diminta:

1. Membuat folder proyek menggunakan Terminal Linux.
2. Membuat beberapa file.
3. Inisialisasi Git.
4. Melakukan beberapa commit.
5. Membuat branch baru.
6. Menambahkan fitur pada branch tersebut.
7. Melakukan merge ke branch utama.
8. Mengunggah repository ke GitHub.

---

# Hasil Akhir

Setelah pelatihan, peserta mampu:
- Menggunakan Terminal Linux.
- Mengelola file melalui command line.
- Memahami konsep Version Control.
- Menggunakan Git untuk pengembangan proyek.
- Berkolaborasi menggunakan GitHub.