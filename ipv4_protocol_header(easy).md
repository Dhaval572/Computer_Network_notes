# IPv4 Protocol Header

The **IPv4 (Internet Protocol version 4)** header is part of the packet that helps route data across the internet. The IPv4 header contains important information about the packet, like the source and destination addresses, as well as how the packet should be processed. Here's a breakdown of its fields:

## 1. Version (4 bits)
- Indicates the version of the IP protocol. For IPv4, this is always `4`.

## 2. IHL (Internet Header Length) (4 bits)
- Specifies the length of the header. The minimum value is 5 (which equals 20 bytes), and this value is in 32-bit words.
- If there are options (extra fields), this value will be greater than 5.

## 3. Type of Service (TOS) (8 bits)
- This field was originally used to specify how the packet should be handled in terms of priority and performance. It includes values like "delay," "throughput," and "reliability."
- It is rarely used today, but it can still influence routing decisions in some cases (e.g., QoS).

## 4. Total Length (16 bits)
- Specifies the total size of the packet (header + data) in bytes. This value can range from 20 to 65,535 bytes.

## 5. Identification (16 bits)
- This field helps with reassembling fragmented packets. If a large packet is broken into smaller fragments, each fragment gets the same identification number.

## 6. Flags (3 bits)
- Indicate control information related to fragmentation. These flags are:
  - **Bit 0**: Reserved (must be 0).
  - **Bit 1**: "Don't Fragment" (DF). If set, the packet cannot be fragmented.
  - **Bit 2**: "More Fragments" (MF). If set, this packet is part of a larger fragmented packet.

## 7. Fragment Offset (13 bits)
- Indicates the position of the fragment in the original packet. It helps reassemble the fragments in the correct order.

## 8. Time to Live (TTL) (8 bits)
- Specifies the maximum number of hops the packet can take before being discarded. This is used to avoid packets circulating forever due to routing errors. Each router decreases the TTL by 1, and if it reaches 0, the packet is discarded.

## 9. Protocol (8 bits)
- Specifies the higher-layer protocol used in the data portion of the packet. For example:
  - `1` = ICMP (Internet Control Message Protocol)
  - `6` = TCP (Transmission Control Protocol)
  - `17` = UDP (User Datagram Protocol)

## 10. Header Checksum (16 bits)
- A checksum for error-checking the header. It ensures the integrity of the header data. If the header is modified during transmission, the checksum will not match, and the packet is discarded.

## 11. Source Address (32 bits)
- The IP address of the sender (source) of the packet. This is a 32-bit address.

## 12. Destination Address (32 bits)
- The IP address of the receiver (destination) of the packet. This is also a 32-bit address.

## 13. Options (variable length, optional)
- This part is optional and is used for additional features like security, record route, timestamp, etc. If the IHL is greater than 5, it means there are options in the header.

## 14. Padding (variable length)
- Used to ensure that the header ends on a 32-bit boundary. Padding is added if necessary to align the header properly.

---

## Example IPv4 Header Structure (in simplified form)

### Simple Explanation:
Imagine you’re sending a letter:
- The **Version** is like writing "Letter Version 4" on the envelope.
- The **Source Address** is your home address.
- The **Destination Address** is your friend’s address.
- The **TTL** is like saying, "If this letter doesn’t reach my friend in 10 stops, throw it away."
- The **Protocol** is like saying, "This letter contains a birthday card (TCP) or a quick note (UDP)."

The rest of the fields help make sure the letter gets to your friend in one piece and in the right order!
