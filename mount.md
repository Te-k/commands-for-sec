# Mount

**Mount CIFS (you need cifs-utils):**
```bash
mount -t cifs -o username=robert,password=foobar123 //192.168.1.11/videos /mnt/vids
```

**Mount Windows drive image for forensic analysis**
```bash
mount -o ro,loop,shows_sys_files,streams_interface=windows img.dd /mnt
```

**Mount a specific partition of a Windows drive image:**
```bash
mount -o ro,loop,shows_sys_files,streams_interface=windows,offset=32256 img.dd /mnt
```
