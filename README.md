# Cyber Kill Chain Attack Simulation using Kali Linux and Mythic C2

## 📌 Project Overview

This project demonstrates a complete Cyber Kill Chain based attack simulation in a controlled lab environment using Kali Linux, Mythic C2, and a Windows Server target machine.

The objective of this project is to simulate a real-world cyber attack lifecycle including:

- Initial Access
- RDP Brute Force Attack
- Remote Access
- Defense Evasion
- Payload Delivery
- Command and Control (C2)
- Data Exfiltration

This project was created for educational and cybersecurity research purposes only.

---

# 🏗️ Lab Architecture

## Machines Used

| Machine | Purpose |
|----------|----------|
| Kali Linux | Attacker Machine |
| Ubuntu Server | Mythic C2 Server |
| Windows Server | Victim Machine |

---

# ⚙️ Technologies & Tools Used

- Kali Linux
- Mythic C2
- Apollo Agent
- Hydra
- Crowbar
- xfreerdp
- Windows Server
- RDP
- Python HTTP Server
- Docker & Docker Compose

---

# 🔥 Attack Flow

## 1. Environment Setup

- Ubuntu server configured as Mythic C2 server
- Windows Server configured as victim machine
- Kali Linux configured as attacker machine

---

## 2. Initial Access – RDP Brute Force

The attacker machine performed a brute-force attack against the Windows Server RDP service using tools like:

- Hydra
- Crowbar

After multiple authentication attempts, valid credentials were obtained.

---

## 3. Remote Access

Using the compromised credentials, the attacker successfully logged into the Windows Server via RDP.

---

## 4. Defense Evasion

Windows Defender and firewall protections were disabled to avoid payload detection.

---

## 5. Payload Delivery

A Mythic Apollo payload was generated and delivered to the Windows machine using a Python HTTP server.

### Payload Delivery Example

```bash
python3 -m http.server 9999
```

## 6. Payload Execution

The payload was executed on the victim machine, establishing communication with the Mythic C2 server.

## 7. Command and Control (C2)

After successful execution, the Windows machine connected back to Mythic C2, allowing remote command execution from the Mythic dashboard.

Capabilities Included
Command execution
File browsing
File upload/download
Remote shell access

## 8. Data Exfiltration

Sensitive files were downloaded from the compromised Windows machine to simulate data theft.

🧠 Cyber Kill Chain Mapping
Cyber Kill Chain Phase	Project Activity
Reconnaissance	Target Identification
Weaponization	Mythic Apollo Payload Creation
Delivery	Payload Transfer
Exploitation	RDP Access & Payload Execution
Installation	Apollo Agent Execution
Command & Control	Mythic Session Established
Actions on Objectives	Sensitive File Exfiltration



⚠️ Disclaimer

This project was developed strictly for educational purposes and authorized lab testing only.

The tools and techniques demonstrated in this repository should not be used against systems without proper authorization.

The author is not responsible for any misuse of this project.

👨‍💻 Author

Solanki Aakash Girishbhai
Cyber Security Student
Final Year Project
