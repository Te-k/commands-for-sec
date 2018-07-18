# GPG

**Send a key to a gpg server:**
```
gpg --send-key 123456
```

**Receive a key from a server:**:
```
gpg --keyserver certserver.pgp.com --recv-keys 1234556
```

**Sign a file with detached signature**:
```
gpg --output FILE.sig --detach-sign FILE
```

**Verify a signature**:
```
gpg --verify FILE.sig FILE
```

**Export a public key:**
```
gpg --export -a "User Name" > public.key
```

**Export a public key:**
```
gpg --export-secret-keys -a Username
```

**List signatures:**
```
gpg --list-sigs
```

**Sign a key:**
```
gpg --sign-key --ask-cert-level someone@example.com
```
(Then you need to send the key to the server if you want to publish it)
