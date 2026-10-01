# Cyber Security Internship - Task 1

## Scan Local Network for Open Ports

### Objective

The objective of this task was to perform basic network reconnaissance by identifying active devices and open TCP ports on my local network using Nmap.

### Tools Used

- Nmap 7.991
- Windows Command Prompt
- Notepad

### Network Information

- Local Network: `192.168.0.0/24`
- Subnet Mask: `255.255.255.0`
- Scan Type: TCP SYN Scan

### Command Used

```bash
nmap -sS 192.168.0.0/24
The scan results were saved using:

```bash
nmap -sS 192.168.0.1 192.168.0.101 192.168.0.110 -oN scan-results.txt
### Scan Results

The scan identified 3 active hosts.

| IP Address | Open Ports | Services |
|---|---|---|
| 192.168.0.1 | 22, 53, 80, 1900 | SSH, DNS, HTTP, UPnP |
| 192.168.0.101 | 80, 10000 | HTTP, snet-sensor-mgmt |
| 192.168.0.110 | 135, 139, 445 | MSRPC, NetBIOS-SSN, Microsoft-DS |

### Security Observations

Open ports indicate that network services are accessible on the corresponding devices.

- Unnecessary services should be disabled.
- Remote administration services such as SSH should be properly secured.
- Windows networking ports such as 139 and 445 should be restricted where they are not required.
- HTTP services should be properly configured and secured.
- UPnP should only be enabled when required.

An open port does not by itself prove that a device is vulnerable. Further assessment would be required to determine whether a service is securely configured.

### Result

The Nmap scan successfully discovered 3 active hosts on the local network and identified their open TCP ports and associated services.

### Conclusion

This task provided practical experience with network reconnaissance, IP ranges, TCP SYN scanning, open ports, and network service exposure using Nmap.

## Evidence

The repository contains the Nmap scan results and supporting screenshots from the task.
