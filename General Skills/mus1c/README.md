# mus1c
- Link: https://play.picoctf.org/practice/challenge/15?category=5&page=4

## Tantangan
I wrote you a [song](https://jupiter.challenges.picoctf.org/static/0e21e3ca94779f56b122296424e879f8/lyrics.txt). Put it in the picoCTF{} flag format.

## Penyelesaian
- Unduh lirik lagu pada soal diatas
```sh
wget https://jupiter.challenges.picoctf.org/static/0e21e3ca94779f56b122296424e879f8/lyrics.txt
```

- Buka file `lyrics.txt` yang sudah diunduh
```sh
cat lyrics.txt
```

- Buka web https://codewithrockstar.com/ lalu klik menu **TRY IT**

- Copy lirik diatas dan paste di field paling atas lalu tekan tombol **Rock!**


- Copy angka yang muncul pada field **Output**


- Buka website https://www.browserling.com/tools/decimal-to-text untuk mengkonversi bilangan desimal ke ASCII. Paste angka desimal diatas pada field

- Tekan tombol **Convert Dec to Text** untuk melakukan konversi

- Flag
```sh
picoCTF{rrrocknrn0113r}
```