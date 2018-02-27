# Yara

**Consider only files with MZ header**
```bash
    condition:
        uint16(0) == 0x5A4D and 3 of the
```

**Consider only files with MZ and PE header**
```bash
    condition:
        uint16(0) == 0x5A4D and uint32(uint32(0x3C)) == 0x00004550 and 2 of them
```

**Consider only a sublist of strings**:
```
strings:
    $mandatory = "aa"
    $optional1 = "bb"
    $optional2 = "cc"
    $optional3 = "dd"
condition:
    $mandatory and 2 of ($optional*)
```
