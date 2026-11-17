<img width="686" height="386" alt="image" src="https://github.com/user-attachments/assets/da9fab5e-c9d3-4045-94c8-0ccf6f00f834" />

# Wireshark Network Analysis & Traffic Triage Lab

## Project Overview
This project focuses on capturing and analyzing live network traffic to inspect core protocols, troubleshoot connectivity, and identify potentially suspicious network activity. Utilizing **Wireshark**, this lab covers foundational packet analysis skills necessary for network security monitoring and initial incident response triage.

---

## Tools Used
* **Wireshark** - Open-source packet analyzer for deep packet inspection and network protocol analysis.
* **Network Protocols Evaluated** - TCP, UDP, DNS, HTTP, HTTPS, ICMP, ARP.

---

## Step-by-Step Lab Execution

### Step 1: Live Traffic Capture & Interface Selection
* Selected the active network interface card (NIC) to initiate real-time packet capturing.
* Monitored initial traffic flows to establish a network baseline.
<img width="990" height="661" alt="image" src="https://github.com/user-attachments/assets/59ae2de8-b864-4d43-ad9f-b7fb09108ea0" />

### Step 2: Protocol Deep-Dive (TCP, DNS, HTTP/S)
* Inspected **DNS** query/response payloads to verify domain resolution behavior.
* Analyzed the **TCP 3-Way Handshake** (SYN, SYN-ACK, ACK) to evaluate connection states.
* Examined **HTTP/HTTPS** headers to understand web traffic structures and encryption limitations.
<img width="991" height="717" alt="image" src="https://github.com/user-attachments/assets/97e65257-1fa5-4e52-8e37-bc1d0c3986c8" />
<img width="999" height="710" alt="image" src="https://github.com/user-attachments/assets/3df59181-f8eb-4c43-9e77-49c1eac94a55" />
<img width="994" height="713" alt="image" src="https://github.com/user-attachments/assets/411efe69-ca12-4f9c-91fe-71ce6dc70114" />

### Step 3: Targeted Packet Filtering
* Utilized Wireshark display filters (e.g., `ip.addr == X.X.X.X`, `tcp.port == 80`, `dns.flags.response == 1`) to cut through network noise and isolate specific target streams.
<img width="992" height="711" alt="image" src="https://github.com/user-attachments/assets/f6ee2411-abbc-4576-bfa8-9cae74b3f011" />

### Step 4: Follow TCP Stream & Payload Inspection
* Used the "Follow TCP Stream" feature to reconstruct fragmented data packets into readable, chronological data exchanges.
<img width="1658" height="713" alt="image" src="https://github.com/user-attachments/assets/f3754f7d-89f4-4d77-9a61-ab4068597af7" />

### Step 5: Network Triage & Troubleshooting
* Identified network anomalies such as TCP retransmissions, duplicate ACKs, or suspicious ICMP ping sweeps to troubleshoot latency issues and flag scanning behaviors.
<img width="1612" height="715" alt="image" src="https://github.com/user-attachments/assets/af57d8e7-5b54-4924-8cd8-e252d590c099" />

---

## Skills Learned
* **Deep Packet Inspection (DPI):** Understanding data structures down to the raw hex/byte level.
* **Traffic Isolation:** Building complex display filters to rapidly parse through thousands of live packets.
* **Network Troubleshooting:** Diagnosing common protocol failures, dropouts, and handshake errors.
* **Security Monitoring:** Detecting early indicators of scanning, cleartext credential leaks, or unauthorized service connections.
