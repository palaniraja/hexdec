# HEXDEC

A simple hexa-decimal to decimal convertor. A faster way of reading your hex dump with custom parsing by defining presets.

**Presets** - Allows you to define your data parsing syntax 

e.g., If your hex data is `68 3C 6D 74` and you need to parse first two bytes as one value and 3rd and 4th byte in the sequence as their own values. Then you define your preset to be `2,1,1` then the hex data will be parsed as `15464 109 116` each data in your preset parsed as little-endian by default. 

Demo: [https://palaniraja.github.io/hexdec/](https://palaniraja.github.io/hexdec/)

---

### Little - Endian (default)

Hex: `68 3C 6D 74`

Preset: `2,1,1`

converts to `3C68 6D 74` => `15464 109 116`

---

### Big - Endian

Hex: `68 3C 6D 74`

Preset: `b,2,1,1` //to treat your bytes as big-endian

`683C 6D 74` => `26684 109 116`

---

### Preset Headers

Hex: `68 3C 6D 74`

Preset: 
```
First and Second Bytes, 3rd Byte, 4th Byte
2,1,1
```

will display the data in table with first row treated as headers

<table><tbody><tr><th>First and Second Bytes</th><th> 3rd Byte</th><th> 4th Byte</th></tr><tr><td>15464</td><td>109</td><td>116</td></tr></tbody></table>
