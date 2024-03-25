# plumbing
- Link: https://play.picoctf.org/practice/challenge/48?category=5&page=4

## Tantangan
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 4427`.

## Penyelesaian
- Lakukan koneksi dengan netcat
```sh
nc jupiter.challenges.picoctf.org 4427
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/plumbing/assets/plumbing%201.JPG)

- Disini banyak string yang muncul, untuk mencari flag kita perlu menambahkan perintah untuk memfilter output tersebut dan menemukan flag sehingga kita ubah perintahnya menjadi sebagai berikut
```sh
nc jupiter.challenges.picoctf.org 4427 | grep pico
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/plumbing/assets/plumbing%202.JPG)

- Flag
```sh
picoCTF{digital_plumb3r_5ea1fbd7}
```