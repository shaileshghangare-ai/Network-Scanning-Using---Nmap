# 🔎 Network Scanning using Nmap

## 📌 Project Overview

This project demonstrates network scanning using Nmap on a Linux system.

The project covers:

1. Host Discovery
2. Port Scanning
3. Service & Version Detection
4. OS Detection
5. NSE Script Scanning
6. Firewall Detection
7. Scan Report

---

## 🎯 Objective

The objective of this project is to understand how Nmap can be used to perform network discovery, port scanning, service identification, operating system detection, NSE script scanning, and firewall
analysis.

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Nmap | Network Scanning |
| Linux | Testing Environment |
| Terminal | Command Execution |

# 1️⃣ Nmap Installation

## Command

```bash
sudo apt update
sudo apt install nmap -y
```
**Description:**
Nmap was installed on the Linux system.
<img width="1600" height="842" alt="WhatsApp Image 2026-09-19 at 13 38 23" src="https://github.com/user-attachments/assets/b3d0bf76-2dd3-4bd6-afce-32df5c5f6435" />
<img width="1600" height="843" alt="WhatsApp Image 2026-09-19 at 14 31 47" src="https://github.com/user-attachments/assets/570ef354-2421-402c-80e0-7492c13aa69b" />

# 2️⃣ Host Discovery

## Command

```bash
nmap -sn 127.0.0.1
```
**Description:**
The -sn option performs host discovery without performing a traditional port scan. It is used to determine whether the target host is available.
<img width="1600" height="843" alt="WhatsApp Image 2026-09-19 at 14 31 47 (1)" src="https://github.com/user-attachments/assets/a797f514-8772-4ecd-8cf1-53de3afac0e9" />

# 3️⃣ Port Scanning

## Command

```bash
sudo nmap -p- 127.0.0.1
```
**Description:**
The -p- option scans all TCP ports from 1 through 65535. The scan helps identify open, closed, and filtered ports.
<img width="1600" height="843" alt="WhatsApp Image 2026-09-19 at 14 31 48" src="https://github.com/user-attachments/assets/d43a715b-4dfa-4873-b1ce-811f85d2bb0d" />

# 4️⃣ Service & Version Detection

## Command

```bash
sudo nmap -sV 127.0.0.1
```
**Description:**
The -sV option attempts to identify services running on open ports and obtain available version information.<img width="1600" height="843" alt="WhatsApp Image 2026-09-19 at 14 31 48 (1)" src="https://github.com/user-attachments/assets/b040e9f6-8ec9-49a6-b9e6-2179dd27e2ec" />

# 5️⃣ OS Detection

## Command

```bash
sudo nmap -O 127.0.0.1
```
**Description:**
The -O option attempts to identify the operating system of the target. OS detection may be limited when scanning localhost.
<img width="1600" height="843" alt="WhatsApp Image 2026-09-19 at 14 31 48 (2)" src="https://github.com/user-attachments/assets/129a7eb9-47f2-41c5-b4ba-c70a0a61ac84" />

# 6️⃣ NSE Script Scanning

## Command

```bash
sudo nmap -sC -sV 127.0.0.1
```
**Description:**
The -sC option runs Nmap's default NSE scripts. The -sV option performs service and version detection. This provides additional information about detected services.
<img width="1600" height="843" alt="WhatsApp Image 2026-09-19 at 14 31 48 (3)" src="https://github.com/user-attachments/assets/2321d390-bef9-4567-805d-3c249896e5ca" />

# 7️⃣ Firewall Detection

## Command

```bash
sudo nmap -sA 127.0.0.1
```
**Description:**
The -sA option performs an ACK scan. The scan can be used to analyze packet-filtering behavior and identify filtered or unfiltered responses.
<img width="1600" height="843" alt="WhatsApp Image 2026-09-19 at 14 31 48 (4)" src="https://github.com/user-attachments/assets/2b3b168f-1873-4944-8efa-24ca20dc5c01" />

# 8️⃣ Final Nmap Scan

## Command

```bash
sudo nmap -sC -sV -O 127.0.0.1
```
**Description:**
The final scan combines:

- Default NSE scripts
- Service and version detection
- OS detection

This provides a consolidated view of the target
<img width="1600" height="843" alt="WhatsApp Image 2026-09-19 at 14 31 48 (5)" src="https://github.com/user-attachments/assets/5183ec6f-334e-4a6a-8720-84321c25eab6" />



