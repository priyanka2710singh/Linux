### 1. `uname -a`

**Description:**  
Displays all available system information including the kernel name, version, hostname, and architecture.

---

**🔧 Sample Output:**

```bash
Linux server1 5.15.0-101-generic #1 SMP Mon Jan 1 00:00:00 UTC 2024 x86_64 GNU/Linux
```
---

### 2. `hostnamectl`

**Description:**  
Detailed system info including hostname, OS, kernel, and architecture.

---

**🔧 Sample Output:**

```bash
   Static hostname: server1
         Icon name: computer-vm
           Chassis: vm
        Machine ID: 123...
           Boot ID: abc...
  Operating System: Ubuntu 22.04.4 LTS
            Kernel: Linux 5.15.0-101-generic
      Architecture: x86-64
```
---

### 3. `uptime`

**Description:**  
Shows: How long the system has been running, number of users, load averages.

---

**🔧 Sample Output:**

```bash
 14:22:31 up 3 days,  5:17,  2 users,  load average: 0.01, 0.03, 0.00

up 3 days: Uptime
2 users: Logged-in users
load average: CPU load in 1, 5, 15 minutes
```
---

### 4. `whoami`

**Description:**  
Shows: Current logged-in user.

---

**🔧 Sample Output:**

```bash
admin
```
---

### 5. `id`

**Description:**  
Shows: User ID, group ID, and groups of current user.

---

**🔧 Sample Output:**

```bash
uid=1000(admin) gid=1000(admin) groups=1000(admin),27(sudo)
```
---

### 6. `lsb_release -a`

**Description:**  
Shows: Distribution-specific information.

---

**🔧 Sample Output:**

```bash
Distributor ID: Ubuntu  
Description:    Ubuntu 22.04.4 LTS  
Release:        22.04  
Codename:       jammy
```
---

### 7. `cat /etc/os-release`

**Description:**  
Shows: OS metadata (standard across distros).

---

**🔧 Sample Output:**

```bash
NAME="Ubuntu"
VERSION="22.04.4 LTS (Jammy Jellyfish)"
ID=ubuntu
PRETTY_NAME="Ubuntu 22.04.4 LTS"
```
---

### 8. `arch`

**Description:**  
Shows: CPU architecture (same as uname -m).

---

**🔧 Sample Output:**

```bash
x86_64
```
---

### 9. `lscpu`

**Description:**  
Shows: Detailed CPU info.


Key fields:
Architecture: x86_64
CPU(s): Number of logical CPUs
Model name: CPU model
Threads per core, Cores per socket, etc.

### 10. free -h

**Description:**  
Shows: RAM and swap usage in human-readable form.

---

**🔧 Sample Output:**

```bash
              total        used        free      shared  buff/cache   available
Mem:           15Gi        3Gi         8Gi        100Mi       4Gi        11Gi
Swap:          2Gi         0Gi         2Gi
```
---
### 11. `vmstat`

**Description:**  
Shows: Memory, swap, I/O, CPU stats.

---

**🔧 Sample Output:**

```bash
procs -----------memory---------- ---swap-- -----io---- -system-- ------cpu-----
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st
 0  0      0 800000 100000 400000    0    0     1     1   10   30  5  1 93  1  0
 ```
---

### 12. `top`

**Description:**  
Shows: Live process monitoring (CPU/mem per process).

---

**🔧 Sample Output:**

```bash
%CPU, %MEM: Resource usage
PID: Process ID
TIME+: Total CPU time
Tasks, load average, Mem, Swap: Summary at top
```
---

### 13. `htop`

**Description:**  
Like top, but user-friendly with colors, graphs, and easier navigation.

### 14. `dmesg`

**Description:**  
Shows: Kernel ring buffer logs (boot messages, hardware detection).

---

**🔧 Sample Output:**

```bash

Common entries:
[ 0.000000] Linux version...
Detected CPU...
eth0: Link is up...
```
---

### 15. `lsblk`

**Description:**  
Shows: Block devices (disks, partitions) in a tree view.

---

**🔧 Sample Output:**

```bash
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sda      8:0    0   50G  0 disk
├─sda1   8:1    0   48G  0 part /
├─sda2   8:2    0    2G  0 part [SWAP]
```
---

### 16. `lspci`

**Description:**  
Shows: PCI devices (network cards, GPUs, etc).

---

**🔧 Sample Output:**

```bash
00:1f.6 Ethernet controller: Intel Corporation Ethernet Connection (7) I219-V
```
---

### 17. `lsusb`

**Description:**  
Shows: Connected USB devices.

---

**🔧 Sample Output:**

```bash
Bus 002 Device 003: ID 046d:c534 Logitech USB Receiver
```
---

### 18. `df -h`

**Description:**  
Shows: Mounted filesystem space usage.

---

**🔧 Sample Output:**

```bash
Filesystem      Size  Used Avail Use% Mounted on  
/dev/sda1        48G   15G   31G  33% /
```
---

### 19. `du -sh *`

**Description:**  
Shows: Disk usage per file/directory in current folder.

---

**🔧 Sample Output:**

```bash
4.0K  file1.txt  
512M  backup  
2.1G  /var
```
---

### 20. `uptime -p`

**Description:**  
Shows: Pretty format uptime.

---

**🔧 Sample Output:**

```bash
up 3 days, 5 hours, 22 minutes
```
---

### 21. `uptime -s`

**Description:**  
Shows: System start time.

---

**🔧 Sample Output:**

```bash
2025-04-16 08:10:15
```
---

### 22. `who`

**Description:**  
Shows: Logged-in users.

---

**🔧 Sample Output:**

```bash
admin   pts/0   2025-04-19 10:00 (10.0.2.2)
```
---

### 23. `w`

**Description:**  
Shows: Who is logged in and what they are doing.

---

**🔧 Sample Output:**

```bash
Includes idle time, current command, login time.
```
---

### 24. `last`

**Description:**  
Shows: History of logins.

---

**🔧 Sample Output:**

```bash
admin  pts/0  10.0.2.2  Fri Apr 19 10:00   still logged in
```
---

### 25. `date`

**Description:**  
Shows: Current date and time.

---

**🔧 Sample Output:**

```bash
Fri Apr 19 14:25:17 IST 2025
```
---

### 26. `timedatectl`

**Description:**  
Shows: Time settings and synchronization status.

---

**🔧 Sample Output:**

```bash
Local time: Fri 2025-04-19 14:25:17 IST  
RTC time:   Fri 2025-04-19 08:55:17  
Time zone:  Asia/Kolkata (IST, +0530)  
NTP enabled: yes
```
---

### 27. `cal`

**Description:**  
Shows: Calendar of current month.

---

**🔧 Sample Output:**

```bash
     April 2025
Su Mo Tu We Th Fr Sa
       1  2  3  4  5
 6  7  8  9 10 11 12
13 14 15 16 17 18 19
...
```
---

### 28. `watch`

**Description:**  
Repeats a command at intervals (default: 2s).
Example:

---

**🔧 Sample Output:**

```bash
watch -n 5 df -h
```
---

### 29. `uname -r`

**Description:**  
Shows: Kernel version.

---

**🔧 Sample Output:**

```bash
5.15.0-101-generic
```
---

### 30. `iostat`

**Description:**  
Shows: CPU and I/O usage statistics.

---

**🔧 Sample Output:**

```bash
avg-cpu:  %user   %system   %iowait ...
           1.00     0.50     0.20

Device:            tps    kB_read/s    kB_wrtn/s
sda               5.00        20.00         5.00
```
---