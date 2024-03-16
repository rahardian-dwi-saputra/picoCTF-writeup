# PW Crack 1
- Link: https://play.picoctf.org/practice/challenge/245?category=5&page=2

## Tantangan
Can you crack the password to get the flag?
Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.

## Penyelesaian
- Unduh password checker diatas
```sh
wget https://artifacts.picoctf.net/c/10/level1.py
```

- Unduh flag yang terenkripsi
```sh
wget https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
```

- Gunakan text editor seperti mousepad untuk membuka script `level1.py`. Disini tertulis bahwa bahwa password untuk mendekrip flag adalah `691d`
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


flag_enc = open('level1.flag.txt.enc', 'rb').read()



def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "691d"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()
```
- Jalankan script `level1.py` diatas dengan `python3` lalu masukkan password `691d`
```sh
python3 level1.py
```


- Flag
```sh
picoCTF{545h_r1ng1ng_56891419}
```