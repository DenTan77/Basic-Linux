# Materi 2: Git

## 1. Apa itu Version Control?
Version control adalah cara mengelola perubahan file secara teratur, terutama saat beberapa orang mengerjakan proyek yang sama. Tanpa version control, perubahan file sering menimbulkan kebingungan.

Contoh masalah:

```
laporan.docx
laporan_fix.docx
laporan_fix2.docx
laporan_final.docx
```

Dengan Git, kita bisa melihat siapa yang mengubah apa dan kapan perubahan itu terjadi.

---

## 2. Apa itu Git?
Git adalah Version Control System yang digunakan untuk:
- Menyimpan riwayat perubahan
- Kolaborasi antar pengguna
- Rollback ke versi sebelumnya
- Branching untuk bekerja pada fitur berbeda

Contoh sederhana:
- Saat membuat program, kita bisa menyimpan versi pertama, versi revisi, dan versi terbaru secara teratur.

---

## 3. Instalasi Git

```bash
git --version
```

Contoh output:
```bash
git version 2.40.1
```

---

## 4. Konfigurasi Git

```bash
git config --global user.name "Nama"
git config --global user.email "email@gmail.com"
git config --list
```

Contoh:
```bash
git config --global user.name "Umar"
git config --global user.email "umar@example.com"
```

---

## 5. Membuat Repository

```bash
mkdir latihan_git
cd latihan_git
git init
```

Contoh hasil:
```bash
Initialized empty Git repository in ...
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

Contoh alur:
1. Edit file di folder kerja.
2. Tambahkan file ke staging.
3. Commit perubahan.

---

## 7. Menambahkan File

```bash
touch hello.py
git status
```

Contoh:
```bash
echo 'print("Halo Git")' > hello.py
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

Contoh:
```bash
git add hello.py
# Menambahkan file hello.py ke staging area
```

---

## 9. Commit

```bash
git commit -m "Pesan Commit"
```

Contoh:
```bash
git commit -m "Tambah file hello.py"
```

---

## 10. Riwayat Commit

```bash
git log
git log --oneline
```

Contoh output:
```bash
abc1234 Tambah file hello.py
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

Contoh:
```bash
git switch -c fitur-login
```

---

## 12. Merge

```bash
git merge feature
```

Contoh:
```bash
git switch main
git merge fitur-login
```

---

## 13. GitHub

Perbedaan:

- Git → Version Control
- GitHub → Hosting Repository
- GitLab → Alternatif GitHub

Contoh: kita membuat repo lokal di komputer lalu menguploadnya ke GitHub agar bisa dibagi ke orang lain.

---

## 14. Clone Repository

```bash
git clone URL
```

Contoh:
```bash
git clone https://github.com/user/nama-repo.git
```

---

## 15. Remote Repository

```bash
git remote add origin URL
git remote -v
```

Contoh:
```bash
git remote add origin https://github.com/user/nama-repo.git
```

---

## 16. Push

```bash
git push origin main
```

Contoh:
```bash
git push origin main
# Mengirim perubahan ke GitHub
```

---

## 17. Pull

```bash
git pull origin main
```

Contoh:
```bash
git pull origin main
# Mengambil update terbaru dari GitHub
```

---

## 18. Merge Conflict

Contoh konflik terjadi ketika dua orang mengubah baris yang sama pada file yang sama.

```text
<<<<<<< HEAD
Hello dari saya
=======
Hello dari teman
>>>>>>> feature
```

Langkah penyelesaian:
1. Buka file yang konflik.
2. Edit bagian yang bertabrakan.
3. Simpan file.
4. `git add <nama-file>`
5. `git commit`

---