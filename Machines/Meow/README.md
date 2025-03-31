# Network Enumeration & Service Exploitation  

## Overview  
This repository focuses on learning how to connect to various network services anonymously and use **Nmap** to identify open ports on a target system.  
We will explore the following services:  

- **FTP** (File Transfer Protocol)  
- **SMB** (Server Message Block)  
- **Telnet**  
- **Rsync**  
- **RDP** (Remote Desktop Protocol)  
- **MongoDB**  

Additionally, we will learn how to use **Nmap** for scanning and enumeration.  

---

## Tasks & Solutions  

### Task 1: What does the acronym VM stand for?  
```sh
# Answer:
Virtual Machine
A Virtual Machine (VM) is a software-based computer that runs an operating system and applications just like a physical computer. It is created and managed using a hypervisor (like VirtualBox, VMware, or KVM), which allows multiple VMs to run on a single physical machine.
```
### Task 2: What tool do we use to interact with the operating system via the command line, also known as a console or shell?
```sh
# Answer:
Terminal
A terminal is a command-line interface (CLI) used to interact with an operating system. It allows users to run commands, execute scripts, and manage system processes without a graphical interface.
```
### Task 3: What service do we use to form our VPN connection into HTB Labs?
```sh
# Answer:
Openvpn
OpenVPN is an open-source VPN (Virtual Private Network) protocol and software that provides secure, encrypted connections over the internet. It allows users to create a private network over a public connection, improving security and privacy.
```

###  Task 4: What tool do we use to test our connection to the target with an ICMP echo Request?
```sh
# Answer:
ping
ping is a command-line tool used to test network connectivity between two devices by sending ICMP (Internet Control Message Protocol) echo requests. It checks if a host is reachable and measures the response time.
```

### Task 5: What is the name of the most common tool for finding open ports on a target?
```sh
# Answer:
nmap
Nmap (Network Mapper) is a powerful open-source tool used for network discovery, security auditing, and vulnerability scanning. It helps identify open ports, running services, and operating systems on a target machine or network.
```

### Task 6: What service do we identify on port 23/tcp during our scans?
```sh
# Answer:
telnet
Telnet is a network protocol and command-line tool used to establish a remote connection to another device over port 23. It allows users to access and control a remote system as if they were physically present.
```
### Task 7: What username is able to log into the target over Telnet with a blank password?
```sh
# Answer:
root
root is the superuser or administrator account on Unix-based operating systems like Linux and macOS. It has full control over the system, including access to all files, commands, and settings.
```

### Task 8: Submit the root flag
```sh
# Flag:
b40abdfe23665f766f9c61ecba8a4c19
```
