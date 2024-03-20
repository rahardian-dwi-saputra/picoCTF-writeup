# chrono
- Link: https://play.picoctf.org/practice/challenge/347?category=5&page=3

## Tantangan
How to automate tasks to run at intervals on linux servers?
Additional details will be available after launching your challenge instance.

## Penyelesaian
- Tekan tombol **Launch Instance** untuk memulai tantangan

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/chrono/assets/chrono%201.JPG)

- Setelah instance berjalan, konek ke SSH server sesuai petunjuk soal. Jika diminta konfirmasi ketik yes lalu enter kemudian masukkan password yang tertera setelah Launch Instance
```sh
ssh picoplayer@saturn.picoctf.net -p 60223
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/chrono/assets/chrono%202.JPG)

- Automate tasks pada linux berada di `\etc\crontab` jadi kita tinggal membuka isi file tersebut
```sh
cat /etc/crontab
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/chrono/assets/chrono%203.JPG)

- Flag
```sh
picoCTF{Sch3DUL7NG_T45K3_L1NUX_7754e199}
```