# LUKS

**Open encrypted device** :
```
cryptsetup --type luks open /dev/sdb1 encrypted
```

**Close encrypted drive:**
```
cryptsetup close encrypted
```

**Format drive:**
```
cryptsetup luksFormat -c aes-xts-plain64 --key-size 512 --hash sha512 --use-urandom /dev/sdb1
```
