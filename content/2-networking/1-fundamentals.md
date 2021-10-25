---
title: 'Fundamentals of Networking'
metaTitle: 'Networking fundamentals'
metaDescription: 'Networking fundamentals'
---

## The Open Systems Interconnection Model (OSI Model)

The **OSI** model is a conceptual model formalized in the 80's.

It's a big picture view of what's hapening from a hardware-to-application-to-hardware within a computer network.

It's made of layers, each communicating with the one above or below it, and a protocol that governs what happens at each layer.

It is used to lay out basic standards and rules for **different devices from different manufacturers to communicate on a network**.

|     | Layer       | Protocol          | Data Unit | Endpoint    |
| --- | ----------- | ----------------- | --------- | ----------- |
| 5   | Application | HTTP, HTTPS, SMTP | Messages  | n/a         |
| 4   | Transport   | TCP/UDP           | Segment   | Port number |
| 3   | Network     | IP                | Datagram  | IP Address  |
| 2   | Data Link   | Ethernet, WiFi    | Frames    | MAC address |
| 1   | Physical    | 10 Base T, 802.11 | Bits      | n/a         |

**Data packet** = An all encompassing term that represents any single set of binary data being sent across a network link.

## Ethernet

The primary purpose of this layer is to **abstract away** the need for any other layers **to care about the physical layer** and **what hardware** is being used.

**Media Access Control Address (MAC)** is a globally unique number to identify network cards on a device.

### Dissecting an Ethernet Frame

An **ethernet frame** is a highly structured collection of information presented in a specific order.

This way, network interfaces at the physical layer can convert a stream of bits into meaningful data.

![Ethernet Frame](./images/ethernet-frame.png)

- **Preamble**: Is a buffer between frames.
- **Start Frame Delimeter (SFD)**: Signals that the preamble is over and the actual frame contents will now follow.
- **Destination MAC address**: The hardware address of the intended recipient.
- **Source MAC addres**: Where the frame originated from.
- **Ether-type**: 16 bits long, used to describe the protocol of the contents of the frame.
- **VLAN header**: Can be found instead of the **ether-type** which indicated whether the frame itself is what's called a VLAN frame. If it is present, the **ether-type** field follows it.
  - **VLAN** = **Virtual LAN** = Is a technique that lets you have multiple logical LANs operating on the same physical equipment.
- **Payload**: The actual data being transported.
- **Frame Check Sequence (FCS)**: Checksum value for the entire frame.

## Internet Protocol

On a **Local Area Network (LAN)**, nodes can communicate with each other through their physical MAC addresses because switches can learn the MAC addresses connected to each of their port to forward transmissions appropriately.

But that doesn't scale well. There is **no way of knowing where in the world a specific MAC address will be at any point of time** .

**Adress Resolution Protocol (ARP)**, which is how nodes learn about each other's MAC addresses on a network, is not translatable to anything besides a single network segment.

**In come the Network Layer and the IP Protocol**.

## IP Addressing

An IP address is a unique number that identifies a computer on a network.

**192.168.2.14:80** is composed of

- Network portion,
- Host portion,
- Port.

### IPv4

**IPv4** was created in the 80's it is a **32 bit address**.

Ex: **192.168.2.14** is composed of 4 sections, each 8 bits

There are ~4.3 billion addresses.

Because there are so many devices on the network, **IPv4 addresses** are running out.

Let's take a look at **192.168.2.14:80**

- The first 3 octets are the **network ID**
  - Tells the router **which network** to send the data to.
- The 4th octet identifies the particular **device** on the **network ID**
  - Tells the router which device on the network.
- :80 represents the port on the target device.

### IPv6

**IPv6** was adopted as a standard in 2017, it is a **128 bit address**.

**There are 340 trillion trillion trillion addresses (not a typo).**

### Network Address Translation (NAT).

**NAT** will route data from your **public IP address** to your **internal IP addresses**.

This allows you to have your **private local area network (LAN)** with 10 devices on it, each with its **own IP address on the LAN**, and your **ISP (Internet Service Provider)** provides you with your own single **Public IP**, so that when different computers connect to your computer, they **first connect to your public IP** and **Network Address Translation (NAT) routes the traffic to the correct device.**

### Network Port

A **Network Port** is associated with IP address and **identifies an application or service running on a networked device**.

- The first 1023 ports are reserved for well-known services like
  - **SMTP**: port 25
  - **DNS** port 53
  - **HTTP**: port 80
  - **HTTPS**: port 443

## Network Classes & Subnetting

**Public IPs are handled by large organizations and they assign out blocks of IPs based on geographic regions**.

![Network Classes](./images/network-classes.png)

### Subnetting

**Subnetting** is dividing a network into smaller networks.

We use a **subnet mask** to define which part of the **IP address** is used for the **network ID** and which part is used for the **host**.

#### Reasons for Subnetting

- Small networks are easier to manage than large networks.
- You get a better allocation of IP addresses in a limited range.
- With smaller networks you get better network performance.
