ACM CCS 2026 open science artifacts submission

This is a repository of all artifacts associated with our PoisonCap paper submission. It contains copies of our source code for our CHERI-enabled LLVM and QEMU fork, CheriBSD fork and CHERI-Toooba that has PoisonCap hardware, and software PoisonCap implementations. It also contains our fork of SQLite, and a list of Juliet Test Cases we have run.

## Relevant Files
### CHERI-Toooba: 
The cache system related changes are placed mainly within Toooba/src_Core/RISCY_OOO/coherence/src, where we detect access to a poisoned memory, also mark and replaced poisoned cache lines. 

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


