# nRF52840 Dongle NVRAM Wipe Helper

When NVRAM gets corrupted, the ZBOSS NCP firmware can fail repeatedly and the dongle may not recover by itself.
The `blinky-nRF52840dongle-wipe.hex` image is used to wipe the problematic area and reset the device state.

## Recovery Process

1. Flash `blinky-nRF52840dongle-wipe.hex`.
2. (Optional) Open minicom to monitor logs.
3. Hold the dongle switch for about 3 seconds.
4. Flash back the normal ZBOSS NCP firmware (`.hex`).

## Example Minicom Output

```text
$ minicom -s

Welcome to minicom 2.9

OPTIONS:
Compiled on Sep 22 2023, 21:10:41.
Port /dev/tty.usbmodem11101, 14:34:20

Press Meta-Z for help on special keys

*** Booting nRF Connect SDK v3.2.0-5dcc6bd39b0f ***
*** Using Zephyr OS v4.2.99-a57ad913cf4e ***
Hold SW0 for ~3s to FULL WIPE (erase everything except app + DFU bootloader) and reboot.
Short press; ignoring wipe request.
FULL WIPE requested: erasing everything except app + DFU bootloader...
FLASH: base=0x0 size=0x100000 erase_block=0x1000
KEEP: merged=[0x0..0xe000)
KEEP: dfu_boot=[0xe0000..0x100000)
ERASE: [0xe000..0xe0000) len=0xd2000
... erased up to 0x1e000
... erased up to 0x2e000
... erased up to 0x3e000
... erased up to 0x4e000
... erased up to 0x5e000
... erased up to 0x6e000
... erased up to 0x7e000
... erased up to 0x8e000
... erased up to 0x9e000
... erased up to 0xae000
... erased up to 0xbe000
... erased up to 0xce000
... erasing page @0xdc000 len=0x1000
... done page @0xdc000 erased=1
... erasing page @0xdd000 len=0x1000
... done page @0xdd000 erased=1
... erased up to 0xde000
... erasing page @0xde000 len=0x1000
... done page @0xde000 erased=1
... erasing page @0xdf000 len=0x1000
... done page @0xdf000 erased=1
ERASE: range complete [0xe000..0xe0000)
DFU probe:
READ 0x000e0000: 18 59 00 20 c9 03 0e 00 d1 03 0e 00 d3 03 0e 00
READ 0x000ffff0: ff ff ff ff ff ff ff ff ff ff ff ff ff ff ff ff
Full wipe complete (application + DFU bootloader preserved).
Rebooting (rc=0)...
```
