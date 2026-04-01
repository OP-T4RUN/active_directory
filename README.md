# 🏠 Active Directory Home Lab

> A hands-on Active Directory security and penetration testing lab built from scratch using VMware, Windows Server 2022, and PowerShell — following [John Hammond's Active Directory series](https://www.youtube.com/playlist?list=PL1H1sBF1VAKVoU6Q2u7BBGPsnkn-rajlp).

---

## 📋 Lab Overview

| Field | Details |
|---|---|
| Platform | VMware Workstation Pro 17 |
| Domain | xyz.com |
| Domain Controller | DC1 — Windows Server 2022 Core |
| Workstation | WS01 — Windows 11 Pro N |
| Network | NAT — 192.168.15.0/24 |
| Purpose | Learning AD security & penetration testing |
| Status | In Progress |

---

## 🖥️ Lab Architecture
```
Host Machine (AMD Ryzen 7 7445HS)
└── VMware Workstation Pro 17 — NAT Network: 192.168.15.0/24
    ├── DC1   Windows Server 2022 Core   192.168.15.155 (Static)
    │         Roles: AD DS, DNS, Kerberos
    │
    └── WS01  Windows 11 Pro N           192.168.15.132 (DHCP)
              Joined to xyz.com
              DNS → 192.168.15.155
```

---

## 📚 Chapters

| # | Title | Status |
|---|---|---|
| [Chapter 0](Chapters/Chapter-0/README.md) | Creating Our Server + Workstation Virtual Environment | ✅ Complete |
| [Chapter 1](Chapters/Chapter-1/README.md) | Joining a Home Lab Domain (Installing the Domain Controller) | ✅ Complete |
| [Chapter 2](Chapters/Chapter-2/README.md) | Automating Domain Users & Groups | ✅ Complete |
| Chapter 3 | AD User Management / Group Policy | 🔜 Upcoming |
| Future | BloodHound Enumeration | 🔜 Upcoming |
| Future | Kerberoasting | 🔜 Upcoming |
| Future | Pass-the-Hash / Pass-the-Ticket | 🔜 Upcoming |
| Future | Golden Ticket Attack | 🔜 Upcoming |
| Future | Privilege Escalation in AD | 🔜 Upcoming |

---

## 🌐 Domain Info

| Field | Value |
|---|---|
| Domain Name | xyz.com |
| NetBIOS Name | XYZ |
| Forest | xyz.com |
| Domain SID | S-1-5-21-1327692051-1775273641-3263256819 |
| PDC Emulator | DC1.xyz.com |
| DNS Root | xyz.com |

### Domain Computers

| Computer | Role | IP |
|---|---|---|
| DC1 | Domain Controller | 192.168.15.155 |
| DESKTOP-8TCVO2K | Workstation (WS01) | 192.168.15.132 |

### Domain Users

| Username | Full Name | Group | Status |
|---|---|---|---|
| Administrator | — | Domain Admins | Enabled |
| alice | Alice lice | Employees | Enabled |
| bob | Bob Ob | Employees | Enabled |
| Guest | — | — | Disabled |
| krbtgt | — | — | Disabled |

### Domain Groups

| Group | Scope | Purpose |
|---|---|---|
| Domain Admins | Global | Built-in admin group |
| Employees | Global | Custom group — created in Chapter 2 |
| DnsAdmins | Domain Local | DNS administration |

---

## 🧰 Tools Used

| Tool | Category | Chapters |
|---|---|---|
| VMware Workstation Pro 17 | Virtualization | 0, 1 |
| Windows Server 2022 | OS | 0, 1 |
| Windows 11 Pro N | OS | 0, 1 |
| PowerShell | Scripting / Mgmt | 1, 2 |
| sconfig | Server Config | 1 |
| AD DS Role | Active Directory | 1 |
| PS Remoting | Remote Mgmt | 1, 2 |
| JSON Schema | IaC / Config | 2 |
| BloodHound | AD Enumeration | 🔜 |
| Impacket | AD Attacks | 🔜 |
| PowerView | AD Enumeration | 🔜 |

---

## 📁 Repository Structure
```
active_directory/
├── README.md
└── Chapters/
    ├── Chapter-0/
    │   ├── README.md
    │   └── screenshots/          (13 screenshots)
    ├── Chapter-1/
    │   ├── README.md
    │   └── screenshots/          (12 screenshots)
    └── Chapter-2/
        ├── README.md
        ├── screenshots/          (8 screenshots)
        └── code/
            ├── gen_ad.ps1
            └── ad_schema.json
```

---

## 📌 Resources

| Resource | URL |
|---|---|
| John Hammond YouTube | https://www.youtube.com/@_JohnHammond |
| Microsoft AD Documentation | https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/ |
| Microsoft Evaluation Center | https://www.microsoft.com/en-us/evalcenter/ |
| VMware Workstation | https://www.vmware.com/products/workstation-pro.html |