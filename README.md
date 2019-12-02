# SBC6802 plus Bus

[Ja](READMEj.md) | En

Rev. 1

![board1](graphics/sbc6802board12a.png)

A single board computer with Motorola 6802. Compatible with SBC-Bus 2.0.
The board design is derived from SBC6800 and SBC6809.

## Features

* MC6802 1MHz
* RAM 32KB (0x0000 - 0x7fff)
* ROM 16KB (0xc000 - 0xffff x two banks, selectable using JP1)
* ACIA (0x8018/0x8019)
* SBC-Bus 2.0 Connector

The actual board is tested with MC68B02 / MC68B50. MC6800 (the 1MHz version of the processor) has not been tested at this moment.

## In This Repository

Some important files:

* [Schematic](sbc6802_sch.pdf)
* [Gerber](sbc6802_gerber_osh.zip)
* [BOM](sbc6802_BOM.pdf)

## SBC-Bus

The bus connector supports [SBC-Bus 2.0](https://store.shopping.yahoo.co.jp/orangepicoshop/pico-a-008.html). Pin 38 is routed to 6802 VMA.

If not using the SBC-Bus, connect the 5V and GND pins to a separate power source.

## Software

Most of the 6800 software found in [SBC6800 datapack](http://www.amy.hi-ho.ne.jp/officetetsu/storage/sbc6800_datapack.zip) are compatible with SBC6802.

## Errata

### Rev. 1

* The front silk for D1 shows wrong polarity. Connect the kathode to the left pad of footprint D1.
* The crystal Y1 should be slightly raised from the PCB so that it would not interfere with D1 and other parts nearby.
* The input pins of unused gates in U2 are not grounded. Wire pins #9, #11 and #13 to the ground.

## References

* [SBC6800](https://www.switch-science.com/catalog/3581/)
* [SBC6809](https://www.switch-science.com/catalog/3583/)
* [SBC-Bus 2.0](https://store.shopping.yahoo.co.jp/orangepicoshop/pico-a-008.html)
* [as0 Motorola 6800 Assembler](https://github.com/JimInCA/motorola-6800-assembler)
* [M6800 Assembly VSCode Extension](https://marketplace.visualstudio.com/items?itemName=RyuStudio.m6800-as0)
