# Ajs38RO4Vz-p

This repo contains a list of artifacts. 

CHERI-Toooba: 
The cache system related changes are placed mainly within Toooba/src_Core/RISCY_OOO/coherence/src, where we detect access to a poisoned memory, also mark and replaced poisoned cache lines. 

The pipeline related changes are placed within, Toooba/src_Core/RISCY_OOO/procs, that includes the implementation of new instructions such as cpoison, cgetcappoison etc. 

Changes to CHERI architecture are placed within, Toooba/libs/cheri-cap-lib, where the reserved bits in capability are defined as POISON, PERM_POISON permission, POISON_VERSION. 

QEMU: 


SQlite: 
the changes that are related to nested temporal safety are placed within src/mem5.c, where we modified MEMSYS5 allocator of SQLite to have CHERI spatial safety, and PoisonCap nested temporal safety. 

Juliet-test-suite:
The juliet test suite test cases we used are placed within, Juliet-test-suite-cases.


