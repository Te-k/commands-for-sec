# dd

**Copy an image to an sd card:**
```
dd bs=4M if=2018-11-13-raspbian-stretch.img of=/dev/sdX status=progress conv=fsync
```

**Exfiltrate the contents of an image via SSH to another machine, compressing (-C) the content.**

```sh
dd if=/dev/rdisk0s1s2s bs=65536 conv=noerror,sync | ssh -C user@<IP> "cat >/tmp/image.dd"
```
