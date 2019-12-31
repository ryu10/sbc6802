# SBC6802 plus Bus

[Ja](READMEj.md) | En

Rev. 2

![boardr2](graphics/sbc6802r2-ab.png)

A single board computer with Motorola 6802. The board design is derived from SBC6800 and SBC6809.

## Features

* MC6802 1MHz
* RAM 32KB (0x0000 - 0x7fff)
* ROM 16KB (0xc000 - 0xffff x two banks, selectable using JP1)
* ACIA (0x8018/0x8019)
* SBC-Bus 2.0 Connector

## In This Repository

The following files are included, along with the KiCAD project:

* [Schematic](sbc6802_r2_sch.pdf)
* [Gerber](sbc6802_gerber_r2.zip)
* [BOM](sbc6802_r2_BOM.pdf)

## SBC-Bus

The bus connector J1 supports [SBC-Bus 2.0](https://store.shopping.yahoo.co.jp/orangepicoshop/pico-a-008.html). Pin 38 is routed to 6802 VMA.

If not using the SBC-Bus, connect the 5V and GND pins to a power supply.

## Software

Most of the 6800 software found in [SBC6800 datapack](http://www.amy.hi-ho.ne.jp/officetetsu/storage/sbc6800_datapack.zip) are compatible with SBC6802.

## References

* [SBC6800](https://www.switch-science.com/catalog/3581/)
* [SBC6809](https://www.switch-science.com/catalog/3583/)
* [SBC-Bus 2.0](https://store.shopping.yahoo.co.jp/orangepicoshop/pico-a-008.html)
* [as0 Motorola 6800 Assembler](https://github.com/JimInCA/motorola-6800-assembler)
* [M6800 Assembly VSCode Extension](https://marketplace.visualstudio.com/items?itemName=RyuStudio.m6800-as0)

## License

CC-BY-SA 3.0 by ryu10/RyuStudio, 2019.
Derived from the original works of SBC6800 and SBC6809 (c) 2017-2018 Tetsuya Suzuki.
