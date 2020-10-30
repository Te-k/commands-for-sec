# (n)Vim


**Remove blank lines:**
```
:g/^$/d
```

**Remove return carriage:**
```
%s/^M//g
```

**Replace something:**
```
%s/origin/destination/g
```

**Sort lines:**
```
CTRL-V and select lines or do ggVG
:sort

For invert sort:
:%sort!

For numerical sort:
:sort n
```
