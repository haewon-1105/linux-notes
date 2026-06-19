# Day 2 - Linux File Ownership and Permissions

## What I Learned

Today I learned how Linux manages file ownership and permissions.

I practiced creating files, changing ownership, modifying permissions, and managing access rights for users, groups, and others. I also completed a permissions challenge that required using Linux commands correctly and troubleshooting common syntax mistakes.

---

## File Creation

### touch

Used to create a new file.

Example:

```bash
touch target_file
```

---

## File Ownership

### chown

Used to change the owner and group of a file.

Example:

```bash
sudo chown user1:group1 target_file
```

Verify ownership:

```bash
ls -l target_file
```

Output:

```text
-rw-rw-r-- 1 user1 group1 0 Jun 17 15:20 target_file
```

### Recursive Ownership Change

Used to change ownership for an entire directory structure.

```bash
sudo chown -R root:root new-dir
```

---

## File Permissions

### chmod

Used to modify file and directory permissions.

Numeric notation:

```bash
chmod 700 example.txt
chmod 760 target_file
chmod -R 755 ~/test-dir
```

### Permission Values

| Number | Permission |
| ------ | ---------- |
| 7      | rwx        |
| 6      | rw-        |
| 5      | r-x        |
| 4      | r--        |
| 0      | ---        |

Example:

```bash
chmod 760 target_file
```

Results in:

```text
rwxrw----
```

Meaning:

* Owner: read, write, execute
* Group: read, write
* Others: no permissions

---

## Symbolic Permissions

Used symbolic notation to add execute permission.

```bash
chmod u+x script.sh
```

This allows the file owner to execute the script.

---

## Shell Script Practice

Created a simple shell script:

```bash
#!/bin/bash
echo "Hello, World"
```

Before adding execute permission:

```bash
./script.sh
```

Output:

```text
permission denied
```

After granting execute permission:

```bash
chmod u+x script.sh
./script.sh
```

Output:

```text
Hello, World
```

---

## sudo

Used administrator privileges to perform system-level changes.

Examples:

```bash
sudo chown root:root example.txt
sudo chmod 700 example.txt
```

---

## Challenge Completed

* Created files using `touch`
* Changed ownership using `chown`
* Modified permissions using `chmod`
* Verified permissions using `ls -l`
* Completed a Linux permissions challenge
* Practiced troubleshooting command syntax errors

---

## Key Takeaways

* Linux permissions are divided into owner, group, and others.
* Numeric notation is useful for quickly setting permissions.
* Symbolic notation is useful for modifying specific permissions.
* Recursive options (`-R`) can apply changes to entire directory structures.
* Execute permission is required to run shell scripts.
* Administrative privileges should be used carefully because incorrect permission changes can affect system security and functionality.
