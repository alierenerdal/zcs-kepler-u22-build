# Zimbra ZCS 9.0.0 — Ubuntu 22 Installer Bundle

![release](https://img.shields.io/badge/release-9.0.0-blue)
![platform](https://img.shields.io/badge/platform-Ubuntu%2022-orange)
![package](https://img.shields.io/badge/package-deb-green)
![license](https://img.shields.io/badge/license-FOSS-lightgrey)
![downloads](https://img.shields.io/github/downloads/REPO_OWNER/REPO_NAME/total)

---

## 📦 Overview

This repository contains a **self-built Zimbra Collaboration Suite 9.0.0 installer bundle**
targeting:

> **Ubuntu 22.04 LTS (Debian package format)**

The archive includes all required `.deb` packages and installer scripts.

This repo is provided **as-is** for reproducible builds and educational use.

---

## 🧱 System Architecture

```
+---------------------------+
|        Internet           |
+------------+--------------+
             |
             v
+---------------------------+
|        NGINX Proxy        |
+------------+--------------+
             |
             v
+---------------------------+
|       Zimbra Core         |
|  Mailbox + LDAP + MTA     |
+------------+--------------+
             |
             v
+---------------------------+
|      Storage Backend      |
|     Local / NFS / SAN     |
+---------------------------+
```

---

## 🖥 Multi-Server Topology

```
LDAP Server
    |
Mailbox Server ---- Proxy Server ---- Internet
    |
MTA Server
```

Supports scalable enterprise deployment.

---

## 🚀 Installation Guide

### Step 1 — Extract

```bash
tar -xzf zcs-9.0.0_GA_XXXX.UBUNTU22_64.tgz
cd zcs-9.0.0*
```

### Step 2 — Run installer

```bash
sudo ./install.sh
```

Follow interactive prompts.

---

## 📸 Install Screenshots

> Replace these with real screenshots

```
docs/screenshots/install-1.png
docs/screenshots/install-2.png
docs/screenshots/setup-complete.png
```

---

## 🔄 Upgrade Guide

### From previous Zimbra version

1. Backup mailbox
2. Stop services:

```bash
zmcontrol stop
```

3. Run installer
4. Start services:

```bash
zmcontrol start
```

---

## 🐳 Docker Install Guide

> Experimental

```bash
docker run -it \
  -p 25:25 -p 80:80 -p 443:443 \
  zimbra/zcs:9.0.0
```

Production deployment should use VM or bare metal.

---

## 🛠 Troubleshooting

### Installer fails

```
/tmp/install.log
/var/log/zimbra.log
```

### Service not starting

```bash
zmcontrol status
```

### Rebuild configs

```bash
zmsetup.pl
```

---

## ❓ FAQ

**Q: Is this official?**
A: No. Community build.

**Q: Supported OS?**
A: Ubuntu 22.04 only.

**Q: Production safe?**
A: Test before deploying.

---

## 📊 Download Counter

GitHub releases automatically track download stats.

---

## ⚙ GitHub Actions Build Pipeline

`.github/workflows/build.yml`

```yaml
name: ZCS Build

on:
  push:
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-22.04
    steps:
      - uses: actions/checkout@v3
      - name: Build
        run: |
          echo "Trigger external build system"
```

---

## 📜 License

Zimbra FOSS license applies.

---

## ❤️ Credits

Built using Zimbra Open Source build tools.

---

## ⚠ Disclaimer

Use at your own risk.
Not affiliated with Synacor or Zimbra Inc.

---
