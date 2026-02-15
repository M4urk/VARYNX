<p align="center">
  <img src="docs/varynx_logo.svg" width="200" />
</p>

<h1 align="center">VARYNX – Mobile Guardian OS</h1>
<p align="center">A privacy‑first, defensive‑only mobile security platform designed to protect everyday users from modern digital threats.</p>

---

## 🚀 Overview
VARYNX is a mobile guardian system built to defend users from scams, unsafe apps, digital manipulation, and high‑risk interactions.  
It combines a modular Python security engine with a native Android interface to deliver real‑time protection without harvesting personal data.

This is a **closed beta** release focused on UI, architecture, and early user feedback.

---

## 🔐 Core Features
- **Call Protection** – Detects scam‑like call patterns  
- **Message Scanner** – Flags phishing SMS and unsafe links  
- **Crypto Shield** – Identifies risky approvals and high‑gas transactions  
- **Permission Guard** – Detects tap‑jacking overlays  
- **Bluetooth Proximity Scanner** – Identifies unknown nearby devices  
- **Guardian Score Dashboard** – Summarizes device safety  
- **Threat History** – Logs recent security events  
- **Lockdown Mode** – Emergency hardening  
- **Child Mode** – Restricts risky apps and installs  

---

## 🧠 Architecture

### 1. Python Guardian Engine (`/python`)
- Modular threat detectors  
- Background guardian loop  
- Unified scoring system  
- Event logging  
- Bluetooth proximity analysis  
- Crypto risk evaluation  
- Overlay detection  

### 2. Android App (`/android`)
- Kotlin + Android Studio  
- `GuardianService` for background monitoring  
- 15+ screens  
- Black + blue gradient UI  
- Real‑time dashboard  
- User controls and toggles  

---

## 📁 Repository Structure

```text
VARYNX/
│
├── README.md
├── LICENSE
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
│
├── android/        # Android Studio project
├── python/         # Guardian engine (Python)
├── docs/           # Documentation + logo
│   ├── overview.md
│   ├── architecture.md
│   ├── modules.md
│   ├── roadmap.md
│   ├── privacy.md
│   └── varynx_logo.svg
└── screenshots/    # UI screenshots
