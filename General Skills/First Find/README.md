# First Find
- Link: https://play.picoctf.org/practice/challenge/320?category=5&page=3

## Tantangan
Unzip this archive and find the file named 'uber-secret.txt'
- [Download zip file](https://artifacts.picoctf.net/c/502/files.zip)

## Penyelesaian
- Unduh file zip yang terlampir
```sh
wget https://artifacts.picoctf.net/c/502/files.zip
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/First%20Find/assets/first%20find%201.JPG)

- Ekstrak file zip yang sudah diunduh
```sh
unzip files.zip
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/First%20Find/assets/first%20find%202.JPG)

- Dari hasil ekstraksi diatas, kita sudah mengetahui lokasi file `uber-secret.txt`. Kita tinggal membaca isi file tersebut dengan path yang sudah ditemukan
```sh
cat files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/First%20Find/assets/first%20find%203.JPG)

- Kita juga bisa menggunakan `strings` lalu memfilter string pico untuk mendapatkan flag
```sh
strings files.zip | grep pico
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/First%20Find/assets/first%20find%204.JPG)

- Atau mencari lewat semua path folder hasil ekstraksi
```sh
grep -r pico files
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/First%20Find/assets/first%20find%205.JPG)

- Flag
```sh
picoCTF{f1nd_15_f457_ab443fd1}
```