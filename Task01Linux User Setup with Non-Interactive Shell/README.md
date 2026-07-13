# Linux Administration - Create a Non-Interactive User

## Objective

Create a user with a non-interactive shell on a remote application server.

## Environment

* Jump Host: `jump-host`
* Target Server: `stapp01`
* User: `tony`

## Steps

1. Connect to the target server:

   ```bash
   ssh tony@stapp01
   ```

2. Create the user with a non-interactive shell:

   ```bash
   sudo useradd -m -s /usr/sbin/nologin john
   ```

3. Verify the user:

   ```bash
   getent passwd john
   ```

## Expected Output

```text
john:x:1001:1001::/home/john:/usr/sbin/nologin
```

## Key Concepts

* `useradd` – Creates a new user.
* `-m` – Creates the user's home directory.
* `-s /usr/sbin/nologin` – Assigns a non-interactive shell, preventing direct login.
* `getent passwd` – Verifies the user account information.

## Skills Practiced

* Linux User Management
* SSH Remote Administration
* Linux Security Best Practices
* System Administration
