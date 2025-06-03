# kerberos-golden-ticket-report
Red Team engagement report demonstrating Kerberoasting and Golden Ticket attack simulation
# 🎯 Kerberos Golden Ticket Red Team Report

**Author:** Zion Spearman  
**Date:** May 31, 2025  
**Client:** FakeCorp Industries (Lab Simulation)  
**Confidentiality:** Internal use only. Not for external distribution.

---

## 📝 Project Overview

This repository contains a red team engagement report simulating a targeted Active Directory compromise using **Kerberoasting** and **Golden Ticket** attack techniques. The assessment was conducted in a controlled lab environment and mirrors real-world post-exploitation scenarios against enterprise networks.

---

## 📄 Report Contents

- `Red Team - Kerberos Golden Ticket.docx`: [Red Team - Kerberos Golden Ticket.docx](https://github.com/user-attachments/files/20575636/Red.Team.-.Kerberos.Golden.Ticket.docx)
 
  A detailed red team report documenting:
  - Initial access and payload delivery
  - Kerberoasting and service ticket extraction
  - Golden Ticket forging and domain persistence
  - Lateral movement across subnets
  - Domain Controller compromise and data exfiltration
  - Screenshots and analysis of tools and commands used

---

## 🛠️ Tools Used

- Metasploit Framework (reverse shell, handler, SOCKS proxy)
- Mimikatz / Kiwi (Golden Ticket creation, token impersonation)
- PowerShell / CMD
- Apache2 (payload delivery)
- Remote Desktop Protocol (Admin access)
- `nano`, `whoami`, `klist`, `ip a`, `ps`, and others

---

## 📌 Attack Objectives

- Extract service account credentials (TGS ticket hashes)
- Forge a Golden Ticket using krbtgt hash
- Access domain-level resources (C$ share, RDP sessions)
- Maintain stealth and persistence within the network
- Demonstrate realistic adversary tactics post-exploitation

---

## ⚠️ Impact Summary

- **Full Domain Admin access**
- **Lateral movement across segmented subnets**
- **DCSync attack** to extract krbtgt hash
- **Persistent domain access** without reauthentication
- **Sensitive file access** (e.g., `flag204090.txt`, `dns.log`)

---

## ✅ Recommendations

- Reset the **krbtgt** account password twice post-compromise
- Deploy **SIEM monitoring** for abnormal Kerberos activity
- Limit use of **Domain Admin accounts**
- Segment internal networks and restrict RDP
- Employ **EDR** tools to detect Mimikatz-like behavior

---

## 🔐 Disclaimer

> This report is for academic and internal training purposes only.  
> All findings and techniques were performed in a controlled lab environment.  
> Unauthorized replication or distribution is strictly prohibited.

