# Yara

**Rule example :**

```
rule EXAMPLE {
    meta:
        author = "ME"

    strings:
        $s1 = "string" ascii

    condition:
        all of them
}
```

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

**Hex strings:**
```
$hex_string = { E2 34 ?? C8 A? FB }
```

**Check for doc header with macro:**
```
    strings:
        $a = {d0 cf 11 e0}
        $b = {00 41 74 74 72 69 62 75 74 00}
    condition:
        $a at 0 and $b
```
