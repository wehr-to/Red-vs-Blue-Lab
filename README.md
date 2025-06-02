# 🥊 Red vs Blue Lab

This repo simulates small, CTF-style attack-defense labs to help me sharpen my skills across the full security loop: **exploitation → detection → response**.

Each lab starts with a vulnerable setup (Red), captures telemetry (Logs), and ends with a detection or hardening response (Blue). These aren't just games — they're practical, repeatable exercises to close real-world security gaps.

## 🎯 Why This Exists

Most security roles require more than knowledge — they require *proof of understanding*. This lab structure forces me to:

- Simulate real attacker behavior
- Collect and analyze logs
- Build detection or hardening steps based on the findings

It’s hands-on, forensic, and forces me to think like both sides.

## 🧪 Lab Format

Each lab follows this structure:
labs/
└── exposed-admin-portal/
├── red-setup.md # Vulnerability setup & attacker walkthrough
├── blue-response.md # Detection rule or mitigation
├── logs/ # Captured logs (Sysmon, Wazuh, auditd, etc.)
├── tools-used.md # Commands, payloads, scanning methods
└── summary.md # What I learned + MITRE mappings

## 📘 Labs Included

| Lab Name                   | Red Tactic                         | Blue Response                                  |
|----------------------------|------------------------------------|------------------------------------------------|
| `exposed-admin-portal`     | Web-based unauth access            | Wazuh rule + access log detection              |
| `brute-force-auth`         | Credential stuffing                | Sysmon alert + account lockout policy          |
| `dns-exfiltration-lab`     | DNS tunneling via `dig`            | Suricata/Splunk rule on suspicious domain freq |
| `powershell-spawn-child`   | Scripted process injection         | Sysmon detection on parent-child process tree  |
| `linux-suid-priv-esc`      | Exploiting SUID misconfigs         | Auditd rule + hardening                        |

## 🧠 Goals & Learning Outcomes

- Practice safe exploitation in controlled labs
- Capture logs from Wazuh, Sysmon, Suricata, auditd, etc.
- Build meaningful detection rules (not just noisy alerts)
- Map tactics to MITRE ATT&CK
- Improve Blue Team thinking by walking through Red Team shoes

## 🔐 Who Should Use This

- Junior SOC analysts training detection instincts
- Aspiring security engineers building a Blue Team portfolio
- Students preparing for CTFs or job interviews
- Blue Teamers who want hands-on attacker simulations

## 🔧 Tools You’ll See

- Wazuh / Auditd / Sysmon
- Suricata / Zeek / Wireshark
- Docker-based vuln stacks (DVWA, Juice Shop)
- `dig`, `curl`, `hydra`, and basic scripting tools

## 🚧 Disclaimer

All labs are run in isolated environments (e.g., local VMs or containers). These are educational simulations — **do not replicate in a production network** or on any systems you don’t own or control.


