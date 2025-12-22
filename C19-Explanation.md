
---

### **Q1-C19**

**Question:** What is the length of an IPv6 address?
**A.** 64
**B.** 96
**C.** 256
**D.** 128
**Correct Answer: D**

**Explanation:**

An IPv6 address is **128 bits** long, which is four times the length of an IPv4 address (32 bits). This provides a massive address space—approximately 2¹²⁸ unique addresses—ensuring we will not run out of IP addresses in the foreseeable future.

---

### **Q2-C19**

**Question:** What is the abbreviated version of the IPv6 address `2001:0AF8:0000:1234:FB00:0000:5000:EF14`?
**A.** `2001:AF8:0000:1234:FB:0000:5000:EF14`
**B.** `2001:0AF8::1234:FB00::5000:EF14`
**C.** `2001:AF8:0:1234:FB00::5000:EF14`
**D.** `2001:0AF8:0000:1234:FB00:0000:5:EF14`
**Correct Answer: C**

**Explanation:**

IPv6 abbreviation follows two main rules:

1. **Omit Leading Zeros:** Within each 16-bit block, leading zeros can be removed. (e.g., `:0AF8:` becomes `:AF8:` and `:0000:` becomes `:0:`).
2. **Compress Continuous Zero Blocks (`::`):** A single sequence of consecutive all-zero blocks can be replaced with a double colon.
* *Note:* You can only use `::` **once** in an address to avoid ambiguity.
In Choice **C**, the third block `0000` is reduced to `0`, and the sixth block `0000` is replaced by `::` (representing the zero block).



---

### **Q3-C19**

**Question:** Which of the following fields is used in a basic IPv6 header but not in an IPv4 header?
**A.** Payload length
**B.** Hop limit
**C.** Next header
**D.** Flow label
**Correct Answer: D**

**Explanation:**

The **Flow Label** (20 bits) is a new field in the IPv6 header. It allows the source to label sequences of packets for which special handling is requested by IPv6 routers (such as real-time service or specific QoS).

* **Hop Limit** is the IPv6 equivalent of IPv4's **TTL**.
* **Next Header** is the IPv6 equivalent of IPv4's **Protocol** field.
* **Payload Length** is the IPv6 equivalent of IPv4's **Total Length** (though it measures only the data, not the header).

---

### **Q4-C19**

**Question:** Depending on the IPv6 address prefix, which of the following address types can IPv6 addresses be classified into? (Multiple Choice)
**A.** Multicast address
**B.** Broadcast address
**C.** Unicast address
**D.** Anycast address
**Correct Answer: ACD**

**Explanation:**

IPv6 uses three types of communication addresses:

* **Unicast:** One-to-one communication.
* **Multicast:** One-to-many communication.
* **Anycast:** One-to-nearest communication (delivered to the "closest" interface in a group).
**Important:** IPv6 **does not have broadcast addresses**. Its functions (like ARP) are replaced by specialized multicast groups.

---

### **Q5-C19**

**Question:** An IPv6 unicast address consists of a network prefix and an interface ID. Common IPv6 unicast addresses, such as global unicast addresses and link-local addresses, require the network prefix and interface ID to be 64 bits.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

By standard convention (and for features like SLAAC - Stateless Address Autoconfiguration to work), IPv6 addresses are split exactly in half:

* **Network Prefix (64 bits):** Identifies the specific network/subnet.
* **Interface ID (64 bits):** Identifies the specific interface on that network.
This **64/64 split** is the standard for Global Unicast (starts with `2000::/3`) and Link-Local (starts with `FE80::/10`) addresses.

---

