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

1.
