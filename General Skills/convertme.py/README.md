# convertme.py
- Link: https://play.picoctf.org/practice/challenge/239?category=5&page=2

## Tantangan
Run the Python script and convert the given number from decimal to binary to get the flag.
[Download Python script](https://artifacts.picoctf.net/c/22/convertme.py)

## Penyelesaian
- Unduh lampiran file diatas
```sh
wget https://artifacts.picoctf.net/c/22/convertme.py
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/convertme.py/assets/convertme%201.JPG)

- Jalankan program `convertme.py`
```sh
python3 convertme.py
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/convertme.py/assets/convertme%202.JPG)

- Terdapat soal untuk mengubah bilangan desimal ke biner. Gunakan tool https://www.rapidtables.com/convert/number/decimal-to-binary.html untuk melakukan konversi
- Tekan tombol **Convert** untuk melakukan konversi

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/convertme.py/assets/convertme%203.JPG)

- Setelah berhasil dikonversi, copy bilangan tersebut dan paste untuk menjawab soal

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/convertme.py/assets/convertme%204.JPG)

- Flag
```sh
picoCTF{4ll_y0ur_b4535_762f748e}
```