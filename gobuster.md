# Gobuster

**Enumerate directories**:
```
gobuster dir -u https://buffered.io -w ~/wordlists/shortlist.txt
```

**DNS mode:**
```
gobuster dns -d mysite.com -t 50 -w common-names.txt
```

**Show IPs in DNS mode:**
```
gobuster dns -d google.com -w ~/wordlists/subdomains.txt -i
```

**vhost mode:**
```
gobuster vhost -u https://mysite.com -w common-vhosts.txt
```
