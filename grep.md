# Grep

**Search for hashtags:**
```
cat file | grep -o '#[[:alnum:]]*'
```

**Search for IPv4 addresses:**
```
$ grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" file.txt
```

**Search for an email address:**
```
grep -E -o "\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,6}\b" file.txt
```
