

---

## 1. Python Execution Modes

**Question:** In which of the following modes can Python be executed?

**Correct Answer: C. Both interactive and script (non-interactive) mode.**

### Why C is correct:

Python offers flexibility in how code is run:

* **Interactive Mode:** Allows you to type commands one by one in the Python shell (`>>>`) and see immediate results. This is great for testing small snippets of code.
* **Script Mode:** You write a complete block of code in a `.py` file and execute it all at once. This is the standard method for running complex automation tasks.

---

## 2. Python Data Containers

**Question:** Which Python data type is an unordered collection of unique elements?

**Correct Answer: B. Set**

### Why B is correct:

Understanding data structures is vital for handling network data (like a list of IP addresses):

* **Set:** An unordered collection where every item is **unique** (no duplicates).
* **List:** An **ordered** collection that allows duplicates (e.g., `[1, 2, 2, 3]`).
* **Dictionary:** Stores data in **Key-Value pairs** (e.g., `{'interface': 'G0/0/1'}`).
* **Tuple:** An ordered collection that **cannot be changed** (immutable) once created.

---

## 3. Netmiko and Paramiko

**Question:** Why do network engineers use the `Netmiko` library in Python?

**Correct Answer: A. To simplify SSH connections and command execution on multi-vendor devices.**

### Why A is correct:

While `Paramiko` handles the low-level SSH "tunneling," **Netmiko** is built specifically for networking. It includes "drivers" for different vendors (Huawei, Cisco, Juniper). It automatically handles tasks like entering "System-view," waiting for command prompts, and cleaning up the output so it's ready for the engineer to read.

---

## 4. NFV vs. SDN

**Question:** What is the primary focus of NFV (Network Functions Virtualization)?

**Correct Answer: B. Decoupling network functions from dedicated hardware.**

### Why B is correct:

* **NFV** is about **moving hardware to software**. Instead of buying a physical firewall, you run a virtual firewall (VNF) on a generic x86 server.
* **SDN** is about **centralizing control**. It separates the Control Plane from the Forwarding Plane to manage the network through a single controller.

---

## 5. Automation Advantages

**Question:** Which of the following is NOT a benefit of network automation?

**Correct Answer: D. Increased equipment hardware costs.**

### Why D is correct:

Automation actually aims to **reduce** costs.

* **A (Efficiency):** Tasks that took hours now take seconds.
* **B (Accuracy):** Eliminates "fat-finger" typos made by humans.
* **C (Agility):** The network can respond instantly to business needs, such as spinning up new bandwidth for a video conference.
* **D (Incorrect):** Automation focuses on software and logic; it doesn't inherently increase the cost of the routers or switches themselves.

---

## 6. YAML and Data Serialization

**Question:** Why is YAML often used in network automation tools like Ansible?

**Correct Answer: A. It is highly human-readable and easy to write.**

### Why A is correct:

YAML (Yet Another Markup Language) is often preferred over XML or JSON for configuration files because it uses **indentation** rather than complex brackets or tags. This makes it very easy for network engineers to read and edit without being professional software developers.

---

