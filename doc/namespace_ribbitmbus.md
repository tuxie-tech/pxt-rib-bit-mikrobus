---
layout: layouts/catalog-page
title: Rib:bit MikroBUS Namespace
---

## Namespace `RibBitMBus`

MikroBUS socket control, serial, and pin calls. Appears in MakeCode as **Rib:Bit MikroBUS**.

## Power

### `switchMBus(state = RibBit.OnOff.On)`

- **Parameters:**
  - `state`: Desired socket power state.
- **Returns:** `void`
- **Description:** Turns power to the MikroBUS socket on or off by writing the controller's MikroBUS control register. Writing this register also releases the socket's SPI select.

## Serial writes

### `serialWriteString(text)`

- **Parameters:**
  - `text`: Text to send.
- **Returns:** `void`
- **Description:** Sends text, unchanged, to the MikroBUS serial port.

### `serialWriteLine(text)`

- **Parameters:**
  - `text`: Text to send.
- **Returns:** `void`
- **Description:** Sends text followed by a new line.

### `serialWriteValue(field, value)`

- **Parameters:**
  - `field`: Name to send.
  - `value`: Value to send.
- **Returns:** `void`
- **Description:** Sends `field = value` followed by a new line.

### `serialWriteNumber(value = 0)`

- **Parameters:**
  - `value`: Number to send.
- **Returns:** `void`
- **Description:** Sends a number as text, with no new line.

### `serialWriteNumbers(values)`

- **Parameters:**
  - `values`: Array of numbers.
- **Returns:** `void`
- **Description:** Sends the numbers separated by `, ` and followed by a new line.

## Serial reads (placeholders)

These calls exist so projects can be written against the final API, but they do not read from the port yet.

### `serialReadLine()`, `serialReadUntil(delimiter)`, `serialReadString()`

- **Parameters:** `delimiter` for `serialReadUntil()` only.
- **Returns:** `string`
- **Description:** Always return an empty string.

### `getBytesAvailable()`

- **Parameters:** None
- **Returns:** `number`
- **Description:** Always returns 0.

### `serialSetBaud(baud = RibBit.SerialBaud.BAUD_9600)`

- **Parameters:**
  - `baud`: Requested baud rate.
- **Returns:** `void`
- **Description:** Does nothing yet. Advanced.

### `onStringReceived(cb)` and `onDelimiterReceived(cb, delimiter = "\n")`

- **Parameters:**
  - `cb`: Callback receiving the received text.
  - `delimiter`: Delimiter to wait for (`onDelimiterReceived()` only).
- **Returns:** `void`
- **Description:** Accept a handler but never call it yet. Advanced.

## Pin functions

### `setPWMPin(value = 0)`

- **Parameters:**
  - `value`: Pulse width in microseconds.
- **Returns:** `void`
- **Description:** Sets the pulse width on micro:bit pin P0, which is wired to the socket's PWM pin.

### `analogRead()`

- **Parameters:** None
- **Returns:** `number`
- **Description:** Reads micro:bit pin P1, which is wired to the socket's analog pin.

### `analogWrite(value = 0)`

- **Parameters:**
  - `value`: Analog value to write.
- **Returns:** `void`
- **Description:** Writes an analog value to micro:bit pin P1.

### `spiSelectMBus(state)`

- **Parameters:**
  - `state`: `true` to select the socket, `false` to release it.
- **Returns:** `void`
- **Description:** First deselects every other SPI device on the Rib:bit, then drives micro:bit pin P12 low to select the socket (or high to release it). Advanced.

### `setResetPin()`

- **Parameters:** None
- **Returns:** `void`
- **Description:** Sends the MikroBUS reset command to the Rib:bit controller. Advanced.

## Used by

- [Rib:bit MikroBUS TypeScript Reference](../typescript/)
