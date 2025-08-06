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
Scan Results  
Port        State         Service  
135/tcp     open         msrpc  
139/tcp     open         netbios-ssn  
445/tcp     open         microsoft-ds  
8090/tcp    open         opsmessaging  
49152/tcp   open         unknown  

NOTE: 995 TCP ports were closed (reset).  

Security Findings  
Ports 135, 139, 445 (used for Windows networking and file sharing):  

These ports are often targeted by malware and attackers, like WannaCry.  

They should be firewalled or turned off if not needed.  

Port 8090 (opsmessaging):  

This port might be connected to software running locally, such as development tools or remote services.  

Make sure it’s secured or not available to the public.  

Port 49152 (unknown):  

This is likely a dynamic or private port.  

It needs more investigation to figure out the service.  

Conclusion  :-
This scan showed how to find open ports and understand basic network exposure. Some detected services, like NetBIOS and SMB, could be risky if not properly secured, especially on public or shared networks.
