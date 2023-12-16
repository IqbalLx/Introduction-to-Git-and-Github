# Sinkronisasi Perubahan

## Gambaran Besar Proses Sinkronisasi Perubahan

![Git Changes Sync](../assets/git_changes_sync.png)

Diagram diatas adalah versi update dari diagram pada modul sebelumnya, dimana sekarang GitHub muncul untuk pertama kalinya.

## Mengintegrasikan Lokal Repo dengan GitHub Repo

Untuk memberikan informasi GitHub repo kepada lokal git repo kita, langkah pertama adalah mendapatkan url github repo kita dengan cara

1. Buka Github kalian pada browser, lalu buka repository yang telah kalian pada modul 1
2. Pada sebelah kiri deskripsi repo, kalian akan menemukan tombol hijau berjudul `Code`, klik, lalu geser pada tab SSH
   ![GitHub Get URL](../assets/github_get_url.png)
3. Copy url tersebut lalu, gunakan command berikut
   ```
   $ git remote add origin <url github repo kalian>
   ```
4. Validasi penambahan Github repo dengan command
   ```
   $ git remote -v
   ```

## Clone Repo di Komputer Lain

Setelah kalian mengintegrasikan lokal repo kalian dengan GitHub repo, teman kalian juga dapat melakukan clone terhadap GitHub repo tersebut menggunakan command

```
$ git clone <url github repo kalian>
```

Teman kalian akan mampu melakukan clone GitHub repo kalian, tetapi belum bisa melakukan penambahan perubaan, untuk itu berikan teman kalian akses menulis pada repo dengan cara mengundang akun GitHub mereka ke dalam GitHub repo kalian. Langkah-langkah nya adalah:

1. Buka repository GitHub proyek kalian, lalu pindah ke Tab `Settings`, kemudian pilih menu `Collaborators`
   ![Github Repo Settings](../assets/github_repo_settings.png)
2. Kemudian pilih `Add People`, masukkan username atau alamat email GitHub teman kalian, lalu invite
   ![Github Invite](../assets/github_invite.png)
3. Minta teman kalian untuk membuka email dan menerima invitation dari kalian
   ![Github Invitation](../assets/github_invitation.png)

## Menambahkan Perubahan pada Branch ke GitHub

Setelah kalian selesai menambahkan perubahan pada branch kalian. Kalian dapat melakukan sinkronisasi perubahan tersebut ke GitHub dengan menggunakan command

```
$ git push -u origin <nama branch>
```

Command diatas akan menambahkan branch beserta seluruh perubahan yang kalian lakukan ke GitHub. Prosesnya mirip seperti kalian mengupload file kalian ke E-Learning atau Google Drive

## Melakukan Merge Request

Setelah kalian mengupload seluruh perubahan kalian menggunakan `git push` pada langkah sebelumnya. Langkah selanjutnya adalah mengembalikan seluruh perubahan tersebut kepada cabang utama kita, yaitu `main`.

Proses ini disebut `Merge` sama seperti sebelumnya, tetapi saat ini kita melakukannya melalui GitHub dengan nama `Merge Request` atau disingkat MR.

Untuk melakukan MR, langkah-langkahnya adalah:

1. Sesaat setelah kalian melakukan push, maka akan tampil tombol hijau diatas repo kalian dengan judul `Compare & pull request`, klik tombol tersebut  
    ![Github Compare and MR](../assets/github_compare_and_mr.png)
   atau bisa juga dengan klik URL yang tampil pada terminal kalian seperti ini  
   ![Github MR from CMD](../assets/github_pr_from_cmd.png)
2. Kemudian kalian akan dibawa ke laman Merge Request, isikan judul MR dan deskripsi singkat sesuai perubahan yang kalian tambahkan. Setelah selesai klik `Create pull request`
   ![Github MR Page](../assets/github_mr_page.png)
3. Berikutnya teman kalian dapat melihat perubahan apa yang kalian coba buat dengan membuka tab `Changes`
   ![Github MR Changes](../assets/github_mr_changes.png)
4. Jika ada revisi yang diperlukan, teman kalian dapat menambahkan komen pada laman MR tersebut, kemudian kalian sebagai pemilik MR dapat menambahkan revisi yang diinginkan pada branch lokal kalian, kemudian mengulangi command `git push`
5. Setelah semua orang dalam proyek sepakat, kalian bisa menambahkan perubahan ini ke cabang utama dengan menekan tombol `Merge pull request`, kemudian pastikan pemilik MR sudah sesuai, lalu tekan `Confirm merge`
   ![Github MR Confirm](../assets/github_mr_confirm.png)

Setelah kalian sukses melakukan Merge, maka akan ada informasi sebagai berikut pada laman MR kalian tadi
![Github Success Merged](../assets/github_success_mr.png)

Kalian akan diberikan opsi untuk menghapus cabang kalian tadi setelah Merge selesai, untuk saat ini biarkan saja cabang tersebut untuk keperluan riwayat cabang.

## Sinkronisasi Perubahan dari MR

Langkah selanjutnya setelah MR berhasil, kalian dan teman kalian dapat kembali ke cabang utama, yaitu `main` kemudian menarik semua perubahan dari MR tadi dengan menggunakan `git pull`

```
$ git checkout main
$ git pull
```

![Git Pull](../assets/git_pull.png)

Maka kalian dan teman kalian akan mandapatkan perubahan terkini
