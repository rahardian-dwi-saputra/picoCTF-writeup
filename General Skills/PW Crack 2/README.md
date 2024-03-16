# PW Crack 2
- Link: https://play.picoctf.org/practice/challenge/246?category=5&page=2

## Tantangan
Can you crack the password to get the flag?
Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.

## Penyelesaian
- Unduh password checker diatas
```sh
wget https://artifacts.picoctf.net/c/15/level2.py
```

- Unduh flag yang terenkripsi
```sh
wget https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
```

- Gunakan text editor seperti mousepad untuk membuka script `level1.py`. Disini kita perlu menambahkan 2 baris program untuk mengetahui password yang digunakan. Ubah script `level2.py` menjadi sebagai berikut
```sh
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level2.flag.txt.enc', 'rb').read()



def level_2_pw_check():
    password = chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65)
    print("Valid password : ",password)
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_2_pw_check()
```
- Jalankan script `level2.py` diatas dengan `python3` lalu masukkan password yang ditampilkan
```sh
python3 level2.py
```


- Flag
```sh
picoCTF{tr45h_51ng1ng_502ec42e}
```