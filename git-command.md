# 🚀 Rangkuman Perintah Git (CLI Cheat Sheet)

Catatan perintah dasar Git untuk dokumentasi dan kolaborasi via Terminal Linux.

## 1. Setup Awal (Cuma Sekali)
Perintah untuk mengenalkan identitas kita ke Git dan mengambil repo dari GitHub.

`git config --global user.name "username"`            # Set nama user
`git config --global user.email "email@gmail.com"`    # Set email user
`git clone git@github.com:user/nama-repo.git`         # Download repo via SSH

**Wajib**
`git status`                        # Cek file apa aja yang berubah/belum disimpan
`git add nama-file.md`              # Masukkan 1 file spesifik ke antrean (staging)
`git add .`                         # Masukkan SEMUA file yang berubah ke antrean
`git commit -m "Pesan catatan"`     # Bungkus dan beri label perubahan
`git push`                          # Upload ke GitHub

**collab**
`git pull`                          # Tarik/download update terbaru dari GitHub ke laptop

**Branching**
`git branch`                        # Lihat daftar cabang & posisi kita saat ini (tanda *)
`git checkout -b nama-cabang`       # Buat cabang baru DAN langsung pindah ke situ
`git checkout nama-cabang`          # Pindah ke cabang yang sudah ada (misal: git checkout main)
`git push -u origin nama-cabang`    # Upload cabang baru ke GitHub (cuma saat pertama kali)
`git branch -d nama-cabang`         # Hapus cabang (kalau sudah selesai digabung)

**Merge**
`git checkout main`                 # 1. Pindah dulu ke jalur utama (main)
`git pull`                          # 2. Pastikan main sudah paling update
`git merge nama-cabang`             # 3. Tarik isi 'nama-cabang' masuk ke dalam 'main'
`git push`                          # 4. Upload hasil gabungannya ke GitHub

**Tambahan**
`git log --oneline`                 # Lihat riwayat (history) commit secara singkat
`git diff`                          # Lihat baris teks mana aja yang barusan diubah
`git checkout -- nama-file.md`      # Batalkan perubahan pada file (kembali ke kondisi awal)
