

---

## 1. Traditional vs. Automated Management

**Question:** Which of the following is a disadvantage of traditional network management (manual CLI configuration)?
**Correct Answer: A. High risk of human error and low efficiency.**

### Why A is correct:

In traditional networking, administrators log into devices one by one to type commands. This process is:

* **Error-Prone:** A single typo in a critical command can take down an entire network segment.
* **Slow:** Scaling a configuration change across 100 routers manually takes hours or days.
* **Inconsistent:** Manual entry often leads to "configuration drift," where different devices end up with slightly different settings over time.

### Why the others are incorrect:

* **B & C:** These usually describe **Automation** or **SDN** advantages (centralized control and fast deployment).
* **D:** Traditional management actually has *lower* initial software costs compared to expensive automation platforms, though the labor cost is much higher.

---

## 2. Python in Networking

**Question:** Why is Python the most popular language for network automation?
**Correct Answer: A, B, and C**

### Why these are correct:

Python has become the industry standard for "NetDevOps" because:

* **A (Simplicity):** It has a clean, readable syntax that is easy for traditional network engineers (who may not be programmers) to learn.
* **B (Libraries):** It has powerful libraries specifically for networking, such as **Netmiko** (for CLI), **NAPALM**, and **PyEZ**.
* **C (Platform Support):** Almost all modern network operating systems (like Huawei VRP, Cisco IOS XE) support Python scripts or provide APIs that Python can easily interact with.

---

## 3. RESTful APIs

**Question:** What does a RESTful API use to communicate between a controller and a network device?
**Correct Answer: B. HTTP/HTTPS**

### Why B is correct:

REST (Representational State Transfer) is a set of rules for web-based communication. It uses standard web protocols—**HTTP** and **HTTPS**—to send and receive data. This allows network controllers to manage devices using common web methods like `GET` (to read config), `POST` (to create config), and `DELETE`.

---

## 4. JSON and XML Data Formats

**Question:** JSON and XML are commonly used to format data sent via APIs because they are machine-readable.
**Correct Answer: Right**

### Why "Right" is correct:

Computers struggle to parse the raw text output of a `display ip interface brief` command because the spacing might change. **JSON** and **XML** provide a structured, "tagged" format. This ensures that an automation script always knows exactly where to find the IP address or the interface status, regardless of the device model.

---

## 5. Intent-Based Networking (IBN)

**Question:** What is the core concept of Intent-Based Networking (IBN)?
**Correct Answer: A. The network automatically translates business goals into network configurations.**

### Why A is correct:

IBN is the next evolution of SDN. Instead of an engineer telling the network *how* to route traffic (CLI), the engineer tells the network *what* the goal is (e.g., "Ensure Video Conferencing has the highest priority"). The IBN controller then automatically calculates and pushes the necessary configurations to every device to achieve that goal.

---

## 6. SSH vs. Telnet for Management

**Question:** Why is SSH preferred over Telnet for managing network devices?
**Correct Answer: B. SSH encrypts the management session, whereas Telnet sends data in cleartext.**

### Why B is correct:

Security is paramount in management. If you use **Telnet**, anyone with a packet sniffer (like Wireshark) on the path can see your username and password. **SSH (Secure Shell)** creates an encrypted tunnel, ensuring that even if the packets are intercepted, the credentials and configuration data cannot be read.

---

