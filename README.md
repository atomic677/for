<div align="center">

# ⚡ Enhanced Multi-VM Manager  
### **QEMU/KVM Cloud-Image Virtual Machine Orchestrator**

![bash](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnu-bash&logoColor=fff)
![License](https://img.shields.io/badge/License-Custom-blue)
![Status](https://img.shields.io/badge/Status-Active-success)
![Platform](https://img.shields.io/badge/Platform-Linux-lightgrey)
![KVM](https://img.shields.io/badge/KVM-Accelerated-important)

**Version: v2.2**

A fully-interactive, cloud-image–powered Virtual Machine Manager written entirely in **Bash**, supporting automated OS deployment, cloud-init configuration, snapshots, cloning, backups, and full VM lifecycle operations.

</div>

---

# 📑 **Table of Contents**

1. [Overview](#-overview)  
2. [Key Features](#-key-features)  
3. [System Requirements](#-system-requirements)  
4. [Supported Guest OS Images](#-supported-guest-os-images)  
5. [Installation](#-installation)  
6. [Quick Start](#-quick-start)  
7. [VM Lifecycle](#-vm-lifecycle)  
8. [Architecture](#-architecture)  
9. [Configuration Files](#-configuration-files)  
10. [Port Forwarding](#-port-forwarding)  
11. [Screenshots](#-screenshots)  
12. [Troubleshooting](#-troubleshooting)  
13. [Security Notes](#-security-notes)  
14. [Contributing](#-contributing)  
15. [License](#-license)

---

# 🌐 **Overview**

**Enhanced Multi-VM Manager** is a Bash-based project that automates the full creation and management of Linux virtual machines using **QEMU + KVM** with minimal host overhead.

It uses:

- **Cloud images** (official OS vendor images)  
- **Overlay qcow2 disks** (space efficient)  
- **cloud-init ISO generation** (automatic users, SSH access, hostname, password)  
- **Interactive menu system** (TUI-style)

This tool is ideal for:

🧪 Developers  
🧱 Homelab users  
☁️ Cloud engineers  
🔧 Sysadmins  
🏫 Students learning virtualization

---

# 🚀 **Key Features**

### 🔧 Core Functionality
| Feature | Description |
|--------|-------------|
| **Create/Delete VM** | Build VMs from cloud images with cloud-init user configuration |
| **Start/Stop VMs** | Run VMs in foreground or background |
| **Snapshots** | Create, list, restore, and delete VM snapshots |
| **Cloning** | Fast clone VMs from existing ones |
| **Disk Resize** | Expand qcow2 virtual disks |
| **Config Editor** | Modify CPU, RAM, ports, disk, or attached ISO |
| **SSH Ready** | Auto-injected user/password & authorized keys |
| **Multiple OS choices** | Ubuntu, Debian, Fedora, CentOS, Rocky, AlmaLinux, Arch, openSUSE, Alpine |

### 💎 Additional Enhancements
✔ Automatic port conflict detection  
✔ Hash-based password generation  
✔ Dependency auto-checker  
✔ System information screen  
✔ Optimized KVM acceleration detection  
✔ Color-coded output & error messages  

---

# 🖥️ **System Requirements**

### Host Requirements
- Linux OS  
- QEMU 4+  
- KVM support (`/dev/kvm`) recommended  
- 2+ GB RAM minimal, 8+ GB recommended  
- 10+ GB free storage  

### Required Packages
- `bash`
- `qemu-system-x86_64`
- `qemu-img`
- `wget`

### Optional but Recommended
- `cloud-localds` OR `genisoimage`
- `openssl`
- `ss` or `netstat`

---

# 🗂 **Supported Guest OS Images**

The script downloads and manages official cloud images from:

### **Ubuntu**
- 22.04 LTS  
- 24.04 LTS  
- 24.10 / 25.04  

### **Debian**
- 11 (Bullseye)  
- 12 (Bookworm)  
- 13 (Trixie)  

### **RedHat Family**
- Fedora 40 / 41  
- CentOS Stream 9  
- Rocky Linux 9  
- AlmaLinux 9  
- Oracle Linux 9  

### **Others**
- Arch Linux  
- openSUSE Leap / Tumbleweed  
- Alpine Linux 3.20  

---

# 📦 **Installation**

Clone the repository:

```bash
git clone https://github.com/<your-username>/vps123.git
cd vps123
chmod +x my.sh
./my.sh
