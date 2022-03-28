# KST3620 Packets Types

## Uplink

One payload is sent with both Temperature & Battery packets concatenated.
Temperature uplinks are in 2's Complement notation. Check the documentation
in the Javascript Parser for more detail.

Example: `006702FE980078021152`

| Packet Type      | Key      | Length | Value    |
|------------------|----------|--------|----------|
| Temperature (°C) | `0x0067` | `0x02` | `0xFE98` |
| Battery (mV)     | `0x0078` | `0x02` | `0x1152` |

## Downlink

A downlink payload can be sent to change the uplink interval time in minutes.

Example: `0100010F` = Set Uplink Interval to 15mins

| Packet Type     | Key      | Length | Value           |
|-----------------|----------|--------|-----------------|
| Uplink Interval | `0x0100` | `0x01` | `0x0F` (15mins) |
