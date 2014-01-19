# stk500boot_atmega256rfr2

Changes to the standard STK500 bootloader to support the ATMega256RFR2
(used by the MeshThing).

# Building

To build the firmware for the meshthing or the ATMega256RFR2 Xplained
Pro.

```
make meshthing
```

To write the firmware to the board.

```
make flash
```

# Notes

For those of you trying to use this with the ATMega256RFR2 Xplained
board there is a change required to flash it as it uses a slightly
different chip to the meshthing.

```
diff --git a/Makefile b/Makefile
index fe6c441..b0e136f 100644
--- a/Makefile
+++ b/Makefile
@@ -36,7 +36,7 @@

 # MCU name
 #MCU = atmega128
-MCU = atmega2564rfr2
+MCU = atmega256rfr2

 #Fuse Settings
 FUSES      = -U hfuse:w:0xd8:m -U lfuse:w:0xef:m
```

# License
Licensed under the GPLv2 license.

