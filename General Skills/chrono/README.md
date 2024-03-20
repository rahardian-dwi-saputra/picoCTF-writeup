# chrono
- Link: https://play.picoctf.org/practice/challenge/347?category=5&page=3

## Tantangan
How to automate tasks to run at intervals on linux servers?
Additional details will be available after launching your challenge instance.

## Penyelesaian
- Tekan tombol **Launch Instance** untuk memulai tantangan

- Setelah instance berjalan, konek ke SSH server sesuai petunjuk soal. Jika diminta konfirmasi ketik yes lalu enter kemudian masukkan password yang tertera setelah Launch Instance
```sh
ssh picoplayer@saturn.picoctf.net -p 60223
```


- Automate tasks pada linux berada di `\etc\crontab` jadi kita tinggal membuka isi file tersebut
```sh
cat /etc/crontab
```


- Flag
```sh
picoCTF{Sch3DUL7NG_T45K3_L1NUX_7754e199}
```