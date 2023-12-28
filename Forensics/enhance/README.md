# Enhance!
- Link: https://play.picoctf.org/practice/challenge/265?category=4&page=1

## Tantangan
Download this image file and find the flag. [Download image file](https://artifacts.picoctf.net/c/100/drawing.flag.svg)

## Penyelesaian
- Download file task
```sh
wget https://artifacts.picoctf.net/c/100/drawing.flag.svg
```

- Gunakan tool `strings` untuk menampilkan string yang terdapat dalam gambar
```sh
strings drawing.flag.svg
```

- Dari hasil perintah diatas ditemukan beberapa potongan flag seperti berikut ini


- Jika potongan karakter disatukan maka ditemukan flag sebagai berikut

- Flag
```sh
picoCTF{3nh4nc3d_aab729dd}
```