ACM CCS 2026 open science artifacts submission

This is a repository of all artifacts associated with our PoisonCap paper submission. It contains copies of our source code for our CHERI-enabled LLVM and QEMU fork, CheriBSD fork and CHERI-Toooba that has PoisonCap hardware, and software PoisonCap implementations. It also contains our fork of SQLite, and a list of Juliet Test Cases we have run.

## Relevant Files
### CHERI-Toooba: 
- `Toooba/src_Core/RISCY_OOO/coherence/src/`, contains PoisonCap changes to memory subsystem include extension to cache replacement algorithm, and store-after-free detection logic
- `Toooba/src_Core/RISCY_OOO/procs`, contains the implementations of PoisonCap added instructions,and PoisonCap detection logic
- `Toooba/libs/cheri-cap-lib`, contains the implementation of PoisonCap extended CHERI capability format

### QEMU: 
- `qemu/target/cheri-common/`, contains the implementation of PoisonCap extended CHERI capability format, PoisonCap added instructions and memory access check 

### CheriBSD: 


### SQLite: 
the changes that are related to nested temporal safety evaluation on memsys5 allocator within SQLite are placed within src/mem5.c, where we modified MEMSYS5 allocator of SQLite to have CHERI spatial safety, and PoisonCap nested temporal safety. 

### Juliet-Test-Suite: 
The juliet test suite test cases we used are placed within, Juliet-test-suite-cases.

## Omissions

This repository is intended to be anonymized via <https://anonymous.4open.science>, which has a 2GB-per-user limit.
To avoid this limit we have removed the following irrelevant, redundant, or binary files:

- directories from `cheribsd/contrib` took up ~650MB of source files unrelated to IOCaps
- `cheribsd/sys/contrib` took up ~370MB of source files unrelated to IOCaps
- `qemu/roms` took up ~660MB and contained binary boot ROMs unrelated to IOCaps

We have also removed `*.git*` files throughout.
