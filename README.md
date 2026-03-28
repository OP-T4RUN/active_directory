# 🏰 Active Directory Home Lab

![Active Directory](https://img.shields.io/badge/Active%20Directory-Windows%20Server%202022-blue?style=for-the-badge&logo=windows)
![Platform](https://img.shields.io/badge/Platform-VMware%20Workstation%2017-lightgrey?style=for-the-badge&logo=vmware)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow?style=for-the-badge)
![Based On](https://img.shields.io/badge/Based%20On-John%20Hammond%20AD%20Playlist-red?style=for-the-badge&logo=youtube)

---

## 📖 About This Repository

This repository contains structured, chapter-by-chapter write-ups
of my hands-on journey learning **Active Directory (AD)** security
and penetration testing, following the
[Active Directory playlist by John Hammond](https://www.youtube.com/@_JohnHammond).

The goal is to:
- 🧠 **Document** every concept, command, and configuration
- 🔬 **Build** a fully functional AD home lab from scratch
- 🛡️ **Understand** both the defensive and offensive sides of AD
- 📝 **Create** a reference I (and others) can revisit anytime

> ⚠️ **Disclaimer:** This repository is strictly for
> **educational purposes** in a controlled lab environment.
> Never use these techniques on systems you do not own
> or have explicit permission to test.

---

## 🖥️ Lab Environment

| Component | Details |
|---|---|
| Virtualization | VMware Workstation Pro 17 |
| Domain Controller | Windows Server 2022 (Server Core) |
| Workstation | Windows 11 Pro N for Workstations |
| Domain Name | `xyz.com` |
| DC Hostname | `DC1` |
| DC IP Address | `192.168.15.155` (Static) |
| Network Type | NAT |

---

## 📚 Chapter Index

| Chapter | Title | Topics Covered | Status |
|---|---|---|---|
| [Chapter 0](Chapters/Chapter-0/README.md) | Creating Our Server + Workstation Virtual Environment | VMware setup, Windows Server 2022 (Server Core) install, Windows 11 install, TPM bypass, snapshots | ✅ Done |
| [Chapter 1](Chapters/Chapter-1/README.md) | Joining a Home Lab Domain | PS Remoting, static IP via sconfig, AD DS install, DC promotion, domain join | ✅ Done |
| Chapter 2 | Coming Soon | — | 🔜 |

---

## 🗂️ Repository Structure
```
active_directory/
└── Chapters/
    ├── Chapter-0/
    │   ├── README.md
    │   └── screenshots/
    ├── Chapter-1/
    │   ├── README.md
    │   └── screenshots/
    └── ...
```

---

## 🧰 Tools Used Across This Series

| Tool | Purpose |
|---|---|
| VMware Workstation Pro 17 | Virtualization platform |
| Windows Server 2022 | Domain Controller OS |
| Windows 11 | Workstation / client OS |
| PowerShell | Primary management interface |
| `sconfig` | Server Core configuration tool |
| Active Directory Domain Services (AD DS) | Core AD role |
| BloodHound | AD enumeration & attack path visualization *(upcoming)* |
| Impacket | AD attack toolkit *(upcoming)* |
| PowerView | AD enumeration via PowerShell *(upcoming)* |

---

## 📌 Resources

- 🎥 [John Hammond's YouTube Channel](https://www.youtube.com/@_JohnHammond)
- 📘 [Microsoft AD Documentation](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/get-started/virtual-dc/active-directory-domain-services-overview)
- 🧰 [Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter/)

---

## 👤 Author

**OP-T4RUN**
- GitHub: [@OP-T4RUN](https://github.com/OP-T4RUN)

---

*⭐ If you find this helpful, consider starring the repo!*