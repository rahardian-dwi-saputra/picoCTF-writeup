# Trivial Flag Transfer Protocol
- Link: https://play.picoctf.org/practice/challenge/44?category=4&page=1

## Tantangan
Figure out how they moved the [flag](https://mercury.picoctf.net/static/88553d672efbccbc5868002f4c6eb737/tftp.pcapng).

## Penyelesaian
- Download file task
```sh
wget https://mercury.picoctf.net/static/88553d672efbccbc5868002f4c6eb737/tftp.pcapng
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/trivial%20flag%20transfer%20protocol/assets/trivial%20flag%201.JPG)

- Buka file menggunakan aplikasi wireshark

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/trivial%20flag%20transfer%20protocol/assets/trivial%20flag%202.JPG)

- Pilih File > Export Objects > TFTP...

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/trivial%20flag%20transfer%20protocol/assets/trivial%20flag%203.JPG)

- Lalu tekan tombol Save All

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/trivial%20flag%20transfer%20protocol/assets/trivial%20flag%204.JPG)

- Pilih lokasi tempat penyimpanan lalu tekan tombol Open dan selanjutnya tekan tombol Close

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/trivial%20flag%20transfer%20protocol/assets/trivial%20flag%205.JPG)

- Buka file `instructions.txt` di terminal
```sh
cat instructions.txt
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/trivial%20flag%20transfer%20protocol/assets/trivial%20flag%206.JPG)

- Dekripsi text tersebut dengan ROT13 dengan tool Cyber Chef https://gchq.github.io/CyberChef/

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/wireshark%20doo%20dooo%20do/assets/wireshark%20do%206.jpg)

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/trivial%20flag%20transfer%20protocol/assets/trivial%20flag%207.JPG)

- Tidak ditemukan informasi apapun dari hasil dekripsi diatas. Sekarang kita coba buka file `plan` diterminal
```sh
cat plan
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/trivial%20flag%20transfer%20protocol/assets/trivial%20flag%208.JPG)

- Dekripsi text tersebut dengan ROT13 dengan tool Cyber Chef https://gchq.github.io/CyberChef/ dari hasil dekripsi dapat diketahui bahwa `DUEDILIGENCE` adalah password mengekstrak steganografi dari salah satu gambar

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/trivial%20flag%20transfer%20protocol/assets/trivial%20flag%209.JPG)

- Setelah dicoba password tersebut bisa digunakan untuk mengekstrak steganografi di file `picture3.bmp`
```sh
steghide extract -sf picture3.bmp -p DUEDILIGENCE
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/trivial%20flag%20transfer%20protocol/assets/trivial%20flag%2010.JPG)

- Sekarang buka file `flag.txt` hasil ekstraksi
```sh
cat flag.txt
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/trivial%20flag%20transfer%20protocol/assets/trivial%20flag%2011.JPG)

- Flag
```sh
picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}
```