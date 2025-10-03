# Task-1
# Kali Nmap Open Port Scanning — Full Guide & Templates

**Project:** `kali_network_scan.sh` / Nmap examples  
**Author:** Amal S  
**Environment:** Kali Linux (or Debian-based distro)

> ⚠️ **LEGAL:** Only run scans on systems/networks you own or have explicit written permission to test. Unauthorized scanning may be illegal.

---

## Table of Contents
- [Quick Summary](#quick-summary)
- [Prerequisites](#prerequisites)
- [Quick Usage (one-liners)](#quick-usage-one-liners)
- [Recommended Automated Script](#recommended-automated-script)
- [Sanitizing / Hiding IPs Before Committing](#sanitizing--hiding-ips-before-committing)
- [Pre-commit Hook (auto-redact IPs)](#pre-commit-hook-auto-redact-ips)
- [.gitignore Snippet](#gitignore-snippet)
- [Sanitized Example Scan Output](#sanitized-example-scan-output)
- [Report Template (`network_scan_report.md`)](#report-template-network_scan_reportmd)
- [Interpreting Results — Quick Checklist](#interpreting-results---quick-checklist)
- [Safety & Best Practices](#safety--best-practices)
- [License](#license)

---

# Quick Summary
This single Markdown file contains everything you need for local network discovery and open-port scanning using **Nmap** on Kali Linux, plus templates and safeguards to avoid leaking real IP addresses when publishing to GitHub.

---

# Prerequisites
Install required tools (run once):
```bash
sudo apt update
sudo apt install -y nmap arp-scan xsltproc ipcalc
# Optional: masscan for fast port discovery (use with caution)
sudo apt install -y masscan
