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
File System Hierarchy

```
/ ├── bin/ │ ├── bash │ └── ls ├── boot/ │ ├── grub/ │ └── vmlinuz ├── dev/ │ ├── sda │ └── tty ├── etc/ │ ├── passwd │ └── network/ ├── home/ │ ├── user1/ │ └── user2/ ├── lib/ │ ├── libc.so │ └── modules/ ├── media/ │ └── usb/ ├── mnt/ │ └── data/ ├── opt/ │ └── software/ ├── proc/ │ ├── cpuinfo │ └── meminfo ├── root/ │ └── .bashrc ├── run/ │ └── lock/ ├── sbin/ │ ├── shutdown │ └── init ├── srv/ │ └── www/ ├── sys/ │ └── fs/ └── usr/ ├── bin/ │ ├── python │ └── java ├── lib/ └── share/
```
