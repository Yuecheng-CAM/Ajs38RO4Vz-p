ACM CCS 2026 open science artifacts submission

This is a repository of all artifacts associated with our PoisonCap paper submission. It contains copies of our source code for our CHERI-enabled LLVM and QEMU fork, CheriBSD fork and CHERI-Toooba that has PoisonCap hardware, and software PoisonCap implementations. It also contains our fork of SQLite, and a list of Juliet Test Cases we have run.

## Relevant Files
### CHERI-Toooba: 
- `Toooba/src_Core/RISCY_OOO/coherence/src/`, the cache system related changes are placed mainly within Toooba/src_Core/RISCY_OOO/coherence/src, where we detect access to a poisoned memory, also mark and replaced poisoned cache lines. 

The pipeline related changes are placed within, Toooba/src_Core/RISCY_OOO/procs, that includes the implementation of new instructions such as cpoison, cgetcappoison etc. 

Changes to CHERI architecture are placed within, Toooba/libs/cheri-cap-lib, where the reserved bits in capability are defined as POISON, PERM_POISON permission, POISON_VERSION. 

### QEMU: 
codes that are relevant:
qemu/target/cheri-common/op_helper_cheri_common.c, cheri-helper-utils.h, cheri_tagmem.c, cheri-helper-common.h, cheri_utils.h, 

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
