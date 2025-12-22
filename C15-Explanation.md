

---

## 1. SNMP Components and Architecture

**Question:** Which of the following is NOT a component of the SNMP (Simple Network Management Protocol) architecture?

**Correct Answer: D. SNMP Server** ### Why D is correct:
The standard SNMP architecture consists of three specific entities:

* **NMS (Network Management Station):** The "Manager" that runs management software to monitor and control devices.
* **Agent:** A software module running on the **Managed Device** (the router or switch) that communicates with the NMS.
* **MIB (Management Information Base):** A database/virtual information store on the agent that defines all the objects (like CPU usage or port status) that can be managed.
* **Note:** While "SNMP Server" is a term sometimes used loosely, it is not the formal name for a component in the standard architecture.

---

## 2. SNMP Operations (Get vs. Set vs. Trap)

**Question:** An administrator wants to receive an immediate notification from a switch when a port goes down. Which SNMP message type is used for this?

**Correct Answer: C. Trap**

### Why C is correct:

SNMP uses different message types depending on who starts the communication:

* **Get:** The **NMS** asks the agent for information (e.g., "What is your uptime?").
* **Set:** The **NMS** tells the agent to change a value (e.g., "Shut down interface G0/0/1").
* **Trap:** The **Agent** proactively sends an unsolicited message to the NMS when a significant event occurs (e.g., "Warning! Port 5 just failed"). This allows for real-time monitoring without constant polling.

---

## 3. Huawei iMaster NCE (The "Network Brain")

**Question:** What is the primary role of Huawei's **iMaster NCE** in a modern network?

**Correct Answer: A, B, and C**

### Why these are correct:

iMaster NCE is an intelligent management and control platform that integrates several key "engines":

* **A (Management & Control):** It provides centralized management, allowing for full-lifecycle automation of campus and data center networks.
* **B (Analysis Engine):** It uses **Telemetry** to collect network data in real-time, building a "digital twin" to visualize network health.
* **C (Intelligence Engine):** It leverages **AI and Big Data** to perform predictive maintenance, identifying 85% of potential faults before they affect users.

---

## 4. Network Design and Planning

**Question:** Which phase is considered the first step in constructing a campus network?

**Correct Answer: A. Network Design and Planning**

### Why A is correct:

Before any cables are plugged in or commands are typed, an engineer must perform **Planning**. This involves understanding business requirements, determining the number of users, choosing the right hardware (routers/switches/APs), and designing the IP addressing and VLAN structure. Skipping this leads to scalability and performance issues later.

---

## 5. SDN Forwarding vs. Control Separation

**Question:** Which statement is true regarding Software-Defined Networking (SDN)?

**Correct Answer: B. SDN separates the forwarding plane from the control plane.**

### Why B is correct:

Traditional routers make their own decisions. In SDN, the **Control Plane** (the "brain") is moved to a centralized controller (like iMaster NCE), while the **Forwarding Plane** (the physical switch) simply follows instructions to move packets. This centralized control makes the network more agile and easier to program.

---

## 6. CampusInsight and Fault Location

**Question:** How does iMaster NCE-CampusInsight improve O&M (Operations and Maintenance)?

**Correct Answer: D. By locating root causes of faults within minutes using AI.**

### Why D is correct:

Traditional troubleshooting is "complaint-driven" (waiting for a user to call). **CampusInsight** is proactive. It monitors the "journey" of every user and application. When a fault occurs, it automatically analyzes the data to pinpoint the root cause—such as a specific AP interference or a DHCP failure—reducing troubleshooting time from hours to minutes.

---

