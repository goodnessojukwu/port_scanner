📌 Project Description

This project was developed for NAU-CYB 221 – Cybersecurity Technology.

The tool:

Enumerates all listening TCP ports

Enumerates all listening UDP ports

Identifies:

Port number

Protocol (TCP/UDP)

Local address

Process name

PID

Service name (if available)

Labels ports as:

Local-only

Exposed

Exports results to:

Terminal table

.txt report

.json report

🛠️ Features
✅ Core Features

Local port enumeration (TCP + UDP)

Process & PID detection

Sorted output (Protocol → Port)

Export to file

Service name mapping (e.g., 22 → SSH)

⭐ Advanced Features

Filter options:

--tcp

--udp

--min-port

Risk classification:

127.0.0.1 / ::1 → Local-only

0.0.0.0 / :: → Exposed

Flags high-interest ports:

21, 22, 23, 25, 53, 80, 110, 139, 143, 443, 445, 3389

“Top 5 Security Attention” summary

📂 Project Structure
local-port-discovery/
│
├── port_scanner.py
├── ports_report.txt
├── ports_report.json
├── README.md
└── requirements.txt
🚀 Installation
1️⃣ Clone the repository
git clone https://github.com/yourusername/local-port-discovery.git
cd local-port-discovery
2️⃣ Install dependencies
pip install -r requirements.txt

If requirements.txt does not exist:

pip install psutil
▶️ Usage

Run the program:

python port_scanner.py

Filter options:

python port_scanner.py --tcp
python port_scanner.py --udp
python port_scanner.py --min-port 1024
📊 Example Output
Protocol  Port   Local Address   PID     Process     Service   Risk
----------------------------------------------------------------------
TCP       22     0.0.0.0         1024    sshd        SSH       Exposed
TCP       631    127.0.0.1       890     cups        IPP       Local-only
UDP       53     0.0.0.0         720     named       DNS       Exposed
TCP       3389   0.0.0.0         1140    svchost     RDP       Exposed
🛡️ Risk Classification
Address Binding	Risk Level
127.0.0.1	Local-only
::1	Local-only
0.0.0.0	Exposed
::	Exposed

Exposed services may be reachable from other systems on the network.

🖥️ Supported Operating Systems

Windows 10 / 11

Linux (Ubuntu, Kali, etc.)

macOS

⚠️ Administrator/root privileges may be required to retrieve process names for certain ports.

🔐 Security Purpose

Open ports increase system attack surface. This tool helps:

Identify unnecessary exposed services

Reduce risk through firewall configuration

Improve secure system configuration practices

⚖️ Ethics & Legal Notice

This tool only inspects the local system

No remote scanning capability is included

Users must test only on systems they own or have explicit permission to assess

Unauthorized scanning of networks is illegal.

📚 Educational Context

Developed as part of:

Course: NAU-CYB 221 – Cybersecurity Technology
Topic: Local Port Discovery & Service Identification
Year: 2026

📄 License

This project is for educational purposes only.
