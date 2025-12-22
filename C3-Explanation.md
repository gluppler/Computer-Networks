---

## 1. False Command Functions

**Question:** Which of the following statements about command functions is false?

**Correct Answer: A. <Huawei>undo //Deletes a file.**

### Why A is correct (False Statement):

The `undo` command is used to restore default settings, disable a function, or delete a specific configuration line. It is **not** used for file system management. To delete a file on a Huawei device, the command used is typically `delete`.

### Why the others are true:

* **B:** The `pwd` (Print Working Directory) command correctly displays the path of the directory you are currently in.
* **C:** The `dir` command is standard for listing files and subdirectories within the current directory.
* **D:** The `more` command is used to read the contents of a text file (like a configuration file) directly in the terminal.

---

## 2. Storage Device Types

**Question:** Which of the following are types of storage device?

**Correct Answer: A, B, C, D, E (All of them)**

### Why these are all correct:

Network devices utilize various types of memory and storage to function:

* **A (SDRAM):** Synchronous Dynamic Random Access Memory, used as the main system memory for running processes.
* **B (Flash):** Used to store the system software (VRP image) and configuration files.
* **C (NVRAM):** Non-Volatile RAM, used to store critical data that must survive a reboot, such as the startup configuration.
* **D & E (SD card / USB):** Removable storage media used for easy file transfers, software upgrades, or log exports.

---

## 3. VRP Functions

**Question:** Which of the following functions are provided by the VRP?

**Correct Answer: A, B, C, D (All of them)**

### Why these are all correct:

The Versatile Routing Platform (VRP) is the network operating system for Huawei devices. Its functions include:

* **A:** Providing a consistent User Interface (CLI) and management experience across different hardware.
* **B:** Managing the **Control Plane** (routing logic) and standardizing how data is handled by the **Forwarding Plane** (actual data movement).
* **C:** Ensuring seamless communication between the hardware's forwarding engine and the software's control logic.
* **D:** Abstracting the underlying hardware so that different products can use the same link layer and network layer features.

---

## 4. Device Management Modes

**Question:** There are two commonly used device management modes: CLI and web system.

**Correct Answer: Right**

### Why "Right" is correct:

Most modern network devices offer these two primary interfaces:

1. **CLI (Command Line Interface):** Preferred by experts for fast, detailed, and scriptable configuration via Console, Telnet, or SSH.
2. **Web System (GUI):** A browser-based interface that is more intuitive for beginners or for performing visual monitoring and basic tasks.

---

