# Privacy Policy for PVE Manager for Proxmox

**Effective Date: October 23, 2026**

This privacy policy applies to the **PVE Manager for Proxmox** mobile application (hereinafter referred to as the "Application") for Android devices, developed and published by **Nicolas Auzanneau** (SIREN: 108113002, France; hereinafter referred to as the "Developer" or "Service Provider").

---

## 1. Application Scope and Core Architecture

The Application is an independent management and monitoring client designed for **Proxmox Virtual Environment (PVE)** and **Proxmox Backup Server (PBS)** infrastructures. 

The Application operates on a **zero-cloud / zero-middleman architecture**:
* **Direct Communication Only:** All network requests (HTTPS REST API calls and SSH connections) are established directly between your Android device and your own configured Proxmox server(s). The Developer operates no intermediary servers, cloud relays, or proxy services.
* **No Personal Data Collection:** The Application does not require an account or registration with the Developer. We do not collect, sell, or transmit your name, email address, physical location, or contact list.
* **Strictly Local and Encrypted Storage:** All server credentials (URLs, hostnames, ports, usernames, passwords, API tokens) and SSH credentials entered into the Application are stored exclusively on your device in an encrypted local database. Server profile configurations exported for backup are encrypted locally using a password specified by the user. This sensitive information is never transmitted to the Developer or any external third party.

---

## 2. Third-Party Services and Telemetry

The Application integrates a minimal set of industry-standard third-party SDKs:

### A. Google Firebase Analytics & Crashlytics
* **Firebase Analytics:** Collects anonymous, aggregated usage metrics (such as screen views, app session starts, and general device/OS information) to help understand user experience and optimize app performance. No personal identifiers, IP addresses, or Proxmox server data are ever captured. You can disable telemetry at any time in the Application's **Options (Settings)** screen.
* **Firebase Crashlytics:** Collects anonymized technical diagnostic information (crash stack traces, device model, operating system version) to help the Developer identify and resolve application crashes and stability issues.

### B. Google Play Billing
* The Application includes a permanent free tier allowing full management of 1 Proxmox VE server, and offers an optional one-time in-app purchase to unlock the "Pro" lifetime license for unlimited servers and advanced features.
* Payment processing is handled entirely and securely by Google Play. The Developer never receives, stores, or has access to your credit card details, billing address, or payment method credentials. The Developer only receives an anonymous cryptographic receipt token from Google Play to unlock Pro features.

---

## 3. Permissions Requested and Justifications

The Application requests only the permissions strictly necessary for its technical operations:

* **Internet Access (`android.permission.INTERNET`):** Required to connect directly to your Proxmox VE and PBS servers over HTTPS and SSH.
* **Network & Wi-Fi State (`android.permission.ACCESS_NETWORK_STATE`, `android.permission.ACCESS_WIFI_STATE`, `android.permission.ACCESS_LOCAL_NETWORK`):** Used to verify network availability, check Wi-Fi connection status, and communicate with Proxmox instances on your local area network (LAN), including compatibility with Android 15+.
* **Notifications (`android.permission.POST_NOTIFICATIONS`):** Optional permission requested on Android 13+ solely to deliver user-configured background alerts (e.g., node offline alerts, VM status changes, or storage threshold warnings).
* **Vibration (`android.permission.VIBRATE`):** Used for haptic feedback and notification alert patterns.
* **Biometric Authentication (`android.permission.USE_BIOMETRIC`, `android.permission.USE_FINGERPRINT`):** Optional security feature allowing you to lock the Application with your device's fingerprint or face unlock. Biometric validation is handled entirely by the local Android OS security hardware (TEE/Secure Element); no biometric information is ever accessed or stored by the Application.

*(Note: The Application does **not** request or use Camera, Location, Contacts, or Microphone permissions).*

---

## 4. Data Security and User Control (GDPR Compliance)

Because the Application stores all configuration data strictly on your local device:
* **Security:** Data security depends on your device's operating system security. We recommend enabling the Application's built-in biometric lock and maintaining a secure device lockscreen.
* **Data Erasure:** You maintain 100% control over your data. You can delete individual servers, clear credentials, or permanently erase all stored application data at any time either from within the Application or via Android system settings (*Settings > Apps > PVE Manager > Clear Storage / Uninstall*).
* **Opt-Out:** You can toggle anonymous telemetry collection on or off at any moment in the Application's Options screen.

---

## 5. Trademark Disclaimer

**Proxmox®** is a registered trademark of Proxmox Server Solutions GmbH. 
**PVE Manager for Proxmox** is an independent third-party tool and is not affiliated with, endorsed by, sponsored by, or supported by Proxmox Server Solutions GmbH.

---

## 6. Changes to this Policy

This Privacy Policy may be updated periodically. Any updates will be reflected with a revised effective date on this page and within the Application's legal notices.

---

## 7. Contact Us

If you have any questions, concerns, or requests regarding this Privacy Policy or data handling, please contact the developer:

* **Developer:** Nicolas Auzanneau (SIREN: 108113002)
* **Email:** [pve_manager@etik.com](mailto:pve_manager@etik.com)
