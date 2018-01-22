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

**Change user agent**:
```
curl -A "Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 6.3; WOW64; Trident/7.0; .NET4.0E; .NET4.0C; .NET CLR 3.5.30729; .NET CLR 2.0.50727; .NET CLR 3.0.30729; Tablet PC 2.0; ms-office)" http://url.com
```
