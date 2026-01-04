
# Introduction to Linux

Welcome to the start of our Linux journey 

In this section, we’re laying the foundation: what Linux is, where it came from, why it runs half the internet, and how it actually works under the hood. No wizardry, no gatekeeping just clear concepts that’ll make everything else easier later.

If cybersecurity had a home turf, Linux would be it.

---

## What is Linux?

Linux is a **Unix-like, open-source, and free operating system kernel** created by Linus Torvalds in 1991. What started as a personal hobby project somehow turned into one of the largest collaborative software projects in human history. Casual flex.

Technically speaking, **Linux is just the kernel** the core component that talks directly to the hardware. But in everyday life, when people say “Linux,” they usually mean the entire operating system built around it, commonly referred to as **GNU/Linux**.

Linux powers:

- 100% of the world’s supercomputers
    
- Most servers on the internet
    
- Android smartphones
    
- Network devices
    
- Even systems running on the International Space Station 
    

Its stability, security, and modular design make it a favorite for developers, system administrators, and security professionals.

---

## Linux vs Windows 

To understand Linux better, it helps to compare it with Windows the most widely used desktop operating system.

|Feature|Linux|Windows|
|---|---|---|
|Source Code|Open-source. Anyone can view and modify it.|Closed-source. Owned by Microsoft.|
|License|Generally free (GPL).|Requires a paid license.|
|File System|Single root (`/`) with a hierarchical structure.|Uses drive letters (`C:\`, `D:\`).|
|User Interface|Optional. Multiple desktop environments (GNOME, KDE, etc.).|Standard built-in interface.|
|Security|Strong permission model, fewer viruses.|Common malware target due to popularity.|
|Hardware Support|Drivers often built into the kernel.|Drivers may require manual installation.|

Linux gives you control. Windows gives you convenience. Pick your poison.

---

## Linux Philosophy

Linux isn’t just software it’s a mindset.

### Freedom

Linux gives users the freedom to **run, study, modify, and redistribute** software. This freedom drives innovation and security.

### Collaboration

Thousands of developers around the world contribute to Linux. More eyes = more bugs found = stronger systems.

### Transparency

Because the source code is open, nothing is hidden. If something breaks, you _can_ look inside and see why.

### 📄 Everything Is a File

In Linux, almost everything is treated as a file:

- Documents
    
- Directories
    
- Disks
    
- Devices
    
- Processes
    
- Network connections
    

This makes system management consistent and powerful.

### Small, Specialized Tools

Linux follows the rule:

> _Do one thing, and do it well._

Commands are small and focused. Complex tasks are done by chaining them together using pipes (`|`). Simple tools, powerful results.

---

## How Linux Works

Linux is an operating system like Windows or macOS but with a very different philosophy.

At its core is the **Linux kernel**, which manages:

- CPU
    
- Memory
    
- Storage
    
- Peripherals
    

Applications don’t talk directly to hardware. Instead, they make requests to the kernel. The kernel decides whether the request is allowed and translates it into hardware-level instructions.

Linux also supports:

- **Multitasking** – many programs at once
    
- **Multi-user environments** – many users, same system
    

This is why Linux dominates server environments.

---

## Linux Filesystem Hierarchy Standard (FHS)

Unlike Windows, Linux uses **one single directory tree** starting at `/` (root). This structure is standardized by the **Filesystem Hierarchy Standard (FHS)**.

|Directory|Purpose|Example|
|---|---|---|
|`/`|Root of the filesystem|Entire system|
|`/bin`|Basic user commands|`ls`, `cp`, `bash`|
|`/boot`|Boot-related files|Kernel, GRUB|
|`/dev`|Device files|`/dev/sda`, `/dev/tty`|
|`/etc`|Configuration files|`passwd`, `sshd_config`|
|`/home`|User home directories|`/home/user`|
|`/lib`|Shared libraries|`libc.so`|
|`/mnt`, `/media`|Mounted drives|USB disks|
|`/opt`|Optional third-party software|Chrome, TeamViewer|
|`/proc`|Virtual system info|`cpuinfo`, `meminfo`|
|`/root`|Root user’s home|Admin files|
|`/sbin`|System admin commands|`iptables`, `reboot`|
|`/tmp`|Temporary files|App caches|
|`/usr`|User applications|`/usr/bin/python`|
|`/var`|Variable data|Logs, web files|

Once this structure clicks, Linux starts making _a lot_ more sense.

---

## Linux Architecture

Linux is built in layers, each with a specific role:

- **Hardware Layer**  
    Physical components like CPU, RAM, disks, and network cards.
    
- **Kernel Layer**  
    The brain of the operating system.
    
    - _Kernel Space_: Secure area with direct hardware access (drivers live here).
        
    - _User Space_: Restricted area for applications. Access happens via system calls.
        
- **System Libraries**  
    Translate complex kernel operations into simple functions (e.g., `glibc`).
    
- **Shell Layer**  
    Command-line interface (Bash, Zsh) that passes user commands to the kernel.
    
- **Application Layer**  
    Programs like browsers, editors, databases, and servers.
    

---

## Linux Boot Process (What Happens After You Press Power)

When a Linux system starts, a lot happens before you see a login screen:

1. **BIOS / UEFI**  
    Performs hardware checks and searches for a bootable device.
    
2. **MBR / GPT**  
    Reads the disk’s boot record.
    
3. **Bootloader (GRUB)**  
    Loads the selected Linux kernel into memory.
    
4. **Kernel**  
    Detects hardware, loads drivers, mounts the root filesystem (`/`).
    
5. **Init System (systemd / SysVinit)**  
    Runs as the first process (PID 1), starts services, networking, and the login screen.
    

By the time you type your password, Linux has already done a marathon behind the scenes.

---

> Linux may look intimidating at first, but once you understand how it’s structured, it stops feeling mysterious and starts feeling powerful.
