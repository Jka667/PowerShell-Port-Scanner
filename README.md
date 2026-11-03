# PowerShell Port Scanner

TCP port scanner in PowerShell, with no external tools: parallel jobs, connection timeouts and a summary at the end.

## Skills demonstrated
- PowerShell: parameters, background jobs, `System.Net.Sockets.TcpClient` with async connect and timeout
- Network service discovery (ATT&CK T1046)

## Value for an employer
- Works on locked-down Windows hosts where nmap cannot be installed
- Useful for firewall rule checks and exposure reviews (RDP 3389, SMB 445, etc.)

## Quick start
```powershell
.\port-scanner.ps1                                          # interactive, default common ports
.\port-scanner.ps1 -target 192.168.1.10 -startPort 1 -endPort 100
```
Default ports: 21, 22, 25, 53, 80, 110, 143, 443, 445, 3389.

> Scan only systems you own or are authorized to test.
