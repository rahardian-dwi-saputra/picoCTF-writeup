# Matryoshka doll
- Link: https://play.picoctf.org/practice/challenge/129?category=4&page=1

## Tantangan
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/5eb456e480e485183c9c1b16952c6eda/dolls.jpg)

## Penyelesaian
- Download file gambar
```sh
wget https://mercury.picoctf.net/static/5eb456e480e485183c9c1b16952c6eda/dolls.jpg
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/matryoshka%20doll/assets/matryoshka%201.JPG)

- Gunakan tool `binwalk` untuk mengekstrak file tersembunyi
```sh
binwalk -e dolls.jpg
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/matryoshka%20doll/assets/matryoshka%202.JPG)

- Navigasi ke folder hasil ekstraksi hingga menemukan gambar `2_c.jpg` kemudian ekstrak file tersembunyi dibalik gambar `2_c.jpg`
```sh
cd _dolls.jpg.extracted
cd base_images
binwalk -e 2_c.jpg
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/matryoshka%20doll/assets/matryoshka%203.JPG)

- Navigasi ke folder hasil ekstraksi hingga menemukan gambar `3_c.jpg` kemudian ekstrak file tersembunyi dibalik gambar `3_c.jpg`
```sh
cd _2_c.jpg.extracted
cd base_images
binwalk -e 3_c.jpg
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/matryoshka%20doll/assets/matryoshka%204.JPG)

- Navigasi ke folder hasil ekstraksi hingga menemukan gambar `4_c.jpg` kemudian ekstrak file tersembunyi dibalik gambar `4_c.jpg`
```sh
cd _3_c.jpg.extracted/base_images
binwalk -e 4_c.jpg
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/matryoshka%20doll/assets/matryoshka%205.JPG)

- Setelah ekstraksi file `4_c.jpg` terdapat file `flag.txt` yang berisi flag
```sh
cd _4_c.jpg.extracted
cat flag.txt
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/matryoshka%20doll/assets/matryoshka%206.JPG)

- Flag
```sh
picoCTF{336cf6d51c9d9774fd37196c1d7320ff}
```