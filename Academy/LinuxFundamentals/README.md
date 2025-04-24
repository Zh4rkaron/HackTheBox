# Linux Fundamentals

**Tags**: `tier 0`, `fundamental`, `general`  
**Sections**: 30  
**Duration**: 6 hours  

## Table of Contents

- [Overview](#overview)
- [Philosophy](#philosophy)
- [Components](#components)
- [Linux Architecture](#linux-architecture)
- [Linux File System Hierarchy](#linux-file-system-hierarchy)
- [Linux Distributions](#linux-distributions)
- [Debian](#debian)
- [Introduction to Shell](#introduction-to-shell)
- [Terminal Emulators](#terminal-emulators)
- [Shell](#shell)
- [Bash Prompt and PS1 Customization](#Bash-Prompt-and-PS1-Customization)
- [Common Special Characters for PS1](#Common-Special-Characters-for-PS1)
- [Getting Help](#Getting-help)
- [System Information](#System-Information)
- [logging in via SSH](#logging-in-via-SSH)

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

## Introduction to Shell

Learning how to use the Linux shell is crucial, especially because many servers (such as web servers) run on Linux. Linux is often chosen over Windows for servers due to its stability and lower error rates.

To control these systems effectively, understanding and mastering the shell is essential. The Linux terminal—also called the shell or command line—is a text-based input/output (I/O) interface between users and the system's kernel. You can think of the shell as a text-based GUI, where commands are entered to perform actions like navigating directories, working with files, and retrieving system information—with much more power and flexibility than a traditional graphical interface.

---

## Terminal Emulators

**Terminal emulators** are programs that emulate the function of a physical terminal within a graphical user interface (GUI). They allow the use of text-based programs from a GUI environment.

A **Command-Line Interface (CLI)** can also run multiple "virtual" terminals within a single terminal window—think of it like having multiple reception desks open at once, each ready to send independent instructions to the server.

In short, a terminal serves as an interface to the shell interpreter.

---

## Shell

The most commonly used shell in Linux is the **Bourne-Again SHell (BASH)**, which is part of the GNU project. Anything you can do through the graphical user interface, you can also do through the shell—with more control and efficiency.

The shell enables:
- Faster interaction with programs and system processes  
- Automation of tasks via small or large scripts  
- Greater control over the system

Besides Bash, other available shells include:
- `Tcsh` / `Csh`
- `Ksh`
- `Zsh`
- `Fish` (Friendly Interactive Shell)

Each shell offers unique features and syntax styles, catering to different user preferences and workflows.

---

# Bash Prompt and PS1 Customization

## What is the Bash Prompt?

The Bash prompt is the line of text that appears in the terminal, letting you know that the system is ready to receive commands. By default, it shows useful information such as:

- 👤 Your **username**
- 💻 Your **hostname** (your computer’s name)
- 📁 The **current working directory**

The prompt typically appears like this:

```
<username>@<hostname><current working directory>$
```

For example, if you're in your home directory, you'll see the tilde symbol (`~`) which represents the home folder:

```
daron@linuxbox[~]$
```

- The **`$`** symbol indicates a regular user.
- When logged in as **root**, the prompt changes to use the **`#`** symbol:

```
root@htb[/htb]#
```

---

## The PS1 Variable

The **`PS1`** variable defines the appearance of your command prompt. It acts like a template, and you can configure it to display more than just your username and directory. Common customizations include:

- IP address
- Date and time
- Success or failure of the last command
- Shell name and job count

You can customize your prompt in the `.bashrc` file (usually located in your home directory).

### Example PS1 Format

PS1="\u@\h[\w]\$ "

This results in a prompt like:

```
daron@linuxbox[~/projects]$ 
```

### Common Special Characters for PS1

| Character        | Description                              |
|------------------|------------------------------------------|
| `\u`             | Current username                         |
| `\h`             | Hostname (up to the first `.`)           |
| `\H`             | Full hostname                            |
| `\w`             | Full path of the current directory       |
| `\W`             | Base name of the current directory       |
| `\d`             | Date (e.g., Mon Apr 14)                  |
| `\D{%Y-%m-%d}`   | Custom date format (e.g., 2025-04-12)    |
| `\t`             | Current time (24-hour format, HH:MM:SS)  |
| `\T`             | Current time (12-hour format, HH:MM:SS)  |
| `\@`             | Current time (12-hour format with am/pm) |
| `\s`             | Shell name                               |
| `\j`             | Number of jobs running in background     |
| `\n`             | Newline                                  |
| `\r`             | Carriage return                          |
| `\$`             | `$` for users, `#` for root              |

## Why Customize the Prompt?

Customizing your prompt improves usability and provides helpful, at-a-glance information while working in the terminal. Benefits include:

- 🧠 Quickly identifying which user or system you're on
- 🕐 Seeing timestamps for commands
- ⚠️ Knowing when a command fails
- 🎯 Enhancing productivity and clarity in scripts or logs

---

# Getting Help

Having established a solid foundation in linux's structures,its various distributions, and the purpose of the shell, we're now prepared to put his knowledge into action. We will always stumble across tools whose optional parameters we do not know from memory or tools we have never seen before. Therefore it is vital to know how we can help ourselves get familiar with thouse tools.The first two ways are the man pages and the help functions. It is always a good idea to familize ourselves with the tool we want to try first. We will also learn some possible tricsk with some of the tools that we thought were not possible. In the man pages, we will find the detailed manuals with detailed explanations. 

```
zharkaron@htb[/htb]$ ls

cacrt.der  Documents  Music     Public     Videos
Desktop    Downloads  Pictures  Templates  

```

The **ls** command in Linux and Unix systems is used to list the files and directories within the current folder or any specified directory, allowing you to see what's inside and manage files more effectively. Like most Linux commands, **ls** comes with additional options and features that help you filter or format the output to display exactly what you want.

## Syntax:

``` 
zharkaron@htb[/htb]$ man <tool>
```
Let us have a look at an example and get help for the **ls** command:

## Syntax:
```
zharkaron@htb[/htb]$man ls
```
## Example:
```
LS(1)                            User Commands                           LS(1)

NAME
       ls - list directory contents

SYNOPSIS
       ls [OPTION]... [FILE]...

DESCRIPTION
       List  information  about  the FILEs (the current directory by default).
       Sort entries alphabetically if none of -cftuvSUX nor --sort  is  speci‐
       fied.

       Mandatory  arguments  to  long  options are mandatory for short options
       too.

       -a, --all
              do not ignore entries starting with .

       -A, --almost-all
              do not list implied . and ..

       --author
 Manual page ls(1) line 1 (press h for help or q to quit)
```
Some tools or commands like **curl** provide a short version of help by using **-h** instead **--help:

## Syntax:
```
zharkaron@htb[/htb]$ <tool> --help
```

## Example:

```
zharkaron@htb[/htb]$ ls --help

Usage: ls [OPTION]... [FILE]...
List information about the FILEs (the current directory by default).
Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.

Mandatory arguments to long options are mandatory for short options too.
  -a, --all                  do not ignore entries starting with .
  -A, --almost-all           do not list implied . and ..
      --author               with -l, print the author of each file
  -b, --escape               print C-style escapes for nongraphic characters
      --block-size=SIZE      with -l, scale sizes by SIZE when printing them;
                             e.g., '--block-size=M'; see SIZE format below

  -B, --ignore-backups       do not list implied entries ending with ~
  -c                         with -lt: sort by, and show, ctime (time of last
                             modification of file status information);
                             with -l: show ctime and sort by name;
                             otherwise: sort by ctime, newest first

  -C                         list entries by columns
<SNIP>
```
Some tools or cmmands like **curl** provide a short version of help by using **-h** instead of **--help**:

## Syntax:

```
zharkaron@htb[/htb]$ <tool> -h
```

## Example:

```
zharkaron@htb[/htb]$ curl -h

Usage: curl [options...] <url>
     --abstract-unix-socket <path> Connect via abstract Unix domain socket
     --anyauth       Pick any authentication method
 -a, --append        Append to target file when uploading
     --basic         Use HTTP Basic Authentication
     --cacert <file> CA certificate to verify peer against
     --capath <dir>  CA directory to verify peer against
 -E, --cert <certificate[:password]> Client certificate file and password
<SNIP>
```

As we can see, the results from each other do not differ in this example. Another tool that can be useful in the beginning is **apropos**. Each manual page has a short description available within it. This tool searches the descriptions for instances of a given keyword.

## Syntax:

```
zharkaron@htb[/htb]$ apropos <keyword>
```

## Example:

```
zharkaron@htb[/htb]$ apropos sudo

sudo (8)             - execute a command as another user
sudo.conf (5)        - configuration for sudo front end
sudo_plugin (8)      - Sudo Plugin API
sudo_root (8)        - How to run administrative commands
sudoedit (8)         - execute a command as another user
sudoers (5)          - default sudo security policy plugin
sudoreplay (8)       - replay sudo session logs
visudo (8)           - edit the sudoers file
```

## System Information
Bellow is a list of essential tools to help gather information about system details, processes, network configuration, user/user settings, and directories. It also plays a key role when assessing security configuration, identifiying vulnerabilties, or preventing potential security risks in Linux operating systems.

| Command  | Description                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| whoami   | Displays current username.                                                                                                   |
| id       | Returns users identify                                                                                                       |
| hostname | Sets or prints the name of current host system.                                                                              |
| uname    | Prints basic information about the operating system name and system hardware.                                                |
| pwd      | Returns working directory name.                                                                                              |
| ifconfig | The config utility is used to assign or view in addres to a network interface and/or configure network interface parameters. |
| netstat  | Shows network status.                                                                                                        |
| ss       | Another utility to investigate sockets.                                                                                      |
| ps       | Shows process status.                                                                                                        |
| who      | Displays who is logged in.                                                                                                   |
| env      | Prints environment or sets and executes command.                                                                             |
| lsblk    | Lists block devices.                                                                                                         |
| lsusb    | Lists USB devices.                                                                                                           |
| lsof     | Lists opened files.                                                                                                          |
| lspci    | Lists PCI devices.                                                                                                           |

## logging in via SSH
