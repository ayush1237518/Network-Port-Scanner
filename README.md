# 🛡️ Cyber Port Scanner

A professional, multithreaded **TCP port scanner** with a modern JavaFX desktop GUI, built in Java 21. Designed as a cybersecurity project demonstrating clean architecture, concurrency, and secure coding practices.

> ⚠️ **Ethical use only.** Only scan hosts and networks you own or have explicit written permission to test. Unauthorized port scanning may violate laws such as the U.S. Computer Fraud and Abuse Act or equivalent legislation in your jurisdiction.

---

## 📖 Project Overview

Network Port Scanner lets you scan a single IPv4 address or hostname across a configurable port range, using a pool of concurrent worker threads for high-speed results. It classifies each port as **Open**, **Closed**, or **Filtered**, identifies likely services by port number, and — for open ports — attempts safe banner grabbing to reveal service version information. Results can be exported to **CSV**, **JSON**, or **TXT** for reporting.

The project is organized around SOLID principles with a clear separation between scanning logic, service detection, export strategies, input validation, and the UI layer, making it easy to extend or test in isolation.

---

## ✨ Features

- Scan any IPv4 address or hostname with DNS resolution
- Configurable start port, end port, timeout, and thread count
- Full input validation with friendly error messages
- Multithreaded scanning via `ExecutorService` for high performance
- Port classification: **Open / Closed / Filtered / Error**
- Service name identification for 25+ well-known ports (HTTP, HTTPS, SSH, FTP, SMTP, DNS, MySQL, PostgreSQL, Telnet, POP3, IMAP, RDP, SMB, MongoDB, Redis, and more)
- Safe, non-crashing banner grabbing on open ports
- Live progress tracking: percentage complete, ports scanned/remaining, elapsed time, and estimated time remaining
- Full scan summary statistics on completion
- Export reports to **CSV**, **JSON**, and **TXT** — no database required
- Modern dark cybersecurity-themed JavaFX GUI with blue neon accents
- Live-filterable, sortable results table
- Real-time activity log panel
- Keyboard shortcuts, tooltips, and animated progress bar
- Safe scan cancellation mid-run

---

## 🖥️ Usage

1. Enter a **target** — an IPv4 address (e.g. `192.168.1.1`) or hostname (e.g. `example.com`).
2. Set the **start port** and **end port** for the scan range.
3. Configure the **timeout** (in milliseconds) and **thread count** for performance tuning.
4. Optionally enable **banner grabbing** to attempt reading service banners.
5. Click **Start Scan** (or press `Ctrl+Enter`).
6. Watch live progress — percentage, ports scanned, elapsed/remaining time — in the sidebar.
7. Use the **search box** to filter results, or click column headers to sort.
8. Click **Export** to save a report as CSV, JSON, or TXT.
9. Use **Stop Scan** (`Esc`) to cancel safely at any time.

### ⌨️ Keyboard Shortcuts
| Shortcut       | Action           |
|----------------|------------------|
| `Ctrl + Enter` | Start scan       |
| `Esc`          | Stop scan        |
| `Ctrl + L`     | Clear results    |
| `Ctrl + F`     | Focus filter box |


---

## 🔒 Security & Ethical Notes

- The scanner performs only **standard TCP connect scans** — no raw sockets, no packet spoofing, no exploitation payloads.
- No credentials, exploits, or attack payloads are included anywhere in this codebase.
- Always obtain authorization before scanning any network you do not own.

---


## 📄 License

This project is licensed under the [MIT License](LICENSE).


Live Demo - https://ayush1237518.github.io/Cyber-Port-Scanner/
