
---

### **Q1-C9**

**Question:** The bridge IDs of SW1, SW2, SW3, and SW4 are 4096.4c1f-aabc-102a, 4096.4c1f-aabc-102b, 4096.4c1f-aabc-001a and 8192.4c1f-aabc-112b, respectively. If the four switches are on the same Layer 2 network and have STP enabled, which switch acts as the root bridge?
**A.** SW1
**B.** SW3
**C.** SW2
**D.** SW4
**Correct Answer: B**

**Explanation:**
The **Root Bridge** is elected based on the **lowest Bridge ID (BID)**. The BID consists of two parts: **Priority** and **MAC Address**.

1. **Compare Priorities:** SW1, SW2, and SW3 all have a priority of **4096**. SW4 has **8192**, so it is immediately eliminated.
2. **Compare MAC Addresses:** Since the priorities tie, we look at the MAC addresses:
* SW1: `4c1f-aabc-102a`
* SW2: `4c1f-aabc-102b`
* SW3: **`4c1f-aabc-001a`**


3. SW3 has the lowest MAC address (001a is smaller than 102a/102b). Therefore, **SW3** is elected as the Root Bridge.

---

### **Q2-C9**

**Question:** What is the default Forward Delay value in STP?
**A.** 30s
**B.** 15s
**C.** 20s
**D.** 2s
**Correct Answer: B**

**Explanation:**
STP uses specific timers to ensure the network is loop-free before forwarding data:

* **Hello Time:** 2 seconds (interval between BPDUs).
* **Max Age:** 20 seconds (how long a switch waits before declaring a neighbor down).
* **Forward Delay:** **15 seconds**.
* *Note:* A port spends 15s in the **Listening** state and 15s in the **Learning** state, totaling 30 seconds of "Forward Delay" before reaching the Forwarding state.

---

### **Q3-C9**

**Question:** The root ID, bridge ID, interface ID, and root path cost (RPC) are the main fields used to determine priorities of configuration BPDUs. To select a superior configuration BPDU, in which of the following sequences does a switch compare these fields?
**A.** Interface ID, root ID, bridge ID, and RPC
**B.** RPC, root ID, bridge ID, and interface ID
**C.** Root ID, bridge ID, interface ID, and RPC
**D.** Root ID, RPC, bridge ID, and interface ID
**Correct Answer: D**

**Explanation:**
When a switch receives a BPDU, it uses the **"Best BPDU Algorithm"** (also called the 4-step decision process). It compares fields in this strict order until a tie is broken:

1. **Root ID:** Lowest Root BID wins.
2. **RPC:** Lowest Root Path Cost (shortest path to the root) wins.
3. **Bridge ID:** Lowest Sender BID (if costs are equal) wins.
4. **Interface ID:** Lowest Sender Port ID (if everything else ties) wins.

---

### **Q4-C9**

**Question:** Which of the following fields are contained in a configuration BPDU? (Multiple Choice)
**A.** Forward Delay
**B.** Port ID
**C.** Root ID
**D.** Bridge ID
**Correct Answer: ABCD**

**Explanation:**
A **Configuration BPDU** is the heartbeat of STP. It contains all the necessary parameters to elect the root and calculate the topology:

* **Root ID:** ID of the current Root Bridge.
* **Bridge ID:** ID of the switch sending the BPDU.
* **Port ID:** ID of the port sending the BPDU.
* **RPC:** Cost to reach the Root.
* **Timers:** Hello Time, Max Age, and **Forward Delay**.

---

### **Q5-C9**

**Question:** By default, a switch runs RSTP.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**
On many Huawei switches (VRP), the default Spanning Tree mode is actually **MSTP (Multiple Spanning Tree Protocol)**. While MSTP is compatible with RSTP, it is a different mode. Therefore, the statement that it runs RSTP "by default" is incorrect. You must use the command `stp mode rstp` to specifically enable RSTP.

---

