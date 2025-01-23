# IP Address

An **IP address** (Internet Protocol address) is a unique identifier assigned to each device on a network. It serves as the address that allows devices to communicate with each other over the internet or a local network.

- Every device connected to a network has its own IP address for communication.
- An IP address consists of two parts:
  1. **Network Address**
  2. **Host Address**

## Network Address:
- The **network address** is a number assigned to a specific network.
- Every network will have a unique network address that identifies it from other networks on the internet or local network.
- This address ensures that data sent across the internet is routed to the correct network.

## Host Address:
- The **host address** is assigned to devices (such as computers, servers, printers, etc.) within the network.
- Every device within a network will have a unique host address.
- The combination of the network address and host address forms the complete IP address, which uniquely identifies each device within its network.

Since IP addresses consist of a network part and a host part, networks can be logically divided into smaller sub-networks, a process known as **subnetting**. Subnetting helps manage IP address allocation more efficiently and securely by creating smaller network segments.

---

# Subnet Mask

A **subnet mask** is a number that looks similar to an IP address. It is used to define the boundaries of the network part of the IP address by masking the network portion. The subnet mask helps routers and other network devices understand which part of an IP address corresponds to the network and which part corresponds to the host.

## What does a Subnet Mask do?
- A subnet mask reveals how many bits in the IP address are used for the network portion by masking the network portion of the address.
- The bits used for the network are set to `1` in the subnet mask, while the bits used for the host are set to `0`. This division helps devices distinguish between the network and host parts of an IP address.

### Example:
For an IP address like `192.168.1.1` and a subnet mask of `255.255.255.0`, the subnet mask shows that the first three octets (`192.168.1`) are used to identify the network, and the last octet (`1`) is used to identify the specific host in the network.

In summary, an IP address combined with a subnet mask allows devices to route data correctly within and between networks.
