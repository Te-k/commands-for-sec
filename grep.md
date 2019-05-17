# Grep

**Search for hashtags:**
```
cat file | grep -o '#[[:alnum:]]*'
```

**Search for IPv4 addresses:**
```
$ grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" file.txt
```
