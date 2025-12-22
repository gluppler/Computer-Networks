

---

### **Q1-C3**

**Question:** Which of the following statements about command functions is false?
**A.** `<Huawei>undo` //Deletes a file.
**B.** `<Huawei>pwd` //Displays the current directory.
**C.** `<Huawei>dir` //Displays information about files in the current directory.
**D.** `<Huawei>more` //Displays the content of a text file.
**Correct Answer: A**

**Explanation:**
The `undo` command is one of the most used commands in Huawei VRP, but its function is to **reverse or cancel a configuration command** (like "no" in Cisco), not to delete files.

* To delete a file in VRP, you use the `delete` command.
* `pwd`, `dir`, and `more` are standard file system commands similar to those found in Linux/Unix.

---

### **Q2-C3**

**Question:** Which of the following are types of storage device?
**A.** SDRAM
**B.** Flash
**C.** NVRAM
**D.** SD card
**E.** USB flash drive
**Correct Answer: ABCDE**

**Explanation:**
Huawei network devices utilize various memory types for different roles:

* **SDRAM:** Running memory (RAM); loses data when powered off.
* **Flash:** Stores the system software (the OS image) and configuration files.
* **NVRAM:** Non-volatile memory often used to store small amounts of persistent data.
* **SD/USB:** External storage used for easy software upgrades or log exports.

---

### **Q3-C3**

**Question:** Which of the following functions are provided by the VRP? (Multiple Choice)
**A.** Provides a unified user interface and a unified management interface.
**B.** Implements functions of the control plane and defines interface standards of the forwarding plane.
**C.** Implements communication between the device forwarding plane and VRP control plane.
**D.** Eliminates the differences between the link layer and network layer of each product.
**Correct Answer: ABCD**

**Explanation:**
VRP is the "brain" of the device. It creates a **consistent user experience** across different hardware (switches, routers, firewalls).

* It manages the **Control Plane** (deciding where traffic should go, like building a routing table).
* It communicates with the **Forwarding Plane** (the hardware specialized for moving packets at high speed).
* By providing a unified software layer, it hides the hardware differences, allowing a network admin to use the same commands on an AR router as they would on an S-series switch.

---

### **Q4-C3**

**Question:** There are two commonly used device management modes: CLI and web system.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**
Network administrators typically manage devices in two ways:

1. **CLI (Command Line Interface):** Preferred by experts for speed and advanced configuration (via Console, Telnet, or SSH).
2. **Web System (GUI):** A user-friendly, browser-based interface often used for basic monitoring or simplified configuration.

---

