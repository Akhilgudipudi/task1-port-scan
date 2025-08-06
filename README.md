# Task 1: Scan Your Local Network for Open Ports

## Tools Used
- **Nmap 7.97**: Network scanning tool for finding devices and open ports.
- **Operating System**: Windows 10
- **Wireshark**: Not used in this task, but recommended for packet analysis.

---

## Network Configuration

- **Device IP (IPv4)**: `192.168.1.8`
- **Subnet Mask**: `255.255.255.0`
- **Default Gateway**: `192.168.1.1`
- **IP Range Scanned**: Single IP (`192.168.1.8`)

---

## Nmap Command Used

```bash
nmap -sS 192.168.1.8
```
