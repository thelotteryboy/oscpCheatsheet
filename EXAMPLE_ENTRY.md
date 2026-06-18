# Example Cheat Sheet Entry

This is an example of how to create a cheat sheet entry using the GitHub issue template.

---

## Category
Enumeration

## Technique/Tool Name
Nmap TCP SYN Scan

## Description
Fast, stealthy port scanning technique that sends SYN packets without completing the TCP handshake. Useful for quickly identifying open ports on target systems without being logged by some intrusion detection systems.

## Details

**Prerequisites:**
- Root/Administrator privileges required for SYN scan
- Target IP address or hostname
- Network connectivity to target

**Key Parameters:**
- `-sS` - SYN scan (stealth scan)
- `-p-` - Scan all 65535 ports
- `-T4` - Timing template (0-5, higher is faster)
- `-A` - Aggressive scan (OS detection, version detection, script scanning)
- `-oN` - Normal output to file

**Expected Output:**
- List of open/closed/filtered ports
- Service versions (with `-sV`)
- OS detection results (with `-O` or `-A`)

**Common Variations:**
- Full port scan: `nmap -p- -T4 <target>`
- Version detection: `nmap -sV -p <ports> <target>`
- OS detection: `nmap -O <target>`

## Code/Commands

```bash
# Basic SYN scan of top 1000 ports
sudo nmap -sS <target_ip>

# Full port scan with service detection
sudo nmap -sS -p- -sV -T4 <target_ip>

# Aggressive scan with OS detection
sudo nmap -sS -A -T4 -oN nmap_scan.txt <target_ip>

# Scan specific ports
sudo nmap -sS -p 80,443,8080 <target_ip>

# Scan subnet
sudo nmap -sS 192.168.1.0/24

# Scan with NSE scripts
sudo nmap -sS -sC -sV -p- <target_ip>
```

## Use Cases

1. **Initial Reconnaissance** - Quick identification of open services
2. **Firewall Testing** - Identify filtered vs closed ports
3. **Service Discovery** - Find running services for further enumeration
4. **Network Mapping** - Map out subnet services

## References

- [Nmap Official Documentation](https://nmap.org/book/man.html)
- [OSCP-like Practice: HTB Starting Point](https://www.hackthebox.com/)
- [Nmap NSE Scripts Reference](https://nmap.org/nsedoc/)

## Tags
#enumeration #network #nmap #recon #linux #windows
