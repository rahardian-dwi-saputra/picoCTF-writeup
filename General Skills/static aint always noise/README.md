# Static ain't always noise
- Link: https://play.picoctf.org/practice/challenge/163?category=5&page=1

## Tantangan
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/static)? This [BASH script](https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/ltdis.sh) might help!

## Penyelesaian
- Download bash script di lampiran soal
```sh
wget https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/ltdis.sh
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/static%20aint%20always%20noise/assets/static%201.JPG)

- Berikan permission execute pada file `ltdis.sh`
```sh
chmod +x ltdis.sh
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/static%20aint%20always%20noise/assets/static%202.JPG)

- Download file binary di lampiran soal
```sh
wget https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/static
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/static%20aint%20always%20noise/assets/static%203.JPG)

- Eksekusi file `ltdis.sh` dan masukkan file `static` sebagai input
```sh
./ltdis.sh static
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/static%20aint%20always%20noise/assets/static%204.JPG)

- Setelah dieksekusi, sekarang kita buka file `static.ltdis.strings.txt` yang berisi kumpulan string
```sh
cat static.ltdis.strings.txt
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/static%20aint%20always%20noise/assets/static%205.JPG)

- Flag
```sh
picoCTF{d15a5m_t34s3r_ccb2b43e}
```