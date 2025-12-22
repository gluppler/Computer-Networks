
---

### **Q1-C16**

**Question:** Which of the following 802.11 protocols works only on the 5 GHz frequency band?
**A.** 802.11ax
**B.** 802.11n
**C.** 802.11ac
**D.** 802.11g
**Correct Answer: C**

**Explanation:**

The IEEE 802.11 standards operate on different frequency bands:

* **802.11g:** Operates only on **2.4 GHz**.
* **802.11n (Wi-Fi 4):** Operates on both **2.4 GHz** and **5 GHz**.
* **802.11ac (Wi-Fi 5):** Operates strictly on the **5 GHz** band to avoid interference and provide higher throughput.
* **802.11ax (Wi-Fi 6):** Operates on both **2.4 GHz** and **5 GHz** (and 6 GHz for Wi-Fi 6E).

---

### **Q2-C16**

**Question:** Which of CAPWAP message types is used by an AC to deliver configuration files to APs?
**A.** Configuration Update Request
**B.** Image Data Request
**C.** Configuration Update Response
**D.** Image Data Response
**Correct Answer: C**

**Explanation:**

CAPWAP (Control and Provisioning of Wireless Access Points) protocol manages APs.

* **Configuration Update Request:** Sent by an **AP** to the AC to request or report configuration status.
* **Configuration Update Response:** Sent by the **AC** to the AP. This message carries the actual configuration parameters or files the AP needs to operate.
* **Image Data:** Used for upgrading the AP's firmware (software image).

---

### **Q3-C16**

**Question:** Which of the following data frames is used by an AP to periodically broadcast its SSID?
**A.** Probe Request
**B.** Probe Response
**C.** Association Request
**D.** Beacon
**Correct Answer: D**

**Explanation:**

WLAN management frames handle the "announcement" and "joining" of networks:

* **Beacon Frame:** The AP sends this periodically (default every 100ms) to announce its presence, SSID, and supported rates.
* **Probe Request:** Sent by a **Client** to search for a specific SSID.
* **Probe Response:** Sent by an AP in response to a Probe Request.
* **Association Request:** Sent by a client to join the AP after authentication.

---

### **Q4-C16**

**Question:** Which of the following modes are used by APs to dynamically discover an AC? (Multiple Choice)
**A.** Manually specifying the AC IP address on the APs
**B.** Broadcast mode
**C.** DHCP mode
**D.** DNS mode
**Correct Answer: BCD**

**Explanation:**

APs need to find their controller (AC) to establish a CAPWAP tunnel. **Dynamic** methods include:

* **Broadcast (B):** The AP sends a Discovery Request to the local subnet broadcast address.
* **DHCP (C):** The DHCP server provides the AC's IP address to the AP using **Option 43**.
* **DNS (D):** The AP queries a specific domain name (like `ac-address.local`) to get the AC's IP.
* *Note: Manual configuration (A) is a static method, not a dynamic discovery method.*

---

### **Q5-C16**

**Question:** Two CAPWAP tunnels are established: data tunnel and control tunnel. They are both kept alive using Keepalive messages.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**

While it is true that CAPWAP establishes two tunnels, they use different "heartbeat" mechanisms:

1. **Control Tunnel:** Uses **Echo** messages (Echo Request/Response) to maintain the link.
2. **Data Tunnel:** Uses **Keepalive** messages.
Because the statement suggests *both* use Keepalive messages, it is technically incorrect according to the protocol specifications.

---

