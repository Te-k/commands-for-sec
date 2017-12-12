# Curl

**Find url of an url shortened link**:
```bash
curl -w "%{redirect_url}" URL
```
**HEAD HTTP request**:
```bash
curl -I -X HEAD URL
```

**Follow redirects**:
```bash
curl -L URL
```

**Do not validate HTTPs certificate:**
```bash
curl -k URL
```
