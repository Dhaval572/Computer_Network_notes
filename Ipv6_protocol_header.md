## 🔹 IPv6 Header Format

| Field              | Size (bits) | Description                          |
|-------------------|------------|----------------------------------|
| Version          | 4          | IPv6 version (always 6)         |
| Traffic Class   | 8          | Used for QoS priority           |
| Flow Label      | 20         | Used for packet flow identification |
| Payload Length  | 16         | Length of the payload in bytes  |
| Next Header     | 8          | Identifies the type of the next header |
| Hop Limit       | 8          | Decremented by each router (like TTL in IPv4) |
| Source Address  | 128        | IPv6 source address             |
| Destination Address | 128    | IPv6 destination address        |
