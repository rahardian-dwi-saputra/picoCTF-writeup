# HashingJobApp
- Link: https://play.picoctf.org/practice/challenge/243?category=5&page=2

## Tantangan
If you want to hash with the best, beat this test!
`nc saturn.picoctf.net 53638`

## Penyelesaian
- Jalankan perintah netcat diatas
```sh
nc saturn.picoctf.net 53638
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/HashingJobApp/assets/hashing%20job%201.JPG)

- Ubah setiap kata yang muncul kedalam hash md5 untuk menjawab setiap soal. Anda bisa menggunakan tool online https://www.md5hashgenerator.com/

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/HashingJobApp/assets/hashing%20job%202.JPG)

- Flag
```sh
picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}
```