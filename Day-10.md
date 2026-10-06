# Day 10: Managing Users and Permissions in Linux

In this lesson, we'll dive deep into user and group management in Linux, including practical applications, commands, and configuration file details.

---

## Importance of Password Security

Passwords are the first line of defense for user accounts. Weak passwords can lead to unauthorized access and compromise system security. Ensure users set complex passwords and follow password policies.

### Key Practices:

* Use at least 8 characters with a mix of upper/lower case letters, numbers, and special characters.
* Periodically change passwords to minimize exposure risk.
* Avoid sharing passwords.

---

## Using `passwd` Command

The `passwd` command is used to change a user's password and manage password-related settings.

### Syntax:

```bash
passwd [OPTIONS] [USER]
```

### Examples:

* Change the current user’s password:

  ```bash
  passwd
  ```
* Change another user's password (requires root privileges):

  ```bash
  passwd username
  ```
* Lock a user's account:

  ```bash
  passwd -l username
  ```
* Unlock a user's account:

  ```bash
  passwd -u username
  ```
* Expire a user's password to force a reset on the next login:

  ```bash
  passwd -e username
  ```

---

## Account Locking and Expiration

Locking accounts can prevent unauthorized logins, while expiration ensures unused accounts are deactivated.

### Lock Account:

```bash
passwd -l username
```

### Check Account Details:

```bash
chage -l username
```

---

## Understanding `/etc/shadow` Fields

The `/etc/shadow` file stores encrypted passwords and account metadata.

### Fields:

```text
username:password:last_change:min_days:m
```
