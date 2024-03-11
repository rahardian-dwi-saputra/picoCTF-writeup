# Nice netcat...
- Link: https://play.picoctf.org/practice/challenge/156?category=5&page=1

## Tantangan
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 22902`, but it doesn't speak English...

## Penyelesaian
- Jalankan perintah command diatas
```sh
nc mercury.picoctf.net 22902
```

- Setelah dijalankan, muncul bilangan desimal sebagai berikut
```sh
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
100 
51 
100 
102 
100 
54 
100 
102 
125 
10
```

- Konversi bilangan desimal diatas ke ASCII melalui link https://onlinetools.com/ascii/convert-decimal-to-ascii

- Flag
```sh
picoCTF{g00d_k1tty!_n1c3_k1tty!_d3dfd6df}
```