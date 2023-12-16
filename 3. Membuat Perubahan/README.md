# Membuat Perubahan

Ini merupakan inti materi kita hari ini, karena alasan mengapa kita membutuhkan Git adalah memudahkan kolaborasi dalam melakukan perubahan kode.

## Gambaran Besar

Berikut adalah gambaran besar bagaimana cara kerja Git dalam mengatur riwayat perubahan kode
![Git Changes Flow](../assets/git_changes_flow.png)

## Menambahkan Perubahan

Seperti pada diagram diatas, untuk menambahkan perubahan kode yang diinginkan kedalam Git Staging, kita dapat menggunakan command

```
$ git add <nama_file>
```

Atau untuk menambahkan seluruh perubahan yang dilakukan, gunakan command

```
$ git add .
```

Jika kalian ragu akan perubahan apa saja yang telah kalian lakukan, kalian bisa menggunakan command berikut:

```
$ git status
```

Maka akan ditampilkan perubahan perubahan yang telah kalian lakukan saat ini

## Menyimpan Perubahan secara Permanen

Setelah kalian selesai dengan perubahan yang kalian lakukan, kalian dapat menambahkan perubahan tersebut secara permanen menggunakan command berikut

```
$ git commit -m "[pesan deskriptif]"
```

`pesan deskriptif` umumnya berisi deskripsi singkat tentang perubahan yang telah kalian lakukan sebagai penanda dalam riwayat perubahan nantinya

## Melihat Riwayat Perubahan

Untuk melakukan riwayat perubahan sejauh ini pada kode kalian, dapat menggunakan command berikut

```
$ git log
```
