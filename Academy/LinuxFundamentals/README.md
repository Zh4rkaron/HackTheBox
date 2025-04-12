# Linux Fundamentals

**Tags**: `tier 0`, `fundamental`, `general`  
**Sections**: 30  
**Duration**: 6 hours  

## Overview

Linux is an indispensable tool and system in the field of cybersecurity. Many servers run on Linux and offer a wide range of possibilities for offensive security practitioners, network defenders, and systems administrators. This module covers the essentials for starting with the Linux operating system and terminal.

In this module, we will cover:
- Linux structure
- Using the shell
- Navigating the Linux operating system
- Working with files and directories
- Linux administration
- Service management
- Permissions management

---

## Philosophy


| **Philosophy**                                   | **Description**                                                                                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Everything is a file**                         | All configuration files for the various services running on the Linux operating system are stored in one or more text files.                          |
| **Small, single-purpose programs**               | Linux offers many different tools that we will work with, which can be combined to work together.                                                      |
| **Ability to chain programs together**           | The integration and combination of different tools enable us to carry out many large and complex tasks, such as processing or filtering specific data.   |
| **Avoid captive user interface**                | Linux is designed to work mainly with the shell (or terminal), which gives the user greater control over the operating system.                         |
| **Configuration data stored in a text file**     | An example of such a text file is the `/etc/passwd` file, which stores all of the users registered on the system.                                       |

---

## Components

| **Component**             | **Description**                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bootloader**             | A piece of code that runs to guide the booting process to start the operating system. Parrot Linux uses the GRUB bootloader.                                          |
| **OS Kernel**              | The kernel is the main component of an operating system. It manages the resources for the system's I/O devices at the hardware level.                                  |
| **Daemons**                | Background services are called "daemons" in Linux. Their purpose is to ensure that key functions such as scheduling, printing, and multimedia are working correctly. These small programs load after we booted or logged into the computer. |
| **OS Shell**               | The operating system shell or the command language interpreter (also known as the command line) is the interface between the OS and the user. This interface allows the user to tell the OS what to do. The most commonly used shells are bash, Tcsh/csh, Ksh, Zsh, and Fish. |
| **Graphics Server**        | This provides a graphical user interface (GUI). There are many options, including GNOME, KDE, MATE, Unity, and Cinnamon. A desktop environment usually has several applications, including file and web browsers. These allow the user to access and manage the essential and frequently accessed features and services of an operating system. |
| **Utilities**              | Applications or utilities are programs that perform particular functions for the user or another program.                                                            |

---

## Linux Architecture

| **Layer**             | **Description**                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hardware**          | Peripheral devices such as the system's RAM, hard drive, CPU, and others.                                                                                             |
| **Kernel**            | The core of the Linux operating system whose function is to virtualize and control common hardware resources like CPU, allocated memory, accessed data, and others. The kernel gives each process its own virtual resources and prevents/mitigates conflicts between different processes. |
| **Shell**             | A command-line interface (CLI), also known as a shell, that a user can enter commands into to execute the kernel's functions.                                          |
| **System Utility**    | Makes available to the user all of the operating system's functionality.                                                                                              |
## Linux File System Hierarchy

```
/
├── bin/
│   ├── bash
│   └── ls
├── boot/
│   ├── grub/
│   └── vmlinuz
├── dev/
│   ├── sda
│   └── tty
├── etc/
│   ├── passwd
│   └── network/
├── home/
│   ├── user1/
│   └── user2/
├── lib/
│   ├── libc.so
│   └── modules/
├── media/
│   └── usb/
├── mnt/
│   └── data/
├── opt/
│   └── software/
├── proc/
│   ├── cpuinfo
│   └── meminfo
├── root/
│   └── .bashrc
├── run/
│   └── lock/
├── sbin/
│   ├── shutdown
│   └── init
├── srv/
│   └── www/
├── sys/
│   └── fs/
└── usr/
    ├── bin/
    │   ├── python
    │   └── java
    ├── lib/
    └── share/
```
| **Path** | **Description** |
|----------|-----------------|
| **/** | The top-level directory is the root filesystem and contains all of the files required to boot the operating system before other filesystems are mounted, as well as the files required to boot the other filesystems. After boot, all of the other filesystems are mounted at standard mount points as subdirectories of the root. |
| **/bin** | Contains essential command binaries. |
| **/boot** | Consists of the static bootloader, kernel executable, and files required to boot the Linux OS. |
| **/dev** | Contains device files to facilitate access to every hardware device attached to the system. |
| **/etc** | Local system configuration files. Configuration files for installed applications may be saved here as well. |
| **/home** | Each user on the system has a subdirectory here for storage. |
| **/lib** | Shared library files that are required for system boot. |
| **/media** | External removable media devices such as USB drives are mounted here. |
| **/mnt** | Temporary mount point for regular filesystems. |
| **/opt** | Optional files such as third-party tools can be saved here. |
| **/root** | The home directory of the root user. |
| **/sbin** | This directory contains executables used for system administration (binary system files). | 
| **/tmp** | The operating system and many programs use this directory to store temporary files. This directory is generally cleared upon system boot and may be deleted at other times without any warning. |
| **/usr** | Contains executables, libraries, man files, etc. |
| **/var** | This directory contains variable data files such as log files, email inboxes, web application-related files, cron files, and more. |

---

# Linux Distributions

Linux distributions — or distros — are operating systems based on the Linux kernel. They are used for various purposes, from servers and embedded devices to desktop computers and mobile phones.

Linux distributions are like different branches or franchises of the same company, each tailored to serve specific markets or customer preferences. While they all share the same core components and structure (software packages and configurations), each Linux distribution is different, with its own set of features, packages, and tools.

## Common Linux Distributions

- Ubuntu  
- Fedora  
- CentOS  
- Debian  
- Red Hat Enterprise Linux  

Many users choose Linux for desktop use because it is free, open-source, and highly customizable. Ubuntu and Fedora are popular choices for beginners. Linux is also widely used on servers due to its security, stability, and frequent updates.

## Use Cases

Linux distributions are used in a wide variety of environments:

- Web servers  
- Mobile devices  
- Embedded systems  
- Cloud computing  
- Desktop computing  

For cybersecurity specialists, some of the most popular Linux distributions include:

| Distribution       | Notes                          |
|--------------------|--------------------------------|
| ParrotOS           | Security-focused               |
| Ubuntu             | Beginner-friendly, versatile   |
| Debian             | Stable and flexible             |
| Raspberry Pi OS    | Lightweight, for Raspberry Pi  |
| CentOS             | Server-focused (RHEL-based)    |
| BackBox            | Pen-testing tools              |
| BlackArch          | Large number of hacking tools  |
| Pentoo             | Based on Gentoo, security tools|

> **Note:** Kali Linux is the most popular Linux distribution for cybersecurity professionals, offering a wide range of security-focused tools and packages.

---

## Debian

Debian is a widely used and well-respected Linux distribution known for its stability and reliability. It's used for various purposes including desktops, servers, and embedded systems.

- Uses the **APT** (Advanced Package Tool) for package management  
- Known for **long-term support releases** (up to 5 years)  
- Offers flexibility and customization  
- Excellent for **advanced users** who want control over their system  

Debian may have a steeper learning curve, but its strength lies in its rock-solid reliability and wide compatibility with other Linux-based systems.
