
---

## 1. Configurable Host Addresses

**Question:** Which of the following IP addresses can be manually configured on a host interface?
**Correct Answer: A and C**

### Why A and C are correct:

A host interface can be configured with standard **Unicast** addresses that belong to Class A, B, or C.

* **A (192.168.1.1):** This is a standard Private Class C address. It is perfectly valid for local network host configuration.
* **C (10.0.0.1):** This is a standard Private Class A address. It is commonly used in large enterprise local networks.

### Why the others are incorrect:

* **B (127.0.0.1):** This is the **Loopback address**. It is reserved by the system to refer to "localhost" and cannot be manually assigned as the primary IP of a physical network interface.
* **D (224.0.0.18):** This is a **Multicast address** (specifically used for VRRP). Multicast addresses (224.0.0.0 to 239.255.255.255) are used for group communication and cannot be assigned as a host's unique interface address.

---

## 2. Private IP Address Ranges

**Question:** Which of the following is a private IP address?
**Correct Answer: A, B, and D**

### Why these are correct:

RFC 1918 defines three specific blocks of IPv4 addresses for private use:

* **A (10.0.0.0 – 10.255.255.255):** The Class A private range.
* **B (172.16.0.0 – 172.31.255.255):** The Class B private range.
* **D (192.168.0.0 – 192.168.255.255):** The Class C private range.

### Why C is incorrect:

* **C (192.172.0.0):** This address falls outside of the 192.168.x.x range. It is a **Public** IP address and cannot be used for private internal networking without potentially causing conflicts on the internet.

---

## 3. Subnet Host Calculation (/30)

**Question:** How many usable host IP addresses are there in a subnet with the mask 255.255.255.252?
**Correct Answer: B. 2**

### Why B is correct:

The mask 255.255.255.252 (or /30 in CIDR) leaves only **2 bits** for the host portion of the address.

* **Total addresses:** .
* **Usable addresses:** To find usable hosts, you must subtract **2** (one for the Network ID and one for the Broadcast address).
* **Calculation:** .
This subnet is commonly used for point-to-point links between two routers where only two IPs are needed.

---

## 4. ICMP Echo Packets

**Question:** The `ping` command uses ICMP Echo Request and Echo Reply packets to test the reachability of a destination host.
**Correct Answer: Right**

### Why "Right" is correct:

The `ping` utility is the most common diagnostic tool for network connectivity. It works by sending an **ICMP Echo Request** (Type 8) to a target. If the target is active and reachable, it responds with an **ICMP Echo Reply** (Type 0). Successful completion of this exchange confirms basic Layer 3 connectivity.

---

## 5. TTL and Packet Discarding

**Question:** When a router receives an IP packet with a TTL (Time to Live) value of 1, it will discard the packet and send an ICMP "Time Exceeded" message to the source.
**Correct Answer: Right**

### Why "Right" is correct:

The TTL field is a safety mechanism to prevent packets from looping infinitely.

1. Every time a packet passes through a router, the router **decrements** the TTL by 1.
2. If a router receives a packet with **TTL = 1**, it decrements it to **0**.
3. Since a packet cannot be forwarded with a TTL of 0, the router **discards** it and notifies the sender using an ICMP "Time Exceeded" error message.

---

