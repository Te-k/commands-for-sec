# Openssl

**Parse and print PEM certificate infos:**
```
openssl x509 -in cert.crt  -text
```

**Same with DER** (read .crl too):
```
openssl x509 -in cert.crt -inform der -text
```

**Verify a certificate:**
```
openssl verify -CAfile <(cat Intermediate.pem RootCert.pem) UserCert.pem
```

**Download and show info on an online certificate**
```
openssl s_client -showcerts -connect DOMAIN:443 </dev/null 2>/dev/null | openssl x509 -text
```

**Get fingerprint of a certificate**
```
openssl x509 -noout -fingerprint -md5 -inform pem -in [certificate-file.crt]
```

**Remotely check a certificate:**
```
openssl s_client -showcerts -connect www.domain.com:443
```

**Print a PKCS7 certificate:**
```
openssl pkcs7 -inform DER -print_certs -text -in FILE
```
