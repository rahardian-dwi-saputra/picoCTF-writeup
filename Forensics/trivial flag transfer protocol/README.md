# Trivial Flag Transfer Protocol
- Link: https://play.picoctf.org/practice/challenge/44?category=4&page=1

## Tantangan
Figure out how they moved the [flag](https://mercury.picoctf.net/static/88553d672efbccbc5868002f4c6eb737/tftp.pcapng).

## Penyelesaian
- Download file task
```sh
wget https://mercury.picoctf.net/static/88553d672efbccbc5868002f4c6eb737/tftp.pcapng
```

- Buka file menggunakan aplikasi wireshark

- Pilih File > Export Objects > TFTP...

- Lalu tekan tombol Save All

- Pilih lokasi tempat penyimpanan lalu tekan tombol Open dan selanjutnya tekan tombol Close

- Buka file `instructions.txt` di terminal
```sh
cat instructions.txt
```

- Dekripsi text tersebut dengan ROT13 dengan tool Cyber Chef https://gchq.github.io/CyberChef/

- Tidak ditemukan informasi apapun dari hasil dekripsi diatas. Sekarang kita coba buka file `plan` diterminal
```sh
cat plan
```

- Dekripsi text tersebut dengan ROT13 dengan tool Cyber Chef https://gchq.github.io/CyberChef/ dari hasil dekripsi dapat diketahui bahwa `DUEDILIGENCE` adalah password mengekstrak steganografi dari salah satu gambar

- Setelah dicoba password tersebut bisa digunakan untuk mengekstrak steganografi di file `picture3.bmp`
```sh
steghide extract -sf picture3.bmp -p DUEDILIGENCE
```

- Sekarang buka file `flag.txt` hasil ekstraksi
```sh
cat flag.txt
```


- Flag
```sh
picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}
```