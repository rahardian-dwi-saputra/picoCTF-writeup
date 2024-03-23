# money-ware
- Link: https://play.picoctf.org/practice/challenge/357?category=5&page=3

## Tantangan
Flag format: picoCTF{Malwarename}
The first letter of the malware name should be capitalized and the rest lowercase.
Your friend just got hacked and has been asked to pay some bitcoins to `1Mz7153HMuxXTuR2R1t78mGSdzaAtNbBWX`. He doesn’t seem to understand what is going on and asks you for advice. Can you identify what malware he’s being a victim of?

## Penyelesaian
- Kita bisa menelusuri alamat bitcoin diatas menggunakan google

- Setelah membuka link ( https://www.cnbc.com/2017/06/28/ransomware-cyberattack-petya-bitcoin-payment.html ) dari hasil pencarian diatas, disini disebutkan bahwa nama malwarenya adalah `petya`


- Flag
```sh
picoCTF{petya}
```