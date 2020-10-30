# Nmap

**Retrieve a TLS certificate:**
```
nmap -p 443 –script ssl-cert didierstevens.com
```


**Quickstart:**

```sh
nmap -sC -sV --top-ports 20 <IP> -o <FILE>
nmap -sC -sV --open --reason <IP> -o <FILE>
```

**Full ports scan:**

```sh
nmap -sV -sC -p- -O --open <IP> -o <FILE>
```

**Ping sweep:**

```sh
nmap -sn -PE <IP or Range>
```

**UDP scan:**

```sh
nmap -sU <IP or Range>
```

**Scan for open ports, determine open services:**

```sh
nmap --open -sV <IP or Range>
```

**Scan and run default scripts:**

```sh
nmap -sC <IP or Range>
```

**Run a specific script:**

```sh
# location on Kali: /usr/share/nmap/scripts/
nmap --script <SCRIPT_NAME> <IP>
```

**Skip ping:**

```sh
nmap -Pn <IP>
```

**Output result to file:**

```sh
nmap <IP> -o <FILE> # text file
nmap <IP> -oG <FiLE> # greppable file
nmap <IP> -oN <FILE> # nmap file
nmap <IP> -oA <FILE> # all formats
```
