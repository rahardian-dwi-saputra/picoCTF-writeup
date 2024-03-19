# First Find
- Link: https://play.picoctf.org/practice/challenge/37?category=5&page=1

## Tantangan
Unzip this archive and find the file named 'uber-secret.txt'
- [Download zip file](https://artifacts.picoctf.net/c/502/files.zip)

## Penyelesaian
- Unduh file zip yang terlampir
```sh
wget https://artifacts.picoctf.net/c/502/files.zip
```

- Ekstrak file zip yang sudah diunduh
```sh
unzip files.zip
```

- Dari hasil ekstraksi diatas, kita sudah mengetahui lokasi file `uber-secret.txt`. Kita tinggal membaca isi file tersebut dengan path yang sudah ditemukan
```sh
cat files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
```


- Kita juga bisa menggunakan `strings` lalu memfilter string pico untuk mendapatkan flag
```sh
strings files.zip | grep pico
```

- Atau mencari lewat semua path folder hasil ekstraksi
```sh
grep -r pico files
```

- Flag
```sh
picoCTF{f1nd_15_f457_ab443fd1}
```