# SBC6802 plus Bus

Ja | [En](README.md)
Rev. 1.0

![board1](graphics/sbc6802board12a.png)

モトローラ 6802 を使用したシングルボードコンピュータです。電脳伝説様設計による SBC68 シリーズからの派生として作成しました。レトロな雰囲気様設計 SBC-Bus 2.0 対応のバスコネクタを装備しています。

現在製作テスト中のコンピュータですので本リポジトリには不完全な情報が多々含まれると思います。内容は随時追加変更する予定です。

## 搭載機能

本ボード搭載機能は以下の通りです。

* MPU MC6802 1MHz（内蔵 RAM は無効化）
* RAM 32KB（0x0000 - 0x7fff）
* ROM 16KB (0xc000 - 0xffff x ２ バンク、ジャンパ JP1 で選択)
* ACIA（0x8018/0x8019）
* SBC-Bus 2.0

## 主なファイル

* [回路図](sbc6802_sch.pdf)
* [Gerber](sbc6802_gerber_osh.zip)
* [部品表](sbc6802_BOM.pdf)

## SBC-Bus

SBC-Bus 2.0 の標準配線から 1 か所だけ変更があります。

* Pin 38: NC -> VMA

ご利用のシステムのピンアサインと競合する場合はパターンカットしてください。

電源供給とリセットボタンも SBC-Bus に依存します。SBC-Bus へ接続しない場合は、ボード下部のコネクタ端子から 5V、GND、Res*（リセット）などを取り出して接続してください。端子名はボード裏面のシルクに印刷されています。

## SBC6800 用ソフトウェアの使用

SBC6802 のメモリおよび ACIA アドレスは SBC6800 互換であるため [SBC6800 データパック](http://www.amy.hi-ho.ne.jp/officetetsu/storage/sbc6800_datapack.zip)に含まれる Mikbug.hex をそのまま EEPROM に焼けば動作します。未検証ですが、データパック内のその他のソフトウェアもほぼすべて使用可能だと思います。

## 参考リンク

* [SBC6800](https://www.switch-science.com/catalog/3581/)
* [SBC6809](https://www.switch-science.com/catalog/3583/)
* [SBC-Bus 2.0](https://store.shopping.yahoo.co.jp/orangepicoshop/pico-a-008.html)
* [as0 Motorola 6800 Assembler](https://github.com/JimInCA/motorola-6800-assembler)
* [M6800 Assembly VSCode Extension](https://marketplace.visualstudio.com/items?itemName=RyuStudio.m6800-as0)

