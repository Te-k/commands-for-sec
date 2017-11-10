# Openssl

<<<<<<< HEAD
**Parse and print certificate infos:**
=======
**Parse and print PEM certificate infos:**
>>>>>>> fb2b4e1dc2dce326e4640cb965be1e624dd23482
```
openssl x509 -in cert.crt  -text
```

<<<<<<< HEAD
=======
**Same with DER** (read .crl too):
```
openssl x509 -in cert.crt -inform der -text
```

>>>>>>> fb2b4e1dc2dce326e4640cb965be1e624dd23482
**Verify a certificate:**
```
openssl verify -CAfile <(cat Intermediate.pem RootCert.pem) UserCert.pem
```
<<<<<<< HEAD
=======

**Download and show info on an online certificate**
```
 openssl s_client -showcerts -connect DOMAIN:443 </dev/null 2>/dev/null | openssl x509 -text
 ```
>>>>>>> fb2b4e1dc2dce326e4640cb965be1e624dd23482
