<div align="center">

# 🛡️ Cyber Attack Simulation Suite

### Interactive, Front-End Security Awareness & Training Platform

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![Made with HTML/CSS/JS](https://img.shields.io/badge/stack-HTML%20%7C%20CSS%20%7C%20JS-blue.svg)]()
[![Purpose](https://img.shields.io/badge/purpose-education%20%26%20awareness-critical.svg)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)

*A curated collection of static, browser-based simulations that recreate the visual and behavioral patterns of real-world cyber attacks - built to train, educate, and raise awareness, without any real-world risk.*

[Overview](#-overview) • [Simulations](#-simulations-included) • [Architecture](#-architecture) • [Getting Started](#-getting-started) • [Security Model](#-security-model) • [Ethics](#️-ethical-use--disclaimer)

</div>

---

> ⚠️ **Disclaimer:** These pages are non-functional mockups. They do not collect, store, or transmit any real credentials or personal data, and they are not connected to any backend, database, or third-party service. This repository must not be used to deceive real users, to impersonate real organizations, or for any unauthorized or illegal activity. See [Ethical Use & Disclaimer](#️-ethical-use--disclaimer) below.

---

## 📖 Overview

This repository showcases interactive, front-end-only recreations of attack scenarios that security teams commonly use to train employees on how to recognize threats. Each simulation is a self-contained HTML page that visually mimics a real-world attack vector without performing any actual malicious action.

Typical use cases:
- Security awareness training demos
- Classroom / workshop teaching aids
- Portfolio pieces demonstrating front-end and security-concept skills
- UI/UX reference for building real phishing-awareness platforms

## 🏗️ Architecture

The suite follows a **static, client-only architecture** - a deliberate design choice that removes any possibility of real data capture or transmission.

```
┌──────────────────────────────────────────────────────┐
│                     Browser (Client)                 │
│                                                      │
│   ┌───────────────┐    ┌───────────────┐             │
│   │  index.html   │───▶│  Simulation   │            │
│   │ (launch page) │    │    Pages      │             │
│   └───────────────┘    └───────┬───────┘             │
│                                 │                    │
│                         ┌───────▼───────┐            │
│                         │  Local JS     │            │
│                         │  (UI logic,   │            │
│                         │  no network   │            │
│                         │  calls)       │            │
│                         └───────────────┘            │
│                                                      │
│     ❌ No server   ❌ No database   ❌ No API      │
└──────────────────────────────────────────────────────┘
```

**Design principles:**
- **Zero data persistence** - no `localStorage`, cookies, or form submission endpoints capture input.
- **Sandboxed by design**  - simulation is a self-contained page with no cross-origin requests.
- **Framework-free** - dependency-free vanilla JS keeps the codebase auditable line-by-line.
- **Fidelity for training value** - visual accuracy is prioritized so trainees learn to spot *real* red flags (spoofed domains, urgency cues, mismatched branding).

## 🛠️ Tech Stack

| Layer | Technology | Purpose |
|---|---|---|
| Structure | HTML5 | Semantic, accessible markup |
| Styling | CSS3 (Flexbox/Grid) | Responsive, pixel-accurate UI recreation |
| Behavior | Vanilla JavaScript (ES6+) | Interactivity without external dependencies |
| Tooling | Git / GitHub Pages (optional) | Version control & static hosting for demos |

> No frameworks, no build pipeline, and no backend - reducing the attack surface of the simulation platform itself to effectively zero.

## 📁 Project Structure

```
cyber-attack-simulation/
├── Simulations/
│   ├── <attack-name-1>/
│   │   └── index.html
│   ├── <attack-name-1>/
│   │   └── index.html
│   └── ...
└── README.md
```

## 🚀 Getting Started

Clone the repository and open any simulation directly in your browser - no build step or server required.

```bash
git clone https://github.com/Janiru-Sudasinghe/Cyber-Attack-Simulation-Suite.git
cd Cyber-Attack-Simulation-Suite
```

Then simply open the desired HTML file in your browser, e.g.:

```bash
open Simulations/<attack-name>/index.html
```

Optionally, serve it locally for a more realistic experience:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000` in your browser.

## 🧭 How to Use These Simulations

1. Present the simulation in a controlled training or classroom environment.
2. Walk through the visual cues that would normally indicate a phishing or social-engineering attempt (mismatched URLs, urgency language, spoofed branding, etc.).
3. Use the discussion points below (or your own) to reinforce awareness.

### Discussion Points (customize per simulation)
- What details give away that this is not the real site/email?
- What should a user do if they encounter this in real life?
- What organizational policies apply here (e.g., reporting phishing)?

## 🖼️ Screenshots

*(Add screenshots or GIFs of each simulation here once uploaded.)*

## ⚖️ Ethical Use & Disclaimer

This project is provided **strictly for educational and awareness purposes**. By using this repository, you agree that you will:

- **Not** deploy these simulations against real users without their informed consent (e.g., through an authorized internal phishing-awareness campaign).
- **Not** use any part of this code to build tools intended to deceive, defraud, or harm others.
- **Not** host these pages on domains designed to impersonate real organizations.
- Use this project only within legal and ethical boundaries, such as internal security training approved by your organization.

The author(s) of this repository assume no liability for misuse of this code.

## 🔒 Security Model

Because this repository simulates attacks, it is held to a *higher* security bar than a typical static site:

- **No outbound network calls** - simulations must not `fetch()`, submit forms to, or load scripts from third-party or attacker-controlled domains.
- **No credential capture** - any "login" or "input" field is cosmetic; submitted values are never stored, logged, or transmitted, and are cleared from memory after use.
- **No real branding impersonation** - logos, names, and domains used in simulations are fictional or clearly marked as illustrative, avoiding trademark or brand-impersonation concerns.
- **Isolated execution** - each simulation runs independently, so no simulation can affect another or the host page.
- **Static analysis before merge** - contributions are reviewed for unintended network requests, tracking scripts, or obfuscated code prior to acceptance.

If you discover a way a simulation could be misused beyond its intended training context, please open a private security advisory rather than a public issue.

## ✅ Testing & Quality Assurance

| Check | Tool / Method | Status |
|---|---|---|
| HTML validation | [W3C Validator](https://validator.w3.org/) | 🔲 |
| Accessibility (a11y) | Lighthouse / axe | 🔲 |
| Cross-browser rendering | Chrome, Firefox, Safari, Edge | 🔲 |
| No external network calls | Manual review / DevTools Network tab | 🔲 |
| Responsive layout | Mobile, tablet, desktop breakpoints | 🔲 |

*(Check off items as each simulation passes review.)*

## 📄 License

This project is licensed under the [MIT License](LICENSE) - feel free to use and adapt it for your own security awareness initiatives, subject to the ethical use terms above.

## 👤 Author

**Janiru Sudasinghe**   
[GitHub](https://github.com/Janiru-Sudasinghe) • [LinkedIn](https://www.linkedin.com/in/janiru-sudasinghe-7182b7186/) 

---

*Built for the security community - help people recognize attacks before they happen.*
