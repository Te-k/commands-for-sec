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
