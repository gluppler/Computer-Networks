
---

### **Q1-C11**

**Question:** What is the default LACP interface priority?
**A.** 4096
**B.** 0
**C.** 32768
**D.** 8192
**Correct Answer: C**

**Explanation:**

In Huawei VRP, both the **LACP System Priority** and **LACP Interface Priority** use a default value of **32768**.

* The system uses this priority to elect the **Actor** (the "boss" device that makes the decisions).
* If priorities are identical, the device with the lower MAC address becomes the Actor.
* Interface priority is used to determine which physical links become "Active" and which stay as "Backup" (M:N mode).

---

### **Q2-C11**

**Question:** Which of the following configurations can be different on member interfaces in an Eth-Trunk interface?
**A.** Spanning tree configurations
**B.** Interface rate
**C.** Duplex mode
**D.** VLAN configurations
**Correct Answer: A**

**Explanation:**

To form a stable Eth-Trunk, member interfaces must be consistent in their physical and basic Layer 2 attributes.

* **Must be the same:** Interface rate (B), Duplex mode (C), and VLAN configurations (D). If these differ, the interface will likely be placed in an "Unselected" or error state.
* **Can be different:** Spanning tree configurations (A). While not recommended for most designs, the STP costs or priorities on individual physical ports do not inherently prevent them from joining an Eth-Trunk, though the Eth-Trunk itself will typically be seen as a single "logical" port by STP once bundled.

---

### **Q3-C11**

**Question:** Which of the following statements is false about selecting active links in LACP mode?
**A.** Devices on both ends exchange LACPDUs to select the Actor.
**B.** The Actor selects active interfaces based on the LACP interface priority and interface number.
**C.** The Actor enables active interfaces and disables backup interfaces, and notifies the device on the other end of the selected active interfaces based on the physical interface status.
**D.** The Partner determines its active interfaces based on the active interfaces selected on the Actor.
**Correct Answer: C**

**Explanation:**

Statement C is **false** because of the specific wording regarding "physical interface status."
In LACP negotiation:

1. Devices exchange LACPDUs to elect the **Actor**.
2. The **Actor** chooses active interfaces based on its own **Interface Priority** (lower is better) and then **Interface ID** (if priorities tie).
3. The **Partner** must follow the Actor's choice.
The selection is based on **LACP configuration/priority logic**, not solely or automatically based on "physical interface status" notification in the manner C describes.

---

### **Q4-C11**

**Question:** Which of the following fields in an LACPDU is used to select the Actor? (Multiple Choice)
**A.** Interface number
**B.** Device MAC address
**C.** Device priority
**D.** Interface priority
**Correct Answer: BC**

**Explanation:**

The **Actor** is the device that controls which links in the bundle are active. To decide which device is the Actor, LACP compares the **System ID**, which consists of:

1. **LACP System Priority (C):** The primary value compared. Lower is better.
2. **Device MAC Address (B):** Used as a tie-breaker if the priorities are equal.
Interface-specific values (A and D) are used later to select active links, but they do not determine which *device* is the Actor.

---

### **Q5-C11**

**Question:** Configuring the lower threshold for the number of active interfaces in an Eth-Trunk ensures that the Eth-Trunk has the minimum required bandwidth.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

The `least active-linknumber` command sets a minimum requirement. If the number of "Up" physical links falls below this threshold, the entire Eth-Trunk interface goes "Down."
This prevents a situation where an Eth-Trunk is technically "Up" but only has 1 functioning link, which might not be enough to handle the traffic load, leading to massive congestion. It's a safety mechanism to ensure quality of service.

---

