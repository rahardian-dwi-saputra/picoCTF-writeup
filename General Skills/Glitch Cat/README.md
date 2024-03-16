# Glitch Cat
- Link: https://play.picoctf.org/practice/challenge/242?category=5&page=2

## Tantangan
Our flag printing service has started glitching!
`$ nc saturn.picoctf.net 52682`

## Penyelesaian
- Jalankan perintah diatas
```sh
nc saturn.picoctf.net 52682
```

- Copy output perintah diatas lalu masukkan sebagai nilai variabel di program python lalu cetak nilai variabel tersebut. Simpan script dibawah ini dengan nama `glitchcat.py`
```sh
flag = 'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
print(flag)
```
- Jalankan script diatas dengan `python3`
```sh
python3 glitchcat.py
```

- Flag
```sh
picoCTF{gl17ch_m3_n07_bda68f75}
```