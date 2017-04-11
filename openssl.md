# Openssl

**Parse and print certificate infos:**
```
openssl x509 -in cert.crt  -text
```

**Verify a certificate:**
```
openssl verify -CAfile <(cat Intermediate.pem RootCert.pem) UserCert.pem
```
