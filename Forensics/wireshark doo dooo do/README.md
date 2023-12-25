# Wireshark doo dooo do doo...
- Link: https://play.picoctf.org/practice/challenge/115?category=4&page=1

## Tantangan
Can you find the flag? [shark1.pcapng.](https://mercury.picoctf.net/static/d6f9aa16d2a2c51d2e431e658d87af9e/shark1.pcapng)

## Penyelesaian
- Download file task
```sh
wget https://mercury.picoctf.net/static/d6f9aa16d2a2c51d2e431e658d87af9e/shark1.pcapng
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/wireshark%20doo%20dooo%20do/assets/wireshark%20do%201.JPG)

- Buka file tersebut pakai aplikasi wireshark

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/wireshark%20doo%20dooo%20do/assets/wireshark%20do%202.JPG)

- Di packet nomor 827 terdapat pesan `OK`

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/wireshark%20doo%20dooo%20do/assets/wireshark%20do%203.JPG)

- Klik kanan packet tersebut terus pilih Follow > HTTP Stream

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/wireshark%20doo%20dooo%20do/assets/wireshark%20do%204.JPG)

- Disini terdapat string yang terenkripsi dengan ROT13

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/wireshark%20doo%20dooo%20do/assets/wireshark%20do%205.JPG)

- Gunakan tool `Cyber Chef` untuk melakukan dekripsi https://gchq.github.io/CyberChef/
- Pada field pencarian ketik `rot13` lalu tarik `ROT13` ke field Recipe

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/wireshark%20doo%20dooo%20do/assets/wireshark%20do%206.jpg)

- Copy string sebelumnya dan paste di field Input

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/Forensics/wireshark%20doo%20dooo%20do/assets/wireshark%20do%207.JPG)

- Flag
```sh
picoCTF{p33kab00_1_s33_u_deadbeef}
```