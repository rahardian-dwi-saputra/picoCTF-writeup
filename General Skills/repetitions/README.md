# repetitions
- Link: https://play.picoctf.org/practice/challenge/371?category=5&page=3

## Tantangan
Can you make sense of this file?
Download the file [here](https://artifacts.picoctf.net/c/474/enc_flag).

## Penyelesaian
- Unduh lampiran file diatas
```sh
wget https://artifacts.picoctf.net/c/474/enc_flag
```

- Buka isi file `enc_flag`
```sh
cat enc_flag
```

- Setelah dibuka, file tersebut berisi string yang terencode dengan base64. Setelah didecode, string tersebut masih berupa encode base64. Jadi kita harus mengdecode beberapa kali hingga menemukan flag
- Simpan code dibawah ini dengan nama file `repetitions.py`
```sh
import base64

f = open("enc_flag", "r")
encrypt_flag = f.read()
print("Encrypt Flag : ",encrypt_flag)

while True:
	base64_bytes = encrypt_flag.encode('ascii')
	flag_bytes = base64.b64decode(base64_bytes)
	flag = flag_bytes.decode('ascii')
	if "pico" in flag:
		print("Flag : ",flag)
		break
	else:
		encrypt_flag = flag

```
- Jalankan script diatas dengan `python3`
```sh
python3 repetitions.py
```


- Flag
```sh
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_3f81f7be}
```