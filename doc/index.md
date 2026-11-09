---
layout: layouts/catalog-page
title: Rib:bit MikroBUS Support
hero: rib-bit-hero.png
info: >-
    Rib:bit MikroBUS adds blocks for the Rib:bit's MikroBUS socket, including socket power, serial output, and the PWM, analog, select, and reset pins.
plugins:
    - ts-to-blocks
tags:
    - software
    - api
    - makecode
    - blocks
    - rib:bit
---

## Overview

Rib:bit MikroBUS lets you power the MikroBUS socket on the Rib:bit and talk to the Click board plugged into it, using beginner-friendly blocks.

This page is the learner-first starting point. If you are new, begin with blocks and only jump into TypeScript when you need deeper control.

This version covers socket power, serial writes, and the pin functions. The serial read and receive blocks are placeholders that return empty values for now.

## Add to MakeCode

1. Open [MakeCode for micro:bit](https://makecode.microbit.org/) and start a **New Project** (or open an existing one).
2. Click the **gear** menu at the top right, then choose **Extensions**.
3. Paste `https://github.com/tuxie-tech/pxt-rib-bit-mikrobus` into the search box and press Enter.
4. Click the **Rib:Bit MikroBUS** tile that appears. A **Rib:Bit MikroBUS** category is added to the block toolbox.

[Rib:bit Basics](../pxt-rib-bit/) is loaded automatically as a dependency, so you do not need to add it yourself.

To edit the extension itself, choose **Import** on the MakeCode home screen, then **Import URL**, and paste the same address.

## What you can build

- Projects that drive a Click board over serial
- Boards that need a PWM or analog signal from the socket
- Classroom experiments with the MikroBUS standard

## Learning path

- Start with blocks: [Rib:bit MikroBUS Blocks Guide](blocks/)
- Use TypeScript when ready: [Rib:bit MikroBUS TypeScript Reference](typescript/)
- Browse the full API structure: [Rib:bit MikroBUS API Index](api/)

## Example

This example powers the socket on, then sends a line of text over its serial port.

```ts
RibBitMBus.switchMBus(RibBit.OnOff.On)

RibBitMBus.serialWriteLine("hello world")
```

## More resources

- TypeScript namespace docs: [Rib:bit MikroBUS Namespace](namespace_ribbitmbus/)
- Shared enums: [On Off Enum](../pxt-rib-bit/enum_onoff/), [Serial Baud Enum](../pxt-rib-bit/enum_serialbaud/)
