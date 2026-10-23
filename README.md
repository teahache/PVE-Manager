# PVE Manager for Proxmox

<div align="center">
  <img src="https://play-lh.googleusercontent.com/j4h5z1ma1RcYWbqKeaqoVvnbWj53AnMbdLpz95NDn4G_bldI8M29fismald1jSBcL5t68-qeqcl5tVu-_I7lNw=w240-h480-rw" width="240" height="240" alt="PVE Manager Logo" />
  <h3>A modern, fast, and privacy-focused Android client for Proxmox VE &amp; Proxmox Backup Server (PBS).</h3>
  <p>
    <a href="https://play.google.com/store/apps/details?id=com.pvemanager.proxmox">
      <img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" height="58" alt="Get it on Google Play" />
    </a>
  </p>
  <p>
    <a href="https://play.google.com/store/apps/details?id=com.pvemanager.proxmox">
      <img src="https://img.shields.io/badge/Google%20Play-v1.5.0-orange?logo=google-play&amp;logoColor=white" alt="Google Play Version" />
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

**PVE Manager for Proxmox** allows system administrators, DevOps engineers, and homelab enthusiasts to monitor, control, and troubleshoot their Proxmox infrastructures directly from their Android smartphones and tablets.

Designed with performance, responsive ergonomics, and security at its core, PVE Manager provides a clean native **Material 3** experience without any cloud reliance or tracking.

---

## ✨ Key Highlights

### 🛡️ 100% Zero-Cloud & Privacy-First
* **Direct Connections Only:** All HTTPS REST API calls and SSH connections are established strictly between your mobile device and your own Proxmox/PBS servers.
* **No Middleman or Proxy:** The developer operates no intermediary servers, cloud accounts, or relays.
* **Encrypted Local Storage:** Passwords, API tokens, and SSH private keys are stored exclusively on your device, encrypted in the app's local database.

### 🖥️ Unified Proxmox VE + PBS Management
Manage your compute and backup infrastructures within a single application:
* **Proxmox VE:** Full cluster overview, nodes, VMs (QEMU/KVM), and LXC containers.
* **Proxmox Backup Server (PBS):** Datastores, backup snapshots, verification jobs, and pruning tasks.

### 💻 Consoles & Terminals (xterm, SPICE, noVNC)
* Built-in interactive **SSH Bash shell**, **SPICE graphical console**, and **noVNC** support.
* Custom command key bar (Esc, Ctrl, Alt, Tab, Arrow keys, AZERTY layout support).
* Run commands, monitor processes (`htop`, `btop`), inspect logs, and manage instances on the fly.

### 🔌 Network & Remote Connectivity
* **Cloudflare Zero Trust:** Connect securely using Client ID / Client Secret headers without exposing open ports.
* **Wake-on-LAN (WOL):** Remotely power on off-line Proxmox nodes directly from the app.

### 📊 Real-Time Metrics, Sensors & SMART Diagnostics
* **Interactive Charts:** Pinch-to-zoom and touch-scrubbing for CPU, RAM, Network, and Disk I/O graphs.
* **Hardware Sensors:** Monitor CPU and motherboard temperatures via SSH.
* **Physical Disk & SMART Health:** View disk health status, SSD wearout percentage, NVMe/SATA protocols, and serial numbers.

### 📱 Modern Android Experience
* **Material 3 Design:** Dynamic theming, light/dark mode consistency, and adaptive layouts for phones and tablets.
* **Home Screen Widgets:** Monitor cluster health and node load at a glance using Android App Widgets (Glance).
* **Biometric Security:** Secure the app with your device's Fingerprint or Face Unlock.

---

## 📋 Feature Breakdown

| Category                    | Supported Capabilities                                                                      |
| :-------------------------- | :------------------------------------------------------------------------------------------ |
| **Nodes & Cluster**         | Live CPU/RAM/Swap usage, disk space, kernel version, uptime, node updates, reboot/shutdown. |
| **Virtual Machines (QEMU)** | Guided creation wizard (8 steps), Start, Stop, Reboot, Snapshot management, disk resizing, SPICE/noVNC console. |
| **Containers (LXC)**        | Guided creation wizard (6 steps), Start, Stop, Console access, vCPU/NUMA/Swap allocations, snapshot rollback. |
| **Backup Server (PBS)**     | Datastore capacity, verification status, backup snapshots list, prune task monitoring.      |
| **Physical Disks & SMART**  | Disk health status, wearout %, serial number, NVMe/SATA protocols, raw terminal diagnostics. |
| **Storage & Templates**     | ZFS, Ceph, LVM, Directory, NFS, SMB/CIFS monitoring, and direct URL template downloads.     |
| **System Maintenance**      | APT package manager with live update progress tracking and Task Viewer execution logs.     |
| **Network & Remote Access** | Cloudflare Zero Trust headers, Wake-on-LAN (WOL), SSL certificate fingerprint verification. |
| **Terminal & Shell**        | Full SSH terminal emulator with custom key bar and AZERTY layout support.                  |
| **Dashboard & Customization**| Custom edit mode to reorder, hide, or display cluster metrics cards.                       |

---

## 💎 Fair Freemium Monetization Model

* **Forever Free Tier:** Connect 1 PVE server, manage and create VMs/LXCs, inspect live node metrics, use local backups, and use the built-in host terminal forever with no time limit.
* **No Subscriptions:** We don't believe in locking homelab tools behind recurring monthly fees.
* **One-Time Purchase:** A single fair in-app purchase unlocks the **Lifetime Pro** version forever across all your Android devices (unlimited PVE servers, Proxmox Backup Server, cluster storage config, guest cloning, guest consoles, cluster migrations, and widgets).

---

## 🛠 Tech Stack & Architecture

* **Language:** Kotlin 2.x
* **UI Framework:** Jetpack Compose with Material 3 Design
* **Concurrency:** Kotlin Coroutines & Asynchronous Flow
* **Dependency Injection:** Dagger Hilt
* **Database & Storage:** Android Room Database & Encrypted DataStore
* **Networking & Protocols:** 
  * Retrofit 2 & Moshi for type-safe Proxmox REST API integration
  * OkHttp with custom TLS TrustManager for self-signed certificates
  * JSch for secure, authenticated SSH shell sessions
* **Widget Engine:** AndroidX Glance AppWidget
* **Security:** AndroidX Biometric & Android Keystore

---

## 📥 Download & Installation

### Google Play Store (Recommended)
Get automated updates, background security checks, and simple purchase restoration:

<a href="https://play.google.com/store/apps/details?id=com.pvemanager.proxmox">
  <img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" height="50" alt="Get it on Google Play" />
</a>

### GitHub Releases
Direct standalone APKs are published with each release in the [GitHub Releases](https://github.com/teahache/Proxmox_Manager/releases) tab for de-Googled devices (GrapheneOS, LineageOS, etc.).

---

## 🔒 Security & Privacy

For full details regarding how permissions and data are handled, please review our [Privacy Policy](PRIVACY_POLICY.md).

* **Zero Personal Telemetry:** The app never collects personal information or sends server data to the developer.
* **Optional Diagnostics:** Anonymized crash reports (Firebase Crashlytics) and anonymous telemetry can be completely disabled at any time in the app's **Options** screen.

---

## ⚖️ Legal Disclaimer

**Proxmox®** is a registered trademark of Proxmox Server Solutions GmbH.

*PVE Manager for Proxmox* is an independent third-party mobile application. It is **not** affiliated with, endorsed by, sponsored by, or supported by Proxmox Server Solutions GmbH.

---

## 🤝 Contributing & Feedback

* Found a bug or have a feature request? Please open an [Issue](https://github.com/teahache/Proxmox_Manager/issues).
* Contact the developer directly: [pve_manager@etik.com](mailto:pve_manager@etik.com)

<div align="center">
  <em>Developed with ❤️ for the self-hosted and homelab community.</em>
</div>
