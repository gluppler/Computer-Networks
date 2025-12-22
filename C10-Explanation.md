
---

## 1. PPP Authentication Protocols

**Question:** Which of the following authentication protocols are supported by PPP?
**Correct Answer: A and B. PAP and CHAP**

### Why A and B are correct:

PPP is a data link layer protocol used for direct connections between two nodes. It offers two main methods of security:

* **A (PAP - Password Authentication Protocol):** A simple, two-way handshake where the password is sent in **cleartext**. It is less secure but consumes fewer resources.
* **B (CHAP - Challenge Handshake Authentication Protocol):** A more secure, three-way handshake that uses a **hashed** value (MD5) so the password is never actually sent over the link.

### Why the others are incorrect:

* **C (MD5):** MD5 is a hashing algorithm used *within* CHAP, but it is not a standalone PPP authentication protocol.
* **D (WEP):** This is a legacy wireless security protocol (Layer 2 for WLAN), not used for serial point-to-point links.

---

## 2. WLAN Frequency Bands

**Question:** Which frequency bands are commonly used by IEEE 802.11 wireless networks?
**Correct Answer: A and C. 2.4 GHz and 5 GHz**

### Why A and C are correct:

Most standard Wi-Fi deployments operate on these two unlicensed bands:

* **2.4 GHz:** Known for better range and penetration through walls, but it is crowded and prone to interference (from microwaves, Bluetooth, etc.).
* **5 GHz:** Offers higher speeds and more non-overlapping channels but has a shorter range and is easily blocked by physical obstacles.

---

## 3. WLAN Deployment Modes

**Question:** In an enterprise WLAN, what is the role of an AC (Access Controller)?
**Correct Answer: A, B, and C**

### Why these are correct:

In "Fit AP" architectures (common in offices and campuses), the AC acts as the "brain":

* **A (Management):** It centrally manages all Access Points (APs), including firmware updates and configuration.
* **B (Channel & Power):** It automatically adjusts the radio channels and power levels of APs to reduce interference.
* **C (Security):** It handles user authentication and enforces security policies across the entire wireless network.

---

## 4. SSID Definition

**Question:** An SSID (Service Set Identifier) is used to identify a specific wireless network.
**Correct Answer: Right**

### Why "Right" is correct:

The SSID is essentially the "name" of the Wi-Fi network that users see when they try to connect. It allows multiple wireless networks to exist in the same physical space while keeping their traffic and access requirements separate.

---

## 5. CSMA/CA in Wireless

**Question:** Wireless networks use CSMA/CD to detect collisions on the medium.
**Correct Answer: Wrong**

### Why "Wrong" is correct:

* **CSMA/CD (Collision Detection):** Used in **wired** Ethernet.
* **CSMA/CA (Collision Avoidance):** Used in **wireless** networks.
Because wireless radios cannot listen and transmit on the same frequency at the same time, they cannot "detect" a collision while it is happening. Instead, they use "Avoidance"—listening to see if the air is clear and then sending a "Request to Send" (RTS) to avoid the crash entirely.

---

## 6. PPP Link Establishment

**Question:** What is the correct order of the PPP link establishment phases?
**Correct Answer: A. Dead, Establish, Authenticate, Network, Terminate**

### Why A is correct:

A PPP session follows a strict lifecycle:

1. **Dead:** The physical link is inactive.
2. **Establish:** LCP (Link Control Protocol) negotiates basic link parameters.
3. **Authenticate:** (Optional) PAP or CHAP verifies the identity of the peer.
4. **Network:** NCP (Network Control Protocol) configures higher-layer protocols like IPv4 or IPv6.
5. **Terminate:** The link is closed.

---

