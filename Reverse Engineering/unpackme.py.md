- Print the `plain` variable.
```bash
┌──(Spadille㉿kali)-[~/Downloads]
└─$ python3 unpackme.flag.py                                                                                                                                                
plain b"\npw = input('What\\'s the password? ')\n\nif pw == 'batteryhorse':\n  print('picoCTF{175_chr157m45_5274ff21}')\nelse:\n  print('That password is incorrect.')\n\n"
What's the password? 
```

Flag:
```
picoCTF{175_chr157m45_5274ff21}
```