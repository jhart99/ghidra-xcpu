## Ghidra CPU module for RDA MIPS processors
My (possibly) incomplete Ghidra processor module for RDA SOC processors.  RDA makes many different MIPS CPUs for radios, cell phones and bluetooth devices such as RDA8809, RDA8955 and RDA5851 processors.

Currently status:
* Disassembly of most firmware from RDA SOCs
* Programs compiled by the mips-rda-elf toolchain

Todo:
* A few opcodes in ROM are unknown/undocumented
* Some coprocessor opcodes are totally unknown especially within VOC code and COP2 code
* Occasional problems with MIPS32/MIPS16e switching in Ghidra.  Low bit flipping works, but sometimes JALR and JALX will fail to switch correctly.

Based upon datasheets, these processors seem to be MIPS R4000 like with both MIPS32 and MIPS16e modes and no MIPS64 mode.  It doesn't have floating point operations, but does have some additional FMA operations.

Some of the undocumented opcodes are just taken from the MIPS specs.
