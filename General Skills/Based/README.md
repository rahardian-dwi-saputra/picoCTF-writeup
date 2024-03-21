# Based
- Link: https://play.picoctf.org/practice/challenge/35?category=5&page=3

## Tantangan
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29956`.

## Penyelesaian
- Jalankan perintah netcat diatas
```sh
nc jupiter.challenges.picoctf.org 29956
```

- Setelah dijalankan akan muncul beberapa soal untuk mengkonversi bilangan ke string (word). Soal pertama adalah konversi bilangan biner ke string, soal kedua adalah konversi bilangan oktal ke string dan soal terakhir adalah konversi bilangan heksa ke string. Anda bisa menggunakan tool Cyber Chef https://gchq.github.io/CyberChef/ untuk menyelesaikan soal diatas
- Flag
```sh
picoCTF{learning_about_converting_values_b375bb16}
```