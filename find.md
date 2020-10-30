# Find

**Delete files:**

```sh
find . -iname "*.nope" -delete
find . -type f -name "tecmint.txt" -exec rm -f {} \;
find . -type f -name "*.txt" -exec rm -f {} \;
find . -type f -name "*.mp3" -exec rm -f {} \;
```

**Find files created on a specific day:**
`find . -type f -newermt 2007-06-07 ! -newermt 2007-06-08`


**Find files modified in the past 5 days:**

```sh
find / -mtime -5 -ctime -5
```

**Find files modified in the last minute:**

```sh
find / -mmin -1
```

**Find SUID/SGID files:**

```sh
find / -type f -a \( -perm -u+s -o -perm -g+s \) -exec ls -l {} \; 2> /dev/null
find / -perm /u=s
find / -perm /g=s
find / -perm 2644
find / -perm 1551
find . -type f -perm 0777 -print
find / -type f ! -perm 777
```


**Find read only files:**

```sh
find / -perm /u=r
find / -perm /a=x
```


**Find all 777 permission files and use chmod command to set permissions to
644:**

```sh
find / -type f -perm 0777 -print -exec chmod 644 {} \;
```


**Send output from the find command to a file:**

```sh
find / -name *.mp3 -fprint nameoffiletoprintto
```

**Find and execute a command against a file:**

```sh
# Search and edit a file at the same time
find / -name filename -exec nano '{}' \;
```


**Find single files based on user:**

```sh
find / -user root -name file.txt
```

**Find all files based on group:**

```sh
find /home -group developer
```

**Find Particular Files of User:**

```sh
find /home -user tecmint -iname "*.txt"
```


**Find Size between 50MB – 100MB:**

```sh
find / -size +50M -size -100M
```


**Find all emtpy files:**

```sh
find /tmp -type f -empty
```

**Find all empty directories:**

```sh
find /tmp -type d -empty
```

**Find all hidden files:**

```sh
find /tmp -type f -name ".*"
```
