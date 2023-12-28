# Enhance!
- Link: https://play.picoctf.org/practice/challenge/265?category=4&page=1

## Tantangan
Download this image file and find the flag. [Download image file](https://artifacts.picoctf.net/c/100/drawing.flag.svg)

## Penyelesaian
- Download file task
```sh
wget https://artifacts.picoctf.net/c/100/drawing.flag.svg
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/enhance/assets/enhance%201.JPG)

- Gunakan tool `strings` untuk menampilkan string yang terdapat dalam gambar
```sh
strings drawing.flag.svg
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/enhance/assets/enhance%202.JPG)

- Dari hasil perintah diatas ditemukan beberapa potongan flag seperti berikut ini

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/enhance/assets/enhance%203.JPG)

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/enhance/assets/enhance%204.JPG)

- Jika potongan karakter disatukan maka ditemukan flag sebagai berikut

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/enhance/assets/enhance%205.JPG)

- Flag
```sh
picoCTF{3nh4nc3d_aab729dd}
```