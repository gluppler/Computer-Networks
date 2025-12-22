---

## 1. OSI Model Layers and Order

**Question:** The Open System Interconnection (OSI) reference model divides a network into seven layers. Which of the following lists the seven layers in the correct order, from bottom to top?
**Correct Answer: A. Physical layer, data link layer, network layer, transport layer, session layer, presentation layer, and application layer**

### Why A is correct:

The OSI model is a standardized framework used to understand network interactions. The "bottom-to-top" order refers to moving from the physical hardware (Layer 1) up to the user interface (Layer 7):

1. **Physical:** Binary transmission and cables.
2. **Data Link:** Physical addressing (MAC).
3. **Network:** Path determination and logical addressing (IP).
4. **Transport:** End-to-end connections and reliability.
5. **Session:** Interhost communication.
6. **Presentation:** Data representation and encryption.
7. **Application:** Network process to application.

### Why the others are incorrect:

* **B, C, & D:** These options shuffle the middle layers (Network, Transport, Session, and Presentation) out of their standardized sequence.

---

## 2. Telnet Port Number

**Question:** Which of the following port numbers is used by Telnet?
**Correct Answer: B. 23**

### Why B is correct:

Telnet is a legacy protocol used for remote terminal access. In the standard TCP/IP port assignments, Port **23** is specifically reserved for Telnet traffic.

### Why the others are incorrect:

* **A (6):** This is not a common well-known service port; 6 is actually the protocol number for TCP itself within an IP header.
* **C (17):** Reserved for the "Quote of the Day" (QOTD) protocol.
* **D (21):** This port is used by **FTP** (File Transfer Protocol) for control signals.

---

## 3. Network Layer Functions

**Question:** What are functions of the network layer?
**Correct Answer: A, C, and D**

### Why these are correct:

The Network Layer (Layer 3) is responsible for routing data between different networks:

* **A:** It provides **logical addresses** (such as IP addresses) so devices can be identified globally.
* **C & D:** Its core purpose is to **route and forward data packets** from the source host to the destination host across interconnected networks.

### Why B is incorrect:

* **B:** Setting up connections between **processes** is a function of the **Transport Layer** (Layer 4) using port numbers, not the Network Layer.

---

## 4. OSI Model Statements

**Question:** Which of the following statements are true about the layers in the OSI reference model?
**Correct Answer: A, B, C, and D (All of them)**

### Why these are all correct:

Each statement accurately describes the primary responsibility of that specific layer:

* **A (Application):** It is indeed the layer closest to the user (e.g., a web browser).
* **B (Session):** It acts as the "dialogue controller," managing the start and end of communications.
* **C (Network):** It defines IP addressing and path selection for routers.
* **D (Transport):** It handles the "how" of transmission, including connection-oriented (TCP) and connectionless (UDP) methods, and error recovery.

---

## 5. MAC Address Structure

**Question:** A MAC address is 48 bits (6 bytes) in length and consists of 12 hexadecimal digits.
**Correct Answer: Right**

### Why "Right" is correct:

A Media Access Control (MAC) address is the permanent physical address of a network interface card (NIC). It is expressed as 12 hex characters (0-9, A-F), such as `00:1A:2B:3C:4D:5E`. Since each hex digit represents 4 bits, 12 × 4 = 48 bits total (which equals 6 bytes).

---

## 6. ARP Reply Packets

**Question:** An ARP Reply packet is broadcast so that all hosts can receive it.
**Correct Answer: Wrong**

### Why "Wrong" is correct:

Address Resolution Protocol (ARP) works in two steps:

1. **ARP Request:** This **is** a broadcast ("Who has IP X.X.X.X?").
2. **ARP Reply:** This is a **Unicast** packet. Because the requester's MAC address was included in the original request, the replying device sends the answer directly to that specific host rather than bothering the entire network.

---

## 7. Data Link Layer Protocols

**Question:** Common data link layer protocols include Ethernet, PPPoE, and PPP.
**Correct Answer: Right**

### Why "Right" is correct:

The Data Link Layer (Layer 2) handles how data is framed for the physical wire:

* **Ethernet:** The standard for local area networks (LANs).
* **PPP (Point-to-Point Protocol):** Used for direct connections between two nodes.
* **PPPoE (PPP over Ethernet):** Commonly used by ISPs to connect users to the internet via DSL.

---
