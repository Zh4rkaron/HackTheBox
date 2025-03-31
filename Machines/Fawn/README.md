# Network Enumeration & Service Exploitation  

## Overview  
This machine focuses on learning how to connect to various network services anonymously and use **Nmap** to identify open ports on a target system.  
We will explore the following services:  

- **FTP**  

Additionally, we will learn how to use **Nmap** for scanning and enumeration.  

## Tags

- **FTP**
- **Protocols**
- **Reconnaissance**
- **Anonymous/Guest Access**

---

## Tasks & Solutions  

### Task 1: What does the 3-letter acronym FTP stand for?
```sh
# Answer:
File Transfer Protocol
FTP (File Transfer Protocol) is a standard network protocol used to transfer files between a client and a server over a TCP/IP network. It allows users to upload, download, delete, and manage files remotely on a server. FTP operates over two separate channels: a command channel and a data channel.
```
### Task 2: Which port does the FTP service listen on usually?
```sh
# Answer:
21
Port 21 is the default port used by the File Transfer Protocol (FTP) for the command/control channel. This is where FTP clients and FTP servers communicate to establish the session, exchange commands, and set up file transfer parameters.
```
### Task 3: FTP sends data in the clear, without any encryption. What acronym is used for a later protocol designed to provide similar functionality to FTP but securely, as an extension of the SSH protocol? 
```sh
# Answer:
SFTP
SFTP (Secure File Transfer Protocol) is a network protocol that allows for secure file transfer between a client and a server. It is based on SSH (Secure Shell), which is widely used for encrypted remote communication. SFTP ensures that both the commands and file data are transmitted securely over the network.
```

###  Task 4: What is the command we can use to send an ICMP echo request to test our connection to the target?
```sh
# Answer:
ping
ping is a command-line tool used to test network connectivity between two devices by sending ICMP (Internet Control Message Protocol) echo requests. It checks if a host is reachable and measures the response time.
```

### Task 5: From your scans, what version is FTP running on the target? 
```sh
# Answer:
 vsftpd 3.0.3
To quickly find the version of a service running on a target using Nmap, you can use the -sV option, which enables version detection.
```

### Task 6: From your scans, what OS type is running on the target? 
```sh
# Answer:
unix
To find the operating system (OS) of a target machine, you can use Nmap with the -O option, which performs OS detection.
```
### Task 7: What is the command we need to run in order to display the 'ftp' client help menu? 
```sh
# Answer:
ftp -?
The ftp -? command is used to display the help information or usage guide for the FTP client on many systems. When you run this command in a terminal or command prompt, it shows a list of available options, commands, and how to use the FTP program.
```

### Task 8: What is username that is used FTP when you want to log in without having an account?
```sh
# Answer:
anonymous
In FTP (File Transfer Protocol), anonymous refers to an anonymous FTP account that allows users to access files on a server without requiring them to provide a username or password.
```

### Task 9: What is the response code we get for the FTP message 'login succesfull?
```sh
# Answer:
230
230 is a successful completion code indicating that the client has successfully logged into the FTP server.
```

### Task 10:  There are a couple of commands we can use to list the files and directories available on the FTP server. One is dir. What is the other that is a common way to list files on a Linux system. 
```sh
# Answer:
ls
The ls command is used in Unix-like operating systems (such as Linux and macOS) to list directory contents. It is one of the most commonly used commands for interacting with the filesystem, providing information about files and directories within the current working directory or a specified directory.
```
### Task 11: What is the command used to download the file we found on the FTP server?
```sh
# answer:
get
The get command is used in FTP (File Transfer Protocol) and SFTP (Secure FTP) to download files from a remote server to your local machine. It is one of the most common commands for retrieving files from a server during an FTP or SFTP session.
```

### Submit Root Flag
```sh
# Flag
035db21c881520061c53e0536e44f815
