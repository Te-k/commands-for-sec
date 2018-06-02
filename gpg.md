# GPG

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
