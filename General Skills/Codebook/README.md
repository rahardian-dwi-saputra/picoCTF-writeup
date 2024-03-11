# Codebook
- Link: https://play.picoctf.org/practice/challenge/238?category=5&page=2

## Tantangan
Run the Python script code.py in the same directory as codebook.txt.
- [Download code.py](https://artifacts.picoctf.net/c/3/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/3/codebook.txt)

## Penyelesaian
- Unduh file `code.py` yang terlampir dalam soal
```sh
wget https://artifacts.picoctf.net/c/3/code.py
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/Codebook/assets/codebook%201.JPG)

- Unduh file `codebook.txt` yang terlampir dalam soal
```sh
wget https://artifacts.picoctf.net/c/3/codebook.txt
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/Codebook/assets/codebook%202.JPG)

- Pastikan file `code.py` dan file `codebook.txt` yang berhasil diunduh terletak di lokasi direktori yang sama
- Jalankan program `code.py` dengan `python3` untuk mendekrip isi file `codebook.txt` 
```sh
python3 code.py
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/Codebook/assets/codebook%203.JPG)

- Flag
```sh
picoCTF{c0d3b00k_455157_197a982c}
```