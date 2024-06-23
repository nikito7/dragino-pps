# dragino-pps
Dragino Allwinner H3. Stratum 1 GPS Clock. PPS on uart1 rx PG7.


# Debug

If it's ok only shows two tty:

```
dmesg | grep serial
[    1.509044] 1c28000.serial: ttyS0 at MMIO 0x1c28000 (irq = 52, base_baud = 1500000) is a 16550A
[    1.510237] 1c28800.serial: ttyS1 at MMIO 0x1c28800 (irq = 53, base_baud = 1500000) is a 16550A
```

PPS registered ok.

Ignore pps1 from usb.
```
dmesg | grep pps
[    1.184551] pps_core: LinuxPPS API ver. 1 registered[    1.184558] pps_core: Software ver. 5.3.6 - Copyright 2005-2007 Rodolfo Giometti <giometti@linux.it>
[    6.775717] pps pps0: new PPS source pps@0.-1
[    6.775838] pps pps0: Registered IRQ 112 as PPS source
[   19.312814] pps_ldisc: PPS line discipline registered
[   19.315655] pps pps1: new PPS source acm0
[   19.315734] pps pps1: source "/dev/ttyACM0" added
```
