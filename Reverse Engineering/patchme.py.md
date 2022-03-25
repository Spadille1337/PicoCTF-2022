patchme.flag.py
```python
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


flag_enc = open('flag.txt.enc', 'rb').read()



def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "ak98" + \
                   "-=90" + \
                   "adfjhgj321" + \
                   "sleuth9000"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), "utilitarian")
        print(decryption)
        return
    print("That password is incorrect")

level_1_pw_check()
```

flag.txt.enc 
```bash
┌──(Spadille㉿kali)-[~/Downloads]
└─$ cat flag.txt.enc                                                                                                                                                        

CR1@    UYX+
6U]WVM

```

```bash
┌──(Spadille㉿kali)-[~/Downloads]
└─$ python3                                                                                                                                                                 
Python 3.9.10 (main, Feb 22 2022, 13:54:07) 
[GCC 11.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print("ak98" + \
...                    "-=90" + \
...                    "adfjhgj321" + \
...                    "sleuth9000")
ak98-=90adfjhgj321sleuth9000
```

```bash
┌──(Spadille㉿kali)-[~/Downloads]
└─$ python3 patchme.flag.py                                                                                                                                   
Please enter correct password for flag: ak98-=90adfjhgj321sleuth9000
Welcome back... your flag, user:
picoCTF{p47ch1ng_l1f3_h4ck_c4a4688b}
```

Flag
```
picoCTF{p47ch1ng_l1f3_h4ck_c4a4688b}
```