# awk

**Select lines in a csv file based on text comparison**
```bash
awk -F ',' '$5 ~ /baddomain.com/' FILE
```

**Print specific fields of a csv file**
```bash
awf -F '|' '{print $3 $4} FILE
```
