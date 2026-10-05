# Day 9: Managing Users and Permissions in Linux

## Overview of User and Permission Management

User and permission management is essential for securing a Linux system and controlling access to resources. This involves creating, modifying, and managing users, groups, and permissions to ensure proper access control.

### Practical:

1. Identify the current user:

```bash
whoami
```

2. View all users on the system:

```bash
cat /etc/passwd
```

## Types of Users

Linux categorizes users into:

1. **Root User**: The administrator with full system access.
2. **System Users**: Used for system processes and services.
3. **Regular Users**: General users with restricted permissions.

### Practical:

1. Check the root user:

```bash
id root
```

2. Identify system users:

```bash
less /etc/passwd | grep -v "/home"
```

## Using `useradd` Command

The `useradd` command creates new user accounts.

### Syntax:

```bash
useradd [options] username
```

### Options:

* `-m`: Create a home directory for the user.
* `-s`: Specify the default shell.
* `-G`: Add the user to supplementary groups.

### Practical:

1. Add a new user:

```bash
sudo useradd -m -s /bin/bash sourabh
```

2. Verify the user:

```bash
id sourabh
```

## Setting User Passwords

Set or change a user password using the `passwd` command.

### Practical:

1. Set a password for a user:

```bash
sudo passwd sourabh
```

2. Test login with the new credentials.

## Managing User Groups

Groups simplify permission management by categorizing users.

### Commands:

* `groupadd`: Create a new group.
* `usermod -aG`: Add a user to a group.
* `groups`: Display groups a user belongs to.

### Practical:

1. Create a new group:

```bash
sudo groupadd developers
```

2. Add a user to the group:

```bash
sudo usermod -aG developers sourabh
```

3. Verify group membership:

```bash
groups sourabh
```

## Removing Users

Delete a user account using the `userdel` command.

### Practical:

1. Remove a user:

```bash
sudo userdel sourabh
```

2. Remove a user and their home directory:

```bash
sudo userdel -r sourabh
```

## Introduction to Affected Files

Several system files are affected during user and permission management:

* `/etc/passwd`: Stores user account details.
* `/etc/shadow`: Stores encrypted passwords.
* `/etc/group`: Stores group details.

### Practical:

1. View the contents of `/etc/passwd`:

```bash
cat /etc/passwd
```

2. Check group details:

```bash
cat /etc/group
```

## User Home Directories

Each user has a dedicated home directory for personal files, typically located in `/home/username`.

### Practical:

1. View a user’s home directory:

```bash
ls /home
```

2. Access another user’s home directory (as root):

```bash
sudo ls /home/sourabh
```

## Switching Between Users in Linux

Switching users is necessary for testing or administrative tasks.

### Using `su` Command

The `su` command switches to another user account.

### Practical:

1. Switch to another user:

```bash
su sourabh
```

2. Return to the previous user:

```bash
exit
```

### Using `sudo` Command

The `sudo` command allows running commands as another user, typically root.

### Practical:

1. Run a command as root:

```bash
sudo apt update
```

## Conclusion

Understanding and managing users and permissions is critical for Linux system administration. By practicing these concepts, you can effectively control access and maintain system security.
