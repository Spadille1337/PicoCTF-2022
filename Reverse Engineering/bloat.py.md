- After observing given python file, I observed function `arg133` is checking whther the password is coorect or inccorect. So, print that statement manually:
```
print(a[71]+a[64]+a[79]+a[79]+a[88]+a[66]+a[71]+a[64]+a[77]+a[66]+a[68])
```

- Next, run the file, you will get the password then enter that password, you will get the flag:
```
┌──(Spadille㉿kali)-[~/Downloads]
└─$ python3 bloat.flag.py                                                                                                                                                   
happychance
arg444 b'\x02\x08\x13\x1c 5*\x17\r\\^\x10\x07\x05F\x00U[]Y\x011\x14V\x07,\x01Y\\Z[\n\x0b\x11\x1c'
Please enter correct password for flag: happychance
arg432 happychance
arg133(arg432) True
Welcome back... your flag, user:
arg112 None
arg423 picoCTF{d30bfu5c4710n_f7w_b8062eec}
```

Flag:
```
picoCTF{d30bfu5c4710n_f7w_b8062eec}
```