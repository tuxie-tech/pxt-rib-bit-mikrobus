---
layout: layouts/catalog-page
title: Rib:bit MikroBUS Blocks Guide
---

## Overview

This page is a visual-blocks-first guide for learners. Every block lives in the **Rib:Bit MikroBUS** category of the MakeCode toolbox, and each block label ends with a warning sign that marks it as a Rib:bit hardware block.

Block images are not generated automatically in this pass. Use the placeholders to insert transparent PNG block captures.

## Suggested block walkthrough order

1. Switch the MikroBUS socket on.
2. Write text to the Click board over serial.
3. Use the pin blocks if your Click board needs PWM or analog.
4. Reach for the advanced blocks only when you need them.

## Power

| Block | What it does |
| --- | --- |
| `switch microbus $state` | Turns power to the MikroBUS socket on or off. |

- Placeholder: insert transparent PNG for the power block.

## Serial Port

| Block | What it does |
| --- | --- |
| `mikroBUS serial write line $text` | Sends text followed by a new line. |
| `mikroBUS serial write value $field = $value` | Sends a name and value as `name = value`, followed by a new line. |
| `mikroBUS serial write number $value` | Sends a number as text. |
| `mikroBUS serial write string $text` | Sends text as it is, with no new line. |
| `mikroBUS serial write numbers $values` | Sends a list of numbers separated by commas, followed by a new line. |
| `mikroBUS serial read line` | Placeholder. Returns empty text in this version. |
| `mikroBUS serial read until $delimiter` | Placeholder. Returns empty text in this version. |
| `mikroBUS serial read string` | Placeholder. Returns empty text in this version. |
| `mikroBUS serial bytes available` | Placeholder. Returns 0 in this version. |
| `set mikroBUS serial baud to $baud` | Advanced. Placeholder. Does nothing in this version. |
| `on mikroBUS string received` | Advanced. Placeholder. Never runs in this version. |
| `on mikroBUS $delimiter received` | Advanced. Placeholder. Never runs in this version. |

- Placeholder: insert transparent PNGs for the serial write blocks.

## Pin Functions

| Block | What it does |
| --- | --- |
| `set mikroBUS PWM pin to $value` | Sets the pulse width, in microseconds, on the PWM pin (micro:bit pin P0). |
| `mikroBUS analog pin value` | Reads the analog pin (micro:bit pin P1). |
| `mikroBUS analog pin set value to $value` | Writes an analog value to the analog pin (micro:bit pin P1). |
| `set mikroBUS select line to $state` | Advanced. Selects the Click board's chip-select line (micro:bit pin P12). |
| `reset mikroBUS port` | Advanced. Resets the MikroBUS port. |

- Placeholder: insert transparent PNGs for the pin blocks.

## Next steps

- TypeScript docs: [Rib:bit MikroBUS TypeScript Reference](../typescript/)
- Full API map: [Rib:bit MikroBUS API Index](../api/)
