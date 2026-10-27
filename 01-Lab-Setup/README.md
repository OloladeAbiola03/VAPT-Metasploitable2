# 01 — Lab Setup and Connectivity

## Objective

The objective of this phase was to deploy the intentionally vulnerable Metasploitable 2 virtual machine, configure the VMware networking environment, and establish communication between Kali Linux and the target.

## Lab Configuration

| Machine | IP Address |
|---|---|
| Kali Linux | 192.168.182.129 |
| Metasploitable 2 | 192.168.186.129 |

## Target Configuration

Metasploitable 2 was deployed locally in VMware and configured as the target system for the authorized VAPT assessment.

The target was started successfully and its network configuration was verified using:

```bash
ifconfig
```

## Connectivity Verification

Connectivity from Kali Linux to the target was tested using:

```bash
ping -c 4 192.168.186.129
```

The test returned four successful responses with 0% packet loss.

## Initial Service Verification

A preliminary Nmap scan was performed against TCP port 22:

```bash
sudo nmap -p 22 192.168.186.129
```

The scan identified TCP port 22 as open.

Service/version detection was subsequently performed using:

```bash
sudo nmap -sV -p 22 192.168.186.129
```

The result identified:

```text
22/tcp open ssh OpenSSH 4.7p1 Debian 8ubuntu1
```

## Evidence

Screenshots documenting the IP configuration and connectivity verification are stored in the `screenshots/` directory.

## Status

Lab deployment and initial connectivity verification completed.
