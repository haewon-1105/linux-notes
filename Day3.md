# Day 3 - Linux System Information and User Management

## What I Learned

Today I learned how to gather system information, monitor system activity, and manage Linux user accounts.

I practiced identifying users, checking operating system information, monitoring processes, creating reports using output redirection, and performing common user administration tasks such as creating accounts, setting passwords, managing groups, and controlling account access.

---

## System Information Commands

### whoami

Displays the current logged-in user.

```bash
whoami
```

### id

Displays user ID (UID), group ID (GID), and group memberships.

```bash
id
```

### who

Displays users currently logged into the system.

```bash
who
```

### uname

Displays operating system and kernel information.

```bash
uname
uname -a
```

### top

Displays running processes and system resource usage in real time.

```bash
top
```

---

## Output Redirection

### Overwrite Output

```bash
command > file.txt
```

Example:

```bash
whoami > report.txt
```

### Append Output

```bash
command >> file.txt
```

Example:

```bash
uname >> report.txt
```

---

## User Management

### Create a User

```bash
sudo useradd username
```

### Set a Password

```bash
sudo passwd username
```

### Modify User Properties

Examples:

```bash
sudo usermod -s /bin/bash username
```

Used to modify user settings such as:

* Default shell
* Home directory
* Account information

### Add User to a Group

```bash
sudo usermod -aG groupname username
```

### Lock a User Account

```bash
sudo passwd -l username
```

### Unlock a User Account

```bash
sudo passwd -u username
```

### Delete a User

```bash
sudo userdel username
```

Delete a user and their home directory:

```bash
sudo userdel -r username
```

---

## Important Linux Concepts

### /etc/passwd

Stores user account information including:

* Username
* UID
* GID
* Home directory
* Default shell

### Home Directory

Each user has a personal directory for storing files and configurations.

Example:

```text
/home/username
```

### Default Shell

Common shells include:

* /bin/bash
* /bin/zsh

### User Groups

Groups allow administrators to manage permissions efficiently across multiple users.

---

## Practical Exercises

During today's labs, I:

* Identified the current user using `whoami`
* Checked user and group information using `id`
* Viewed logged-in users with `who`
* Retrieved system information with `uname`
* Monitored processes using `top`
* Created reports using output redirection (`>` and `>>`)
* Created and modified user accounts
* Managed user passwords and groups
* Locked and unlocked user accounts
* Deleted user accounts

---

## Key Takeaways

* Linux uses users and groups to manage access and security.
* System information commands help administrators understand the current environment.
* Process monitoring is essential for troubleshooting and performance analysis.
* Output redirection allows command results to be saved for documentation and reporting.
* Proper user account management is a fundamental system administration skill.
