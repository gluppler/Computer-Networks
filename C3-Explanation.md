---
### **Q1-C3**

**Question:** Which of the following statements about command functions is false?
**A.** `<Huawei>undo //Deletes a file.`
**B.** `<Huawei>pwd //Displays the path of the current directory.`
**C.** `<Huawei>dir //Lists files and subdirectories.`
**D.** `<Huawei>more //Reads the contents of a text file.`
**Correct Answer: A**

**Explanation:**

The `undo` command is used to restore default settings, disable a function, or delete a specific configuration line. It is **not** used for file system management. To delete a file on a Huawei device, the command used is typically `delete`.

**Why the others are true:**

* **B:** The `pwd` (Print Working Directory) command correctly displays the path of the directory you are currently in.
* **C:** The `dir` command is standard for listing files and subdirectories within the current directory.
* **D:** The `more` command is used to read the contents of a text file (like a configuration file) directly in the terminal.

---

### **Q2-C3**

**Question:** Which of the following are types of storage device?
**A.** SDRAM
**B.** Flash
**C.** NVRAM
**D.** SD card
**E.** USB
**Correct Answer: A, B, C, D, E (All of them)**

**Explanation:**

Network devices utilize various types of memory and storage to function:

* **A (SDRAM):** Synchronous Dynamic Random Access Memory, used as the main system memory for running processes.
* **B (Flash):** Used to store the system software (VRP image) and configuration files.
* **C (NVRAM):** Non-Volatile RAM, used to store critical data that must survive a reboot, such as the startup configuration.
* **D and E (SD card / USB):** Removable storage media used for easy file transfers, software upgrades, or log exports.

---

### **Q3-C3**

**Question:** Which of the following functions are provided by the VRP?
**A.** Providing a consistent user interface
**B.** Managing the control plane and forwarding plane
**C.** Ensuring communication between hardware and software
**D.** Abstracting the underlying hardware
**Correct Answer: A, B, C, D (All of them)**

**Explanation:**

The Versatile Routing Platform (VRP) is the network operating system for Huawei devices. Its functions include:

* **A:** Providing a consistent User Interface (CLI) and management experience across different hardware.
* **B:** Managing the **Control Plane** (routing logic) and standardizing how data is handled by the **Forwarding Plane** (actual data movement).
* **C:** Ensuring seamless communication between the hardware's forwarding engine and the software's control logic.
* **D:** Abstracting the underlying hardware so that different products can use the same link layer and network layer features.

---

### **Q4-C3**

**Question:** There are two commonly used device management modes: CLI and web system.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

Most modern network devices offer these two primary interfaces:

1. **CLI (Command Line Interface):** Preferred by experts for fast, detailed, and scriptable configuration via Console, Telnet, or SSH.
2. **Web System (GUI):** A browser-based interface that is more intuitive for beginners or for performing visual monitoring and basic tasks.

---
