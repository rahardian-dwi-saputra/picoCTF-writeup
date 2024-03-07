# Magikarp Ground Mission
- Link: https://play.picoctf.org/practice/challenge/189?category=5&page=1

## Tantangan
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `abcba9f7`
Additional details will be available after launching your challenge instance.

## Penyelesaian
- Tekan tombol **Launch Instance** untuk memulai tantangan


- Setelah instance berjalan, konek ke SSH server sesuai petunjuk soal. Jika diminta konfirmasi ketik `yes` lalu enter kemudian masukkan password diatas
```sh
ssh ctf-player@venus.picoctf.net -p 55995
```

- Setelah berhasil login, ketik `ls` untuk melihat daftar file yang tersedia. Disini terdapat file `1of3.flag.txt` yang berisi potongan flag pertama. Buka isi file tersebut
```sh
cat 1of3.flag.txt
```

- Selanjutnya baca petunjuk lokasi potongan flag selnjutnya di file `instructions-to-2of3.txt`
```sh
cat instructions-to-2of3.txt
```

- Dari petunjuk diatas diketahui bahwa lokasi potongan flag selanjutnya berada di direktori root atau `/`. Sekarang kita pindah ke direktori root
```sh
cd /
ls
```

- Di direktori root terdapat file `2of3.flag.txt` yang berisi potongan flag kedua. Sekarang buka isi file tersebut
```sh
cat 2of3.flag.txt
```

- Petunjuk lokasi potongan flag terakhir berada di file `instructions-to-3of3.txt`
```sh
cat instructions-to-3of3.txt
```

- Dari petunjuk diatas diketahui bahwa lokasi potongan flag terakhir berada di direktori `/home`. Sekarang kita pindah ke direktori `/home`
```sh
cd ~
ls
```

- Potongan flag terakhir berada di file `3of3.flag.txt` Sekarang buka isi file tersebut
```sh
cat 3of3.flag.txt
```

- Sekarang kita susun potongan flag tersebut menjadi satu bagian yang utuh seperti ini

- Flag
```sh
picoCTF{xxsh_0ut_0f_\/\/4t3r_21cac893}
```