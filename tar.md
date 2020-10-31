# Tar

**Decompress things:**

```sh
tar xf archive.tar
tar xvzf archive.tar.gz
tar xjf archive.tar.bz2
tar xtvf file.tar.gz | grep <WORD>
tar -C <DEST> -xvf <FILE>
unzip archive.zip
gzip -d archive.gz

# read a gz file without decompressing
zcat archive.gz
zless archive.gz
zgrep <WORD> /var/log/mailliog*.gz

# Search instide a zip archive
zipgred *.txt archive.zip
```

**Compress things:**

```sh
zip -r file.zip /dir/*
tar cf archive.tar files
tar czf archive.tar.gz files
tar cjf archive.tar.bz2 files
gzip file
```
