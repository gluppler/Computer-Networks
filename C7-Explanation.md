Q1-C7
Question: What type of MAC address is 01-00-5e-00-00-01? A. Unicast MAC address B. Multicast MAC address C. Broadcast MAC address D. Anycast MAC address Correct Answer: B

Explanation: MAC addresses are categorized by their first octet:

Unicast: The least significant bit of the first octet is 0.

Multicast: The least significant bit of the first octet is 1. Specifically, IPv4 multicast MAC addresses always start with the prefix 01-00-5e.

Broadcast: All bits are 1 (FF-FF-FF-FF-FF-FF).

The address 01-00-5e-00-00-01 is the standard multicast MAC used for "All Systems on this Subnet" (mapping to IP 224.0.0.1).

Q2-C7
Question: Which of the following actions does a switch take by default after it receives an unknown unicast frame? A. Learns the mapping... and discards this data frame. B. Learns the mapping between the source MAC address and interface that receives this data frame, and floods this data frame. C. Learns the mapping... and forwards this data frame based on the MAC address table. D. Does not learn... Correct Answer: B

Explanation: A switch performs three main operations when a frame arrives:

Learning: It records the Source MAC and the incoming port in its MAC Address Table.

Lookup: It looks for the Destination MAC in its table.

Forwarding/Flooding: Since the Destination MAC is "Unknown" (not in the table), the switch must flood the frame out of all ports except the one it arrived on to ensure it reaches the destination.

Q3-C7
Question: Which of the following ARP packets is used to request the MAC address corresponding to an IP address? A. ARP Request B. ARP Reply C. RARP Request D. RARP Reply Correct Answer: A

Explanation: As covered in earlier chapters, the ARP Request is the "question" sent by a host asking for a MAC address.

ARP Request: "I have IP X, who has IP Y? Send me your MAC." (Broadcast)

ARP Reply: "I am IP Y, here is my MAC." (Unicast)

RARP: Reverse ARP is used to find an IP if you only have a MAC (mostly obsolete).

Q4-C7
Question: Which of the following fields are contained in an Ethernet frame in the IEEE 802.3 format? (Multiple Choice) A. Length B. Destination MAC C. Source MAC D. FCS Correct Answer: ABCD

Explanation: The IEEE 802.3 frame structure includes:

Destination MAC (6 bytes): Where the frame is going.

Source MAC (6 bytes): Where the frame came from.

Length (2 bytes): In 802.3, this field indicates the length of the data (In Ethernet II, this is the "Type" field).

Data/Payload: The encapsulated packet.

FCS (Frame Check Sequence): A 4-byte CRC used to detect errors during transmission.

Q5-C7
Question: A switch floods unknown unicast frames and frames whose destination MAC address is a broadcast MAC address. A. Right B. Wrong Correct Answer: Right

Explanation: This is a fundamental rule of switch behavior called BUM traffic handling (Broadcast, Unknown Unicast, and Multicast).

Broadcast: Must go to everyone.

Unknown Unicast: The switch doesn't know where the destination is, so it must flood it to find it.

Multicast: By default (without IGMP Snooping), a switch treats multicast like a broadcast and floods it.
