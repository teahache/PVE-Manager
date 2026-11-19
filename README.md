# PVE Manager for Proxmox

<div align="center">
  <img src="assets/css/PVE%20Manager%20for%20Proxmox.jpg" width="100%" alt="PVE Manager for Proxmox Banner" />
  <h3>A modern, fast, and privacy-focused Android client for Proxmox VE &amp; Proxmox Backup Server (PBS).</h3>
  <p>
    <a href="https://play.google.com/store/apps/details?id=com.pvemanager.proxmox">
      <img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" height="58" alt="Get it on Google Play" />
    </a>
  </p>
  <p>
    <a href="https://play.google.com/store/apps/details?id=com.pvemanager.proxmox">
      <img src="https://img.shields.io/badge/Google%20Play-v1.6.2-orange?logo=google-play&amp;logoColor=white" alt="Google Play Version" />
    </a>
    <img src="https://img.shields.io/badge/Platform-Android%207.0%2B%20(API%2024%2B)-brightgreen?logo=android&amp;logoColor=white" alt="Android Version" />
    <img src="https://img.shields.io/badge/Language-Kotlin-7F52FF?logo=kotlin&amp;logoColor=white" alt="Kotlin" />
    <img src="https://img.shields.io/badge/UI-Jetpack%20Compose%20%E2%80%A2%20Material%203-4285F4?logo=jetpackcompose&amp;logoColor=white" alt="Jetpack Compose" />
    <img src="https://img.shields.io/badge/Architecture-Zero--Cloud%20%7C%20100%25%20Local-success?logo=shield" alt="Zero-Cloud" />
    <a href="PRIVACY_POLICY.md">
      <img src="https://img.shields.io/badge/Privacy-Zero%20Data%20Collection-blue" alt="Privacy Policy" />
    </a>
  </p>
</div>

---

## 🚀 Overview

**PVE Manager for Proxmox** allows system administrators, DevOps engineers, and homelab enthusiasts to monitor, control, and troubleshoot their Proxmox VE and Proxmox Backup Server infrastructures directly from Android phones, foldables, and tablets.

Designed for speed, reliability, and security, PVE Manager delivers a native **Material 3** experience with a **100% direct client-to-server** architecture—no intermediary servers, no cloud accounts, and no tracking. You can even explore the entire interface immediately using the built-in **Demo Mode** before adding your own servers.

---

## ✨ Key Highlights

### 🛡️ 100% Zero-Cloud & Privacy-First
* **Direct Connections Only:** All HTTPS REST API calls and SSH connections happen strictly between your Android device and your Proxmox/PBS hosts.
* **No Middleman or Proxy:** No developer-operated relay servers, cloud accounts, or external credential storage.
* **Encrypted Local Storage:** Passwords, API tokens, and SSH keys are stored exclusively on your device inside a locally encrypted Room database and DataStore protected via the Android Keystore.
* **Certificate & Host Key Pinning:** Built-in TLS certificate fingerprint verification for self-signed Proxmox certificates and SSH host key pinning.
* **Encrypted Config Backup:** Export and import your server profiles in a passphrase-encrypted local backup file to easily migrate across devices.

### 🖥️ Unified Proxmox VE & PBS Management
Manage compute, storage, networking, and backups from a single app:
* **Proxmox VE:** Cluster quorum & High Availability (HA) overview, multi-node comparison, VMs (QEMU/KVM), LXC containers, storage, SDN, and PVE firewall.
* **Proxmox Backup Server (PBS):** Datastore capacity & deduplication stats, backup snapshots browser (verify, restore, prune/forget), and sync/verify/GC job monitoring.
* **Global Quick Switcher:** Instantly search and jump to any VM, LXC, node, storage, or server profile.

### 💻 Consoles & Terminals (SSH, xterm, SPICE, noVNC)
* Built-in interactive **SSH Bash shell**, **xterm.js** web console, **noVNC**, and **SPICE** graphical console support.
* Custom command key bar (`Esc`, `Ctrl`, `Alt`, `Tab`, arrow keys, special characters, AZERTY/QWERTY keyboard support) and dedicated text/password injection dialog.
* Manage live sessions, run `htop`/`btop`, inspect logs, and apply system updates on the fly.

### 📊 Real-Time Metrics, GPU & Hardware Sensors
* **Interactive Graphs:** Pinch-to-zoom and touch-scrubbing across live and historical time scales for **CPU, RAM, Swap, GPU, Disk I/O, and Network** traffic.
* **GPU & Hardware Temperatures:** Monitor CPU, motherboard, and GPU temperatures and utilization via SSH.
* **Physical Disks & SMART Health:** Inspect NVMe/SATA health status, SSD wearout percentage, temperatures, serial numbers, and raw SMART attributes.

### 🔔 Background Monitoring, Alerts & Home Widgets
* **Glance Home Screen Widgets:** Responsive small, horizontal, and large Android widgets featuring multi-server and node switching, cluster quorum & pending APT update badges, Wake-on-LAN trigger, favorite VM/LXC power actions, and offline cache fallback.
* **Threshold & Push Alerts:** Configure CPU, RAM, Swap, and Disk alert thresholds alongside periodic background checks (`WorkManager`) for high load, failed tasks, and completed backups.
* **Webhook Integration:** Forward background alerts to your own webhook endpoint with optional Bearer token authentication.

### 📱 Modern Adaptive Android Experience
* **Material 3 & Adaptive Layouts:** Light/dark themes, two-pane list-detail views for Guests and Storage on tablets and foldables, and a customizable Dashboard edit mode.
* **Offline Cache Mode:** Browse cached cluster, node, and guest snapshots when your server is temporarily unreachable.
* **Biometric Security:** Protect the app with Fingerprint or Face Unlock and configurable auto-lock timeout.
* **11 Languages Supported:** English, Français, Español, Deutsch, Português (Brasil), Italiano, Polski, Türkçe, Русский, 日本語, and 中文.

---

## 📋 Feature Breakdown

| Category | Supported Capabilities |
| :--- | :--- |
| **Cluster & Nodes** | Cluster quorum banner, High Availability (HA) resources, multi-node comparison, live CPU/RAM/Swap/GPU/Disk I/O metrics, node journal logs (`journalctl`), APT package updates, reboot/shutdown. |
| **Virtual Machines (QEMU)** | Guided 8-step creation wizard, Start/Stop/Shutdown/Reboot, batch multi-select actions, tag & pool filtering, hardware & Cloud-Init editing, snapshots, backups, clone, migrate, convert to template, FSTrim, guest firewall rules, pending OS update check & upgrade, noVNC/SPICE/xterm consoles. |
| **Containers (LXC)** | Guided 6-step creation wizard, Start/Stop/Reboot, batch actions, tag & pool filtering, resource & network editing, snapshots & rollback, backups, clone, migrate, guest firewall rules, OS update check, shell access. |
| **Backup Server (PBS)** | Datastore usage & deduplication metrics, snapshot list with verify/restore/prune actions, scheduled job & task monitoring. |
| **Storage, Ceph & Disks** | ZFS pools, Ceph cluster health & pools (with OSD scrub), LVM, Directory, NFS, SMB/CIFS, replication jobs, resource pools, scheduled `vzdump` backup jobs (create & run on demand), direct URL ISO/template download, physical disks & SMART diagnostics. |
| **Network, SDN & Firewall** | Linux bridges & physical NIC inspection/editing, pending network changes (`ifupdown2` apply/revert), guest NIC interconnections with Ping diagnostics, SDN Zones & VNets, Cluster & Node PVE Firewall rule management. |
| **Connectivity & Auth** | API Token & PAM/PVE realm auth with automatic 401 ticket refresh, Cloudflare Zero Trust headers, Wake-on-LAN (WOL), TLS certificate & SSH host key pinning, encrypted config export/import. |
| **Terminal & Tasks** | Full SSH terminal emulator with custom key bar & AZERTY support, background Task Tracking & live Task Viewer execution logs. |
| **Widgets & Alerts** | Interactive AndroidX Glance widgets (node/server switch, guest power actions, WOL), CPU/RAM/Swap/Disk threshold alerts, background WorkManager notifications, and custom Webhooks. |

---

## 💎 Fair Freemium Monetization Model

* **Built-in Demo Mode:** Try the full experience immediately with simulated Proxmox VE and PBS infrastructure.
* **Forever Free Tier:** Connect **1 Proxmox VE server**, monitor live node metrics, create & manage VMs/LXCs, run local backups, and use the host SSH terminal forever with no time limit.
* **No Subscriptions:** Homelab and infrastructure tools shouldn't require recurring monthly fees.
* **Lifetime Pro (One-Time Purchase):** A single in-app purchase unlocks **Pro** forever across your Android devices (with **Google Play Family Sharing** support): unlimited PVE servers, Proxmox Backup Server (PBS), guest consoles (noVNC/SPICE/xterm), guest hardware & config editing, cluster migrations, host network & firewall editing, storage configuration, background alerts & webhooks, encrypted config export/import, and home screen widgets.

---

## 🛠 Tech Stack & Architecture

* **Language:** Kotlin 2.x
* **UI Framework:** Jetpack Compose with Material 3 & adaptive multi-pane layouts
* **Concurrency:** Kotlin Coroutines & Flow
* **Dependency Injection:** Dagger Hilt
* **Database & Storage:** Room Database (offline cache & encrypted server storage) & DataStore
* **Networking & Protocols:**
  * Retrofit 2 & Moshi for Proxmox REST API integration
  * OkHttp with custom TLS certificate pinning (`PinningTrustManager`)
  * JSch for SSH shell sessions, hardware sensors, and host key pinning
* **Background & Widgets:** AndroidX WorkManager & AndroidX Glance AppWidget
* **Security:** AndroidX Biometric & Android Keystore

---

## 📥 Download & Installation

**PVE Manager for Proxmox** is distributed exclusively on **Google Play** for automated updates, Play Integrity/security checks, and seamless license restoration across devices:

<a href="https://play.google.com/store/apps/details?id=com.pvemanager.proxmox">
  <img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" height="54" alt="Get it on Google Play" />
</a>

*(Note: PVE Manager for Proxmox is proprietary closed-source software; standalone APKs and source code are not published on GitHub.)*

---

## 🔒 Security, Privacy & Terms

For full details regarding terms of use and how permissions and data are handled, please review our [Privacy Policy](PRIVACY_POLICY.md) and [Terms of Service](TERMS_OF_SERVICE.md).

* **Zero Personal Telemetry:** The app never collects personal information or sends your server data to the developer.
* **Optional Diagnostics:** Anonymized crash reports (Firebase Crashlytics) and anonymous usage analytics can be disabled at any time in the app's **Options** screen.

---

## ⚖️ Legal Disclaimer

**Proxmox®** is a registered trademark of Proxmox Server Solutions GmbH.

*PVE Manager for Proxmox* is an independent third-party mobile application. It is **not** affiliated with, endorsed by, sponsored by, or supported by Proxmox Server Solutions GmbH.

---

## 🤝 Feedback & Support

* Questions, bug reports, or feature requests? Contact the developer directly: [pve_manager@etik.com](mailto:pve_manager@etik.com)

<div align="center">
  <em>Developed with ❤️ for the self-hosted and homelab community.</em>
</div>
