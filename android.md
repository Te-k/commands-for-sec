# Android

**See apk permissions**:
```
aapt l -a app.apk
```

**Convert Android xml to xml using androguard:**
```
androaxml -i content/AndroidManifest.xml
```

**Check certificates**:
```
keytool -printcert -file contents/META-INF/CERT.RSA
```

**Decompile with androguard :**
```
androdd.py -i FILENAME.apk -o OUTPUT_DIR
```

**Decompile with jadx**:
```
jadx -d out classes.dex
```

**Compare two APK with androguard :**
```
Androsim.py -i FILENAME_1.apk FILENAME_2.apk -c ZLIB -n
```
