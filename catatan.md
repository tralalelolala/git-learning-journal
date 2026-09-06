Rangkuman Perintah Dasar Git

- git init: Menginisialisasi repositori Git baru di dalam direktori lokal.
- git add <file>: Memasukkan perubahan file ke dalam Staging Area.
- git commit -m "pesan": Menyimpan snapshot perubahan dari Staging Area ke Repository lokal.
- git push: Mengirim commit dari repositori lokal ke remote repository (GitHub/GitLab).
- git pull: Mengambil dan menggabungkan perubahan terbaru dari remote ke repositori lokal.
- git branch <nama-branch>: Membuat cabang baru untuk mengembangkan fitur secara terisolasi.
- git merge <nama-branch>: Menggabungkan branch lain ke dalam branch yang sedang aktif.

Penanganan Merge Conflict Sederhana
Merge conflict terjadi ketika dua branch mengubah baris kode yang sama dan Git tidak tahu mana yang harus dipertahankan. 

Cara menyelesaikannya:
1. Saat terjadi conflict setelah perintah `git merge`, Git akan menandai file yang bermasalah.
2. Buka file tersebut di text editor (seperti VS Code).
3. Cari penanda conflict:
   `<<<<<<< HEAD` (Perubahan di branch saat ini)
   `=======`
   `>>>>>>> nama-branch-lain` (Perubahan dari branch yang digabungkan)
4. Hapus penanda tersebut dan pilih/edit kode mana yang ingin dipertahankan.
5. Simpan file, lalu jalankan:
   `git add <file-yang-conflict>`
   `git commit -m "fix: resolve merge conflict on [nama file]"`