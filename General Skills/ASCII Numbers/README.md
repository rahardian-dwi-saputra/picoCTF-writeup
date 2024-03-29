# ASCII Numbers
- Link: https://play.picoctf.org/practice/challenge/390?category=5&page=3

## Tantangan
Convert the following string of ASCII numbers into a readable string:
`0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x34 0x35 0x63 0x31 0x31 0x5f 0x6e 0x30 0x5f 0x71 0x75 0x33 0x35 0x37 0x31 0x30 0x6e 0x35 0x5f 0x31 0x6c 0x6c 0x5f 0x74 0x33 0x31 0x31 0x5f 0x79 0x33 0x5f 0x6e 0x30 0x5f 0x6c 0x31 0x33 0x35 0x5f 0x34 0x34 0x35 0x64 0x34 0x31 0x38 0x30 0x7d`

## Penyelesaian
- String diatas merupakan kumpulan bilangan heksa yang harus diconvert ke dalam teks (ASCII). Buka tool Cyber Chef https://gchq.github.io/CyberChef/

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/ASCII%20Numbers/assets/ascii%20numbers%201.JPG)

- Klik **From Hex** lalu drag dan drop di kolom **Recipe**

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/ASCII%20Numbers/assets/ascii%20numbers%202.jpg)

- Copy string pada soal diatas lalu paste di kolom **Input**

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/ASCII%20Numbers/assets/ascii%20numbers%203.JPG)

- Flag
```sh
picoCTF{45c11_n0_qu35710n5_1ll_t311_y3_n0_l135_445d4180}
```