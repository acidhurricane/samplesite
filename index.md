# CIS 106 - Linux Fundamentals
# Linux Fundamentals Notes

---

## 1. What is Linux?

- Linux is an open-source, Unix-like operating system.
- Based on the Linux kernel, created by Linus Torvalds in 1991.
- Used in:
  - Servers
  - Cloud infrastructure
  - Supercomputers
  - Embedded systems
  - Desktop environments
  - Android (via modified Linux kernel)

---

## 2. Linux Distributions (Distros)

A Linux distribution bundles the Linux kernel with software and package managers.

Popular distros:
- Ubuntu
- Debian
- Fedora
- CentOS
- Arch Linux

---

## 3. Linux Architecture

```
User Applications
       ↓
Shell
       ↓
Kernel
       ↓
Hardware
```

### Kernel

- Core of the OS
- Manages:
  - CPU
  - Memory
  - Devices
  - File systems
  - Processes

### Shell

- Command-line interface (CLI)
- Acts as an interpreter between user and kernel
- Popular shells:
  - Bash
  - Zsh
  - Sh

---

## 4. Linux File System Structure

Linux uses a hierarchical directory structure starting from root `/`.

| Directory | Purpose |
|------------|----------|
| `/` | Root directory |
| `/home` | User home directories |
| `/root` | Root user home |
| `/etc` | Configuration files |
| `/bin` | Essential user binaries |
| `/sbin` | System binaries |
| `/usr` | User programs |
| `/var` | Variable files (logs, spool) |
| `/tmp` | Temporary files |
| `/dev` | Device files |
| `/proc` | Process & kernel info |

---

## 5. Basic Linux Commands

### File & Directory Commands

```bash
pwd        # Print working directory
ls         # List files
ls -l      # Long listing
cd dir     # Change directory
mkdir dir  # Create directory
rmdir dir  # Remove empty directory
rm file    # Remove file
rm -r dir  # Remove directory recursively
```

---

### File Viewing & Editing

```bash
cat file
less file
head file
tail file
nano file
vi file
```

---

### Search & Filters

```bash
grep "text" file
find /path -name file
locate filename
```

---

## 6. File Permissions

Linux has 3 types of permissions:

- `r` → Read  
- `w` → Write  
- `x` → Execute  

Permission Groups:

- User (u)  
- Group (g)  
- Others (o)  

Example:

```
-rwxr-xr--
```

Change permissions:

```bash
chmod 755 file
chmod u+x script.sh
```

Change ownership:

```bash
chown user file
chgrp group file
```

---

## 7. Package Management

Different distros use different package managers:

- `apt` → Ubuntu / Debian  
- `dnf` → Fedora  
- `yum` → CentOS  
- `pacman` → Arch Linux  

Examples:

```bash
sudo apt update
sudo apt install package_name
sudo dnf install package_name
```

---

## 8. Process Management

View running processes:

```bash
ps
ps aux
top
htop
```

Manage processes:

```bash
kill PID
kill -9 PID
```

- Each process has a PID (Process ID).
- Foreground vs Background processes (`&` to run in background).

---

## 9. Users and Groups

Create user:

```bash
sudo useradd username
```

Set password:

```bash
sudo passwd username
```

Switch user:

```bash
su username
```

Superuser:

```bash
sudo command
```

---

## 10. Networking Basics

Check IP:

```bash
ip a
ifconfig
```

Test connectivity:

```bash
ping google.com
```

Download files:

```bash
wget url
curl url
```

---

## 11. Redirection & Pipes

### Output Redirection

```bash
command > file      # overwrite
command >> file     # append
```

### Input Redirection

```bash
command < file
```

### Pipes

```bash
command1 | command2
```

Example:

```bash
ls -l | grep ".txt"
```

---

## 12. Environment Variables

View variables:

```bash
printenv
echo $PATH
```

Set temporary variable:

```bash
export VAR=value
```

---

## 13. Shell Scripting Basics

Example script:

```bash
#!/bin/bash
echo "Hello, Linux"
```

Make executable:

```bash
chmod +x script.sh
./script.sh
```

---

# Summary

Linux fundamentals include:

- Understanding the Linux architecture  
- Navigating the file system  
- Using basic commands  
- Managing permissions  
- Handling processes  
- Managing packages  
- Basic networking  
- Shell scripting  

