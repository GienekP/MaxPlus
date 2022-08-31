# MaxPlus

Cartridge project for ATARI XE computers based on ATF22V10C

Depending on the version of JED, you can do:
-  Atarimax 128 KB Flash cartridge
-  MaxFlash 128kB PLUS cartridge
-  Atarimax 1 MB Flash cartridge (old/new) for 512kB flash memory
-  JAC512kB cartridge


Upgraded Format:

"MaxFlash 128kB PLUS"

This bank-switched cartridge occupies 8 KB of address space between $A000 and $BFFF. The cartridge memory is divided into 16 banks, 8 KB each. The 4 lowest bits of the ADDRESS written to $D500-$D50F select the bank mapped to $A000-$BFFF. Writing to $D510-$D51F disables the cartridge. Additionally, the 2 lowest bits of the address written to $D520-$D52F select the "side" of SST39SF020A/SST39SF040"


SST39SF010A - 128kB

SST39SF020A - 256kB (2 sides)

SST39SF040 - 512kB (4 sides)



STA $D500 - select bank 0 (first)

STA $D503 - select bank 3

STA $D50F - select bank 15 (last)

STA $D51X - disable cartridge

STA $D520 - select side 0 (standard maxflash)

STA $D521 - select side 1 (only SST39SF020A & SST39SF040)

STA $D522 - select side 2 (SST39SF040)

STA $D523 - select side 3 (SST39SF040)


The presented solution can be used unlimitedly and freely without any legal obligations, especially in the field of educational, commercial and non-commercial activities.
