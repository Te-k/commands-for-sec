# lldb

* Launch process: `process launch --stop-at-entry`
* Disassemble at a specific address: `d -s 0x100001080`
* Set breakpoint at an address: `br s -a 0x10000`
* Print data: (b for byte, w for word, c for char, x for hex, s for string): `x/40bx $rdx`
* Step in: `step` or `s`
* Step over: `next` or `n`
* Print variable value: `p $r12`
* Print all registries values: `re r -f i`
* List binary and libraries loaded : `image list`
* List sections : `image dump sections`

