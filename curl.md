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

**POST requests**
```
curl -d "param1=value1&param2=value2" -X POST http://localhost:3000/data
```

**POST Json request**:
```
curl -d '{"key1":"value1", "key2":"value2"}' -H "Content-Type: application/json" -X POST http://localhost:3000/data
```

**Force DNS resolution**
```
curl https://DOMAIN.TLD --resolve "DOMAIN.TLD:443:IP_ADDRESS"
```

**Test if a proxy is open:**
```
http_proxy=http://X.X.X.X:8080/ curl -4 -s http://nyc2.mirrors.digitalocean.com/tools/open_proxy_check.txt
```
