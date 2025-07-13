# 🛡️ PackageScan – Unified Vulnerability Scanner for Code, Systems & Containers

**PackageScan** is a fast, modular security scanner built in Go that helps developers and DevOps teams detect vulnerabilities across:

- Application dependencies (Go, Node.js, Python, etc.)
- Hardcoded secrets in source code
- Server configurations and Linux system packages
- Dockerfiles and running container environments

Whether you're building a microservice, maintaining an open-source repo, or deploying production containers — PackageScan helps you stay ahead of security issues before they become risks.

---

## 🔍 What It Does

| Target          | What It Checks                                             |
|------------------|------------------------------------------------------------|
| 🧑‍💻 Application Code | - Vulnerable packages (via CVE APIs)<br>- Unsafe coding patterns<br>- Hardcoded credentials or secrets |
| 🐧 Linux Server     | - Outdated OS packages<br>- Weak SSH config<br>- SUID/SGID binaries<br>- World-writable files |
| 🐳 Containers       | - Insecure base images<br>- Open ports<br>- Dockerfile flags (e.g., `--privileged`) |

---

## ⚙️ Features

- 📦 Dependency scanning (`go.mod`, `package.json`, `requirements.txt`)
- 🔐 Secrets detection via entropy + pattern match
- 🐧 OS-level checks for Ubuntu, Debian, RHEL
- 🐳 Dockerfile analyzer (base image age, risks)
- 📄 Output formats: JSON, Markdown, table (CLI)
- 🧩 Modular design with custom rule plugin support
- 🚀 Lightweight, fast, and easily CI-integrated

---

## 🚀 Quick Start

```bash
# Install from source
go install github.com/yourusername/packagescan@latest

# Run a scan
packagescan scan ./my-project

