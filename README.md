## Ghidra CPU module for RDA MIPS processors
RDA makes many different MIPS CPUs for radios, cell phones and
bluetooth devices such as RDA8809, RDA8955 and RDA5851 processors.

This module can be added to
[Ghidra](https://github.com/NationalSecurityAgency/ghidra) to allow
dissassembly of firmware using these CPUs.  This family of processors
has a slightly different mix of available operations than any of the
MIPS processors built into Ghidra.

Currently status:
* Disassembly of the firmware I could find from SDKs and programmed to
  devices.
* Programs compiled by the mips-rda-elf toolchain

Todo:
* Two opcodes in the ROM is currently unknown.  They do cache
  invalidation and are undocumented.
* Occasional problems with MIPS32/MIPS16e switching in Ghidra.  Low
  bit flipping works, but sometimes JALR and JALX will fail to switch
  correctly. If you encounter this issue, clear the disassembly and
  manually select MIPS32 or MIPS16e to fix the code block.
