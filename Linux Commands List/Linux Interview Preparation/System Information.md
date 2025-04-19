### 1. `uname -a`

**Description:**  
Displays all available system information including the kernel name, version, hostname, and architecture.

---

**🔧 Sample Output:**

```bash
Linux server1 5.15.0-101-generic #1 SMP Mon Jan 1 00:00:00 UTC 2024 x86_64 GNU/Linux


### 2. `hostnamectl`
Shows: Detailed system info including hostname, OS, kernel, and architecture.
Sample Output:
   Static hostname: server1
         Icon name: computer-vm
           Chassis: vm
        Machine ID: 123...
           Boot ID: abc...
  Operating System: Ubuntu 22.04.4 LTS
            Kernel: Linux 5.15.0-101-generic
      Architecture: x86-64

3. uptime

Shows: How long the system has been running, number of users, load averages.

Sample Output:
 14:22:31 up 3 days,  5:17,  2 users,  load average: 0.01, 0.03, 0.00

up 3 days: Uptime
2 users: Logged-in users
load average: CPU load in 1, 5, 15 minutes

4. whoami
Shows: Current logged-in user.
admin

5. id
Shows: User ID, group ID, and groups of current user.
uid=1000(admin) gid=1000(admin) groups=1000(admin),27(sudo)

6. lsb_release -a

Shows: Distribution-specific information.
Distributor ID: Ubuntu  
Description:    Ubuntu 22.04.4 LTS  
Release:        22.04  
Codename:       jammy

7. cat /etc/os-release
Shows: OS metadata (standard across distros).
NAME="Ubuntu"
VERSION="22.04.4 LTS (Jammy Jellyfish)"
ID=ubuntu
PRETTY_NAME="Ubuntu 22.04.4 LTS"

8. arch
Shows: CPU architecture (same as uname -m).
x86_64

9. lscpu
Shows: Detailed CPU info.

Key fields:
Architecture: x86_64
CPU(s): Number of logical CPUs
Model name: CPU model
Threads per core, Cores per socket, etc.

10. free -h

Shows: RAM and swap usage in human-readable form.
              total        used        free      shared  buff/cache   available
Mem:           15Gi        3Gi         8Gi        100Mi       4Gi        11Gi
Swap:          2Gi         0Gi         2Gi

11. vmstat

Shows: Memory, swap, I/O, CPU stats.
procs -----------memory---------- ---swap-- -----io---- -system-- ------cpu-----
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st
 0  0      0 800000 100000 400000    0    0     1     1   10   30  5  1 93  1  0

12. top

Shows: Live process monitoring (CPU/mem per process).
%CPU, %MEM: Resource usage
PID: Process ID
TIME+: Total CPU time
Tasks, load average, Mem, Swap: Summary at top

13. htop

Like top, but user-friendly with colors, graphs, and easier navigation.

14. dmesg

Shows: Kernel ring buffer logs (boot messages, hardware detection).

Common entries:
[ 0.000000] Linux version...
Detected CPU...
eth0: Link is up...

15. lsblk

Shows: Block devices (disks, partitions) in a tree view.
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sda      8:0    0   50G  0 disk
├─sda1   8:1    0   48G  0 part /
├─sda2   8:2    0    2G  0 part [SWAP]

16. lspci

Shows: PCI devices (network cards, GPUs, etc).
00:1f.6 Ethernet controller: Intel Corporation Ethernet Connection (7) I219-V

17. lsusb

Shows: Connected USB devices.
Bus 002 Device 003: ID 046d:c534 Logitech USB Receiver

18. df -h

Shows: Mounted filesystem space usage.
Filesystem      Size  Used Avail Use% Mounted on  
/dev/sda1        48G   15G   31G  33% /

19. du -sh *

Shows: Disk usage per file/directory in current folder.
4.0K  file1.txt  
512M  backup  
2.1G  /var

20. uptime -p

Shows: Pretty format uptime.
up 3 days, 5 hours, 22 minutes

21. uptime -s

Shows: System start time.
2025-04-16 08:10:15

22. who

Shows: Logged-in users.
admin   pts/0   2025-04-19 10:00 (10.0.2.2)

23. w

Shows: Who is logged in and what they are doing.
Includes idle time, current command, login time.

24. last

Shows: History of logins.
admin  pts/0  10.0.2.2  Fri Apr 19 10:00   still logged in

25. date

Shows: Current date and time.
Fri Apr 19 14:25:17 IST 2025

26. timedatectl

Shows: Time settings and synchronization status.
Local time: Fri 2025-04-19 14:25:17 IST  
RTC time:   Fri 2025-04-19 08:55:17  
Time zone:  Asia/Kolkata (IST, +0530)  
NTP enabled: yes

27. cal

Shows: Calendar of current month.
     April 2025
Su Mo Tu We Th Fr Sa
       1  2  3  4  5
 6  7  8  9 10 11 12
13 14 15 16 17 18 19
...

28. watch

Repeats a command at intervals (default: 2s).
Example:
watch -n 5 df -h

29. uname -r

Shows: Kernel version.
5.15.0-101-generic

30. iostat

Shows: CPU and I/O usage statistics.
avg-cpu:  %user   %system   %iowait ...
           1.00     0.50     0.20

Device:            tps    kB_read/s    kB_wrtn/s
sda               5.00        20.00         5.00