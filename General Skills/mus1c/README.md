# mus1c
- Link: https://play.picoctf.org/practice/challenge/15?category=5&page=4

## Tantangan
I wrote you a [song](https://jupiter.challenges.picoctf.org/static/0e21e3ca94779f56b122296424e879f8/lyrics.txt). Put it in the picoCTF{} flag format.

## Penyelesaian
- Unduh lirik lagu pada soal diatas
```sh
wget https://jupiter.challenges.picoctf.org/static/0e21e3ca94779f56b122296424e879f8/lyrics.txt
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/mus1c/assets/music%201.JPG)

- Buka file `lyrics.txt` yang sudah diunduh
```sh
cat lyrics.txt
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/mus1c/assets/music%202.JPG)

- Buka web https://codewithrockstar.com/ lalu klik menu **TRY IT**

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/mus1c/assets/music%203.JPG)

- Copy lirik diatas dan paste di field paling atas lalu tekan tombol **Rock!**

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/mus1c/assets/music%204.JPG)

- Copy angka yang muncul pada field **Output**

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/mus1c/assets/music%205.JPG)

- Buka website https://www.browserling.com/tools/decimal-to-text untuk mengkonversi bilangan desimal ke ASCII. Paste angka desimal diatas pada field

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/mus1c/assets/music%206.JPG)

- Tekan tombol **Convert Dec to Text** untuk melakukan konversi

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/mus1c/assets/music%207.JPG)

- Flag
```sh
picoCTF{rrrocknrn0113r}
```