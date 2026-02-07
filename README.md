# Zimbra ZCS 9 KEPLER Ubuntu 22 Build

![Build](https://img.shields.io/github/actions/workflow/status/alierenerdal/zcs-kepler-u22-build/build.yml)
![Release](https://img.shields.io/github/v/release/alierenerdal/zcs-kepler-u22-build)
![Downloads](https://img.shields.io/github/downloads/alierenerdal/zcs-kepler-u22-build/total)
![License](https://img.shields.io/badge/license-FOSS-blue)

Official Zimbra Collaboration Suite 9 (KEPLER) Ubuntu 22 custom build bundle.

---

## 📦 Download

👉 **Latest Release:**  
https://github.com/alierenerdal/zcs-kepler-u22-build/releases/latest

---

## 🧱 System Architecture

![Architecture Diagram](docs/architecture.png)

ZCS multi-layer architecture:

- LDAP
- Mailbox
- Proxy
- MTA
- Logger
- SNMP
- Web client

Supports:

- Single server
- Multi-server topology
- Horizontal scaling

---

## 🖥 Install Guide

```bash
tar -xzf zcs-9.0.0_GA_1013.UBUNTU22_64.20260207114844.tgz
cd zcs-9.0.0*
./install.sh
```

Follow interactive installer.

Screenshots:

![Install Step](screenshots/install/step1.png)

---

## 🔁 Upgrade Guide

See:

👉 docs/upgrade-guide.md

Supports upgrade from:

- ZCS 8.8.x
- ZCS 9 GA
- ZCS KEPLER builds

---

## 🧩 Multi-Server Topology

See:

👉 docs/architecture.md

Includes:

- LDAP master/replica
- Proxy tier
- Mailbox cluster
- MTA pool

---

## 🐳 Docker Install (Experimental)

```bash
cd docker
docker compose up -d
```

Template only. Production requires tuning.

---

## 🛠 Troubleshooting

Common issues covered:

- LDAP sync errors
- Postfix queue stuck
- Proxy TLS mismatch
- Java memory tuning
- Mailbox corruption recovery

👉 docs/troubleshooting.md

---

## ❓ FAQ

👉 docs/faq.md

Includes:

- Supported OS?
- RAM requirements?
- Backup strategy?
- Migration paths?
- License questions?

---

## 📊 Analytics

GitHub traffic analytics enabled.

Optional:

Add Plausible / GA badge here.

---

## 🔧 CI Pipeline

GitHub Actions pipeline:

- Build verification
- Release packaging
- GitHub Pages deployment
- Artifact validation

---

## 📄 Release Notes

Template:

👉 RELEASE_TEMPLATE.md

---

## 📜 License

Zimbra FOSS components.

See upstream licensing.

---

## ❤️ Maintainer

Ali Eren Erdal  
https://seonedir.co
