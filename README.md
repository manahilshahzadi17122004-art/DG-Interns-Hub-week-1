
### 2. Lab Setup
| VM | Hypervisor | Network | IP | Gateway |
| :--- | :--- | :--- | :--- | :--- |
| Parrot Security 7.2 (used in place of Kali) | VMware Workstation | NAT | 192.168.32.128/24 (ens33) | 192.168.32.2 |
| Ubuntu 26.04.1 | VirtualBox | NAT | 10.0.2.15/24 (enp0s3) | 10.0.2.2 |

> A clean snapshot named `Clean` was taken for each VM. Screenshots are in `Findings/Lab Setup`.

### 3. Linux Practice
Performed on Parrot (all commands in `Findings/Linux Practice`)

- **3 users:** alice, bob, carol
- **2 groups:** devteam (alice, bob) and analysts (carol)
- **Shared folder:** `/srv/shared` , owner root, group devteam, mode `2770` (drwxrws---)
- **Test:** alice and bob can create files; carol gets Permission denied.
- **Commands used:** `find /etc -name "*.conf"`, `grep "root" /etc/passwd`, `ps aux`, `sudo ss -tulpn`
- **Cron job:** `* * * * * echo "hello $(date)" >> /tmp/cron.log`

### 4. Network Map
Recorded with `ip a`, `ip route`, `cat /etc/resolv.conf`, `ping`, `traceroute`, `nslookup / dig` on both VMs.

- Parrot (VMware): 192.168.32.128 | Gateway 192.168.32.2
- Ubuntu (VirtualBox): 10.0.2.15 | Gateway 10.0.2.2 | DNS 127.0.0.53

> Diagram (draw.io) is in `Findings/Network Map` as PNG and .drawio. Two VMs run on different hypervisors, each reaches internet via its own NAT.

### 5. Cheat Sheet
Table "Linux Command - What It Does - When to Use It" with 42 entries is in the `Cheat Sheet` folder.

### 6. Notes (Theory)
Eight separate files covering:
- Cybersecurity and CIA triad
- SOC vs VAPT vs Incident Responder
- OSI vs TCP/IP
- IP / MAC / DNS / DHCP and Ports
- Linux file system and permissions
- Threat / Vulnerability / Risk / Exploit
- VM networking modes
- Legal and ethical basics

### 7. TryHackMe Writeups - Completed (100%)
1. Search Skills
2. Learning Cyber Security
3. Linux Fundamentals Part 1
4. What is Networking?
5. Introductory Networking
6. Networking Concepts
7. Pyramid of Pain
8. Intro to LAN
9. Bonus - Defensive Security Intro

### 8. OverTheWire Bandit (levels 0-10)
Writeups and screenshots in `Writeups` and `Findings/Over the Wire Bandit`. Passwords not included.

### 9. Key Learnings
- How to build a small home lab with two VMs and read their network settings
- Managing users, groups and permissions in Linux, including setgid bit on shared folders
- How IP, gateway and DNS fit together
- The OSI and TCP/IP models and TCP vs UDP
- How defenders think (Pyramid of Pain, SOC work)

---
**Thanks DG Interns Hub**
