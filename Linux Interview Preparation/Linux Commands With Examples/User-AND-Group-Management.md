### 1. `adduser username`

**Description:**  
Interactive command to add a new user with home directory, shell, and prompts for password.

---

**🔧 Sample Output:**

```bash
Adding user `john' ...
Adding new group `john' (1001) ...
Adding new user `john' (1001) with group `john' ...
Creating home directory `/home/john' ...
Copying files from `/etc/skel' ...
New password:
Retype new password:
```

### 2. `useradd`


**Description:** 
Low-level command to add a new user (non-interactive). Use -m to create home directory.

---

**🔧 Sample Output:**

```bash
useradd -m alice
```

Creates user alice with home directory /home/alice.

### 3. `userdel`

**Description:** 
Deletes a user account. Add -r to remove home directory.

---

**🔧 Sample Output:**

```bash
userdel -r alice
```

Deletes user alice and their home directory.

### 4. `usermod`

**Description:** 
Modifies an existing user account. Used to change login name, group, shell, etc.

---

**🔧 Sample Output:**

```bash

usermod -l alice john
```

Renames user john to alice.

### 5. `passwd'

**Description:** 
Changes the password of a user.

---

**🔧 Sample Output:**

```bash

passwd john
New password:
Retype new password:
```

### 6. `chage`

**Description:** 
Views or modifies user account aging information.

---

**🔧 Sample Output:**

```bash

chage -l john
```

Shows password expiration and account aging details.

7. groupadd

**Description:** 
Description:Creates a new group.

---

**🔧 Sample Output:**

```bash
groupadd developers
```

Creates a group named developers.

8. groupdel

**Description:** 
Deletes a group.


---

**🔧 Sample Output:**

```bash

groupdel developers
```

Deletes the developers group.

9. groupmod

Description:Modifies a group (e.g., renames it).

🔧 Sample Output:

groupmod -n devteam developers

Renames group developers to devteam.

10. gpasswd

Description:Administers /etc/group, sets group administrator and password.

🔧 Sample Output:

gpasswd -a john developers

Adds user john to developers group.

11. groups username

Description:Displays groups of the specified user.

🔧 Sample Output:

groups john
john : john sudo developers

12. id username

Description:Prints user ID (UID), group ID (GID), and groups.

🔧 Sample Output:

id john
uid=1001(john) gid=1001(john) groups=1001(john),27(sudo)

13. getent passwd

Description:Fetches entries from the /etc/passwd database.

🔧 Sample Output:

getent passwd john
john:x:1001:1001:John Doe:/home/john:/bin/bash

14. getent group

Description:Fetches entries from the /etc/group database.

🔧 Sample Output:

getent group sudo
group:x:27:john

15. who

Description:Displays who is logged in.

🔧 Sample Output:

john    pts/0        2025-04-19 10:00 (192.168.1.10)

16. w

Description:Displays logged-in users and their activity.

🔧 Sample Output:

 10:10:01 up 5 days,  2:00,  2 users,  load average: 0.01, 0.05, 0.00
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT
john     pts/0    192.168.1.10     10:00    1:00   0.01s  0.01s -bash

17. users

Description:Prints the login names of the users currently logged in.

🔧 Sample Output:

john alice

18. su - username

Description:Switches to another user’s shell with login environment.

🔧 Sample Output:

su - alice
Password:

19. sudo -i

Description:Starts a root shell as if the user had logged in directly.

🔧 Sample Output:

sudo -i
root@hostname:~#

20. visudo

Description:Safely edits the sudoers file with syntax checking.

🔧 Sample Output:

visudo

Launches editor for /etc/sudoers.

21. sudo usermod -aG sudo username

Description:Adds a user to the sudo group.

🔧 Sample Output:

sudo usermod -aG sudo john

22. lastlog

Description:Displays last login of all users.

🔧 Sample Output:

Username         Port     From             Latest
john             pts/0    192.168.1.10     Fri Apr 19 10:00:00 +0530 2025

23. faillog

Description:Displays failed login attempts.

🔧 Sample Output:

Login       Failures Maximum Latest
john        2        3       04/19/25 09:59:59 +0530

24. finger

Description:Shows user information.

🔧 Sample Output:

Login: john                          Name: John Doe
Directory: /home/john               Shell: /bin/bash

25. loginctl

Description:Manages user logins (systemd-based systems).

🔧 Sample Output:

loginctl list-sessions
   SESSION        UID USER     SEAT  TTY
        2        1001 john     seat0 tty2

26. nologin

Description:Denies a user login access (used as shell).

🔧 Sample Output:

usermod -s /usr/sbin/nologin john

27. adduser username --disabled-password

Description:Creates a user without setting a password.

🔧 Sample Output:

adduser john --disabled-password

28. vipw

Description:Safely edits the /etc/passwd file.

🔧 Sample Output:

vipw

29. vigr

Description:Safely edits the /etc/group file.

🔧 Sample Output:

vigr

30. pwck

Description:Checks integrity of /etc/passwd and /etc/shadow files.

🔧 Sample Output:

pwck