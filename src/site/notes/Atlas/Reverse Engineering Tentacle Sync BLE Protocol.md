---
{"dg-publish":true,"permalink":"/atlas/reverse-engineering-tentacle-sync-ble-protocol/","title":"Reverse Engineering Tentacle Sync BLE Protocol","tags":["🌱_Processing","reverse-engineering"],"updated":"2025-10-18T22:36:33.982-07:00"}
---


## Decoding
format: LSB(?)

### Advertising

#### Manufacturer Specific data in advertising packet

```
0000   0d ff 3f 04 01 01 93 18 06 33 18 10 1f 64
```

| data                          | meaning                                            |
| ----------------------------- | -------------------------------------------------- |
| 0d                            | Length                                             |
| ff                            | Type (manufacturer specific)                       |
| 3f 04                         | Company ID                                         |
| 01 01 93 18 06 33 18 10 1f 64 | _Current theory is that this is the timecode data_ |

Examples of the data:

```
0000   01 01 93 18 06 33 18 10 1f 64
0000   01 01 93 18 06 33 18 12 80 d2
0000   01 01 93 18 06 33 18 15 36 50
```

### Scan Response

```
0000   06 ff 3f 04 46 05 00 06 09 42 2d 43 41 4d
```

| data           | meaning                      |
| -------------- | ---------------------------- |
| 06             | Length                       |
| ff             | Type (manufacturer specific) |
| 3f 04          | Company ID                   |
| 46 05 00       | ???                          |
| 06             | Length                       |
| 09             | Type (device name)           |
| 42 2d 43 41 4d | `B-CAM`                      |

## References
- [Bluetooth SIG assigned numbers](https://www.bluetooth.com/specifications/assigned-numbers/)
## Raw Notes
- Company ID: 0x043f Tentacle Sync GmbH
- Advertised Services
	- 0x180F - Battery Service
- Scan Response
	- 06 ff 3f 04 46 05 00 06 09 42 2d 43 41 4d
