# IPv4 Address Classes

In IPv4, IP addresses are divided into five classes: **A, B, C, D, and E**. These classes are defined based on the range of their first octet and their intended use. Here's a breakdown of each class:

---

## **Class A**
- **Range**: `1.0.0.0` to `126.0.0.0`
- **First octet range**: 1 to 126
- **Purpose**: Designed for very large networks.
- **Subnet mask**: `255.0.0.0` (/8)
- **Network bits**: 8 bits (first octet)
- **Host bits**: 24 bits (3 octets)
- **Total networks**: 126 (2^7 - 2, as 0.0.0.0 and 127.0.0.0 are reserved)
- **Hosts per network**: 16,777,214 (2^24 - 2)

---

## **Class B**
- **Range**: `128.0.0.0` to `191.255.0.0`
- **First octet range**: 128 to 191
- **Purpose**: Designed for medium to large networks.
- **Subnet mask**: `255.255.0.0` (/16)
- **Network bits**: 16 bits (first 2 octets)
- **Host bits**: 16 bits (last 2 octets)
- **Total networks**: 16,384 (2^14)
- **Hosts per network**: 65,534 (2^16 - 2)

---

## **Class C**
- **Range**: `192.0.0.0` to `223.255.255.0`
- **First octet range**: 192 to 223
- **Purpose**: Designed for small networks.
- **Subnet mask**: `255.255.255.0` (/24)
- **Network bits**: 24 bits (first 3 octets)
- **Host bits**: 8 bits (last octet)
- **Total networks**: 2,097,152 (2^21)
- **Hosts per network**: 254 (2^8 - 2)

---

## **Class D**
- **Range**: `224.0.0.0` to `239.255.255.255`
- **First octet range**: 224 to 239
- **Purpose**: Reserved for **multicasting** (sending data to multiple devices simultaneously).
- **No subnet mask**: Not used for individual devices or networks.
- **Not divided into network/host portions**.

---

## **Class E**
- **Range**: `240.0.0.0` to `255.255.255.255`
- **First octet range**: 240 to 255
- **Purpose**: Reserved for experimental or future use.
- **Not used in practice**: These addresses are not assigned to devices or networks.

---

## **Special Notes**:
- **Reserved addresses**:
  - `0.0.0.0`: Default route or "this network."
  - `127.0.0.0` to `127.255.255.255`: Loopback addresses (e.g., `127.0.0.1` for localhost).
  - `255.255.255.255`: Limited broadcast address.
