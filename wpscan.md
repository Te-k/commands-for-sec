# WPScan

**Quick install:**
```
gem install wpscan
```

**Update the database:**
```
wpscan --update
```

**Enumerate vulnerable plugins:**
```
wpscan --url http://yourwebsite.com --enumerate vp
```

**Enumerate users:**
```
wpscan --url http://yourwebsite.com --enumerate u
```

**Password bruteforce:**
```
wpscan --url www.example.com --wordlist wordlist_file.txt --threads 30 --username admin
```


