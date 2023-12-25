# Wireshark doo dooo do doo...
- Link: https://play.picoctf.org/practice/challenge/115?category=4&page=1

## Tantangan
Can you find the flag? [shark1.pcapng.](https://mercury.picoctf.net/static/d6f9aa16d2a2c51d2e431e658d87af9e/shark1.pcapng)

## Penyelesaian
- Download file task
```sh
wget https://mercury.picoctf.net/static/d6f9aa16d2a2c51d2e431e658d87af9e/shark1.pcapng
```

- Buka file tersebut pakai aplikasi wireshark


- Di packet nomor 827 terdapat pesan `OK`

- Klik kanan packet tersebut terus pilih Follow > HTTP Stream


- Disini terdapat string yang terenkripsi dengan ROT13

- Gunakan tool `Cyber Chef` untuk melakukan dekripsi https://gchq.github.io/CyberChef/

- Pada field pencarian ketik `rot13` lalu tarik `ROT13` ke field Recipe

- Copy string sebelumnya dan paste di field Input

- Flag
```sh
picoCTF{p33kab00_1_s33_u_deadbeef}
```