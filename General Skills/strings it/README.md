# strings it
- Link: https://play.picoctf.org/practice/challenge/37?category=5&page=1

## Tantangan
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?

## Penyelesaian
- Download file yang terlampir di soal
```sh
wget https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
```

- Setelah file `strings` berhasil diunduh, sekarang kita cari string yang mengandung kata `pico` yang terdapat di dalam file tersebut untuk mendapatkan flag
```sh
strings strings | grep pico
```

- Flag
```sh
picoCTF{5tRIng5_1T_7f766a23}
```