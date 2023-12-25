# Information
- Link: https://play.picoctf.org/practice/challenge/186?category=4&page=1

## Tantangan
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/7cf6a33f90deeeac5c73407a1bdc99b6/cat.jpg)

## Penyelesaian
- Download file `cat.jpg`
```sh
wget https://mercury.picoctf.net/static/7cf6a33f90deeeac5c73407a1bdc99b6/cat.jpg
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/information/assets/inf%201.JPG)

- Gunakan tool `exiftool` untuk menampilkan metadata gambar. Pada informasi license terdapat string yang terencode dengan base64
```sh
exiftool cat.jpg
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/information/assets/inf%202.JPG)

- Kita bisa menyeleksi string tersebut dengan perintah berikut
```sh
exiftool cat.jpg | grep License | sed -e 's/.*: //'
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/information/assets/inf%203.JPG)

- Sekarang kita decode string tersebut dengan base64
```sh
exiftool cat.jpg | grep License | sed -e 's/.*: //' | base64 -d
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/information/assets/inf%204.JPG)

- Selain cara diatas, kita juga bisa copas string tersebut kemudian decode menggunakan base64
```sh
echo 'cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9' | base64 -d
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/information/assets/inf%205.JPG)

- Flag
```sh
picoCTF{the_m3tadata_1s_modified}
```