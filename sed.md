# Sed

**Remove brackets in a domain name (for IOCs)**
```bash
sed -E 's/\.([a-z]*)$/[.]\1/g'
```
