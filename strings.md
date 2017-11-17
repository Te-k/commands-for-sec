# Strings

**Search for unicode strings (16-bit little endian encoding here)**
```
strings -el FILE
(s = single-7-bit-byte characters (ASCII, ISO 8859, etc., default), S = single-8-bit-byte characters, b = 16-bit bigendian, l = 16-bit littleendian, B = 32-bit bigendian, L = 32-bit littleendian)
```

**Print offset in decimal**
```
strings -td FILE
```
