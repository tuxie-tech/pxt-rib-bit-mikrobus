---
layout: layouts/catalog-page
title: Rib:bit MikroBUS TypeScript Reference
---

## Overview

This page documents the TypeScript-facing API for Rib:bit MikroBUS.

If you are learning, start with [Rib:bit MikroBUS Support](../) and [Rib:bit MikroBUS Blocks Guide](../blocks/).

## Quick call summary

- Power: `switchMBus()`
- Serial writes: `serialWriteLine()`, `serialWriteValue()`, `serialWriteNumber()`, `serialWriteString()`, `serialWriteNumbers()`
- Serial reads (placeholders): `serialReadLine()`, `serialReadUntil()`, `serialReadString()`, `getBytesAvailable()`, `serialSetBaud()`, `onStringReceived()`, `onDelimiterReceived()`
- Pins: `setPWMPin()`, `analogRead()`, `analogWrite()`, `spiSelectMBus()`, `setResetPin()`

## Example

```ts
RibBitMBus.switchMBus(RibBit.OnOff.On)

basic.forever(function () {
    RibBitMBus.serialWriteValue("analog", RibBitMBus.analogRead())
    basic.pause(1000)
})
```

## API details

- API index: [Rib:bit MikroBUS API Index](../api/)
- Namespace details: [Rib:bit MikroBUS Namespace](../namespace_ribbitmbus/)
- Shared enums: [On Off Enum](../../pxt-rib-bit/enum_onoff/), [Serial Baud Enum](../../pxt-rib-bit/enum_serialbaud/)
