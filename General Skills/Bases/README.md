# Bases
- Link: https://play.picoctf.org/practice/challenge/67?category=5&page=2

## Tantangan
What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.

## Penyelesaian
- String diatas adalah string yang diencode dengan base64. Jadi kita tinggal decode string tersebut menggunakan base64
```sh
echo 'bDNhcm5fdGgzX3IwcDM1' | base64 -d
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/Bases/assets/bases%201.JPG)

- Sekarang kita tinggal memasukkan hasil encode tersebut kedalam flag
- Flag
```sh
picoCTF{l3arn_th3_r0p35}
```