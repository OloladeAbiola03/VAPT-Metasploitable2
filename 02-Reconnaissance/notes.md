# Reconnaissance Notes

## 2026-10-27 — Initial Verification

### Target

Metasploitable 2

IP:

`192.168.186.129`

### Host Discovery

Command:

```bash
sudo nmap -sn 192.168.186.129
```

Result:

The target was identified as reachable.

### Initial Port Enumeration

Command:

```bash
sudo nmap -p 22 192.168.186.129
```

Result:

TCP port 22 was open.

### Service Enumeration

Command:

```bash
sudo nmap -sV -p 22 192.168.186.129
```

Result:

```text
22/tcp open ssh OpenSSH 4.7p1 Debian 8ubuntu1
```

### Interpretation

The target exposes an SSH service. The identified OpenSSH version should be investigated further during the vulnerability assessment phase to determine whether it presents a relevant security weakness.

### Next Step

Perform full TCP port enumeration to identify the complete externally accessible service attack surface.
