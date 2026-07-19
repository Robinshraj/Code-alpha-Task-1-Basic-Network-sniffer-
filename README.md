# 🛡️ Network Sniffer

A Python-based network packet sniffer built using **Scapy**, developed and tested on **Kali Linux**. This tool captures live network traffic and displays key packet details such as source/destination IP addresses, protocol type, port numbers, and raw payload data — helping to understand how data moves across a network at the packet level.

---

## 📌 Project Overview

Packet sniffing is a fundamental technique in network analysis and cybersecurity used to monitor, capture, and inspect data traveling across a network. This project implements a lightweight command-line network sniffer in Python that leverages Scapy to capture live packets and extract meaningful information from them in real time.

This project was built as a hands-on learning exercise to understand networking fundamentals (IP, TCP, UDP, ICMP), packet structures, and how tools like Wireshark work under the hood.

---

## ✨ Features

- 📡 Captures live packets from the network interface in real time
- 🌐 Displays Source IP and Destination IP addresses
- 🔢 Identifies the protocol number (`1` = ICMP, `6` = TCP, `17` = UDP)
- 🔌 Displays TCP source and destination ports when available
- 📦 Extracts and prints raw payload data from captured packets
- 🖥️ Simple, readable console output with clear packet separators

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| **Python 3** | Core programming language |
| **Scapy** | Packet crafting, sniffing, and analysis library |
| **Kali Linux** | Development and testing environment |
| **Nano / Terminal** | Script editing and execution |

---

## ⚙️ Setup Instructions

### Prerequisites
- Kali Linux (or any Linux distribution)
- Python 3 installed
- Root/sudo privileges (required for raw packet capture)

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/network-sniffer.git
cd network-sniffer
```

### 2. Install Scapy
```bash
sudo apt update
sudo apt install python3-scapy -y
```

> 💡 If installing via pip, use a virtual environment since Kali's Python is externally managed:
> ```bash
> python3 -m venv venv
> source venv/bin/activate
> pip install scapy
> ```

### 3. Run the Sniffer
```bash
sudo python3 sniffer.py
```

> ⚠️ Root privileges are required because raw socket access is needed to capture packets.

---

## 📄 Sample Output

```
==================================================
Source IP: 10.0.2.15
Destination IP: 142.250.182.110
Protocol: 1
Payload: b'\xbarTj\x00\x00\x00\x00\xff\x05\x05\x00\x00\x00\x00\x10\x11\x12...'

==================================================
Source IP: 10.0.2.15
Destination IP: 10.74.10.88
Protocol: 17

==================================================
Source IP: 10.74.10.88
Destination IP: 10.0.2.15
Protocol: 17
```

---

## 🖼️ Screenshots

| Step | Description |
|---|---|
| 1️⃣ | Writing the sniffer script in Nano (`sniffer.py`) |
| 2️⃣ | Setting up the environment — updating packages, checking Python version, installing dependencies |
| 3️⃣ | Installing Scapy via `apt` and verifying the import works in the Python shell |
| 4️⃣ | Creating the project directory and running the sniffer for the first time |
| 5️⃣ | Live program output showing captured packets with source/destination IPs, protocol, and payload |

*(Add your screenshot image files to a `/screenshots` folder in the repo and reference them here, e.g. `![Script Editing](screenshots/code_1.jpeg)`)*

---

## 🖥️ Program Output

When executed, the script listens on the network interface and prints details for each captured packet as it arrives, including:
- A separator line for readability
- Source and Destination IP addresses
- Protocol number
- TCP port information (if applicable)
- Raw payload bytes (if applicable)

The sniffer stops automatically after capturing the specified number of packets (set via the `count` parameter in the script), or can be configured to run continuously.

---

## 📁 Repository Structure

```
network-sniffer/
│
├── sniffer.py          # Main packet sniffing script
├── README.md           # Project documentation
├── LICENSE             # License file
└── screenshots/        # Screenshots of setup and program output
    ├── code_1.jpeg
    ├── code_2.jpeg
    ├── code_3.jpeg
    ├── code_4.jpeg
    └── code_5.jpeg
```

---

## 🎓 Learning Outcomes

Through this project, I gained hands-on experience with:
- Understanding the fundamentals of network protocols (IP, TCP, UDP, ICMP)
- Using Scapy to sniff and analyze live network packets
- Working with Linux terminal environments and package management (`apt`, `pip`, virtual environments)
- Handling permission and dependency issues (e.g. externally managed Python environments)
- Interpreting raw packet data and payloads
- Building a foundational tool that mirrors core functionality of professional tools like Wireshark

---

## ⚠️ Disclaimer

This tool is developed **strictly for educational and ethical learning purposes**. It should only be used on networks you own or have explicit, written permission to monitor. Unauthorized interception or monitoring of network traffic may violate privacy laws and regulations in your jurisdiction. The author is not responsible for any misuse of this tool.

---

## 👤 Author

**Robinsh Raj**
BCA Student | Cybersecurity Enthusiast | Cyber Security Intern @ Code Alpha

---

## 🙏 Acknowledgements

- [Scapy Documentation](https://scapy.net/) — for the powerful packet manipulation library
- [Kali Linux](https://www.kali.org/) — for the security-focused testing environment
- **Code Alpha** — for the internship opportunity and guidance that inspired this project
- The wider cybersecurity community for tutorials and resources on packet analysis

---
