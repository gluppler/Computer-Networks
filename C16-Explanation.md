

---

## 1. DHCP Working Principle

**Question:** Which of the following is the correct order of messages exchanged between a DHCP client and a DHCP server when a client requests an IP address for the first time?

**Correct Answer: A. Discover, Offer, Request, ACK**

### Why A is correct:

The DHCP process (often called **DORA**) follows a specific four-step handshake:

1. **Discover:** The client broadcasts a message to find available DHCP servers.
2. **Offer:** The server responds with a proposed IP address and configuration.
3. **Request:** The client selects an offer and asks the server to "reserve" that IP.
4. **ACK (Acknowledgment):** The server confirms the lease and provides the final configuration details.

---

## 2. DHCP Relay Agent

**Question:** Why is a DHCP Relay Agent required in some network environments?

**Correct Answer: B. To allow DHCP clients to obtain IP addresses from a server located in a different broadcast domain.**

### Why B is correct:

DHCP "Discover" messages are Layer 2 broadcasts, which routers do not forward. If the DHCP server is not on the same local network as the client, the router acting as the **Relay Agent** intercepts the broadcast and forwards it as a **Unicast** message to the remote server.

---

## 3. DNS (Domain Name System)

**Question:** What is the primary function of a DNS server?

**Correct Answer: A. Mapping domain names to IP addresses.**

### Why A is correct:

Computers communicate using IP addresses, but humans prefer names. DNS acts as the "phonebook" of the internet, translating a human-readable name like `www.huawei.com` into its corresponding machine-readable IP address.

### Why the others are incorrect:

* **B:** Mapping MAC addresses to IPs is the job of **ARP**.
* **C:** Encrypting traffic is the job of protocols like **SSL/TLS**.

---

## 4. HTTP and HTTPS Port Numbers

**Question:** Which port numbers are used by default for HTTP and HTTPS, respectively?

**Correct Answer: C. 80 and 443**

### Why C is correct:

* **Port 80:** The standard port for **HTTP** (unencrypted web traffic).
* **Port 443:** The standard port for **HTTPS** (encrypted web traffic), which uses SSL/TLS for security.

---

## 5. FTP Transfer Modes

**Question:** Which FTP mode is more "firewall-friendly" because the client initiates the data connection?

**Correct Answer: B. Passive Mode (PASV)**

### Why B is correct:

* In **Active Mode**, the server tries to connect *back* to the client, which firewalls usually block.
* In **Passive Mode**, the client initiates both the control and data connections, making it much easier for traffic to pass through security filters.

---

## 6. DHCP Address Leasing (True/False)

**Question:** A DHCP client will attempt to renew its IP address lease when 50% of the lease time has expired.

**Correct Answer: Right**

### Why "Right" is correct:

By default, the renewal process (DHCP Request) starts at the **T1 timer** (50% of the lease duration). If the server doesn't respond, the client tries again at the **T2 timer** (87.5% of the lease duration) before finally giving up the IP when the lease hits 100%.

---

