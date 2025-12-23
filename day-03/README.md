# Day 03 – Disable direct SSH root login

## Task Summary
The task was to improve server security by disabling direct SSH login for the root user on all App Servers in the Stratos Datacenter.

## What I Did
```bash
# App Server 1
sudo vi /etc/ssh/sshd_config
sudo systemctl restart sshd
ssh root@172.16.238.10

# App Server 2
sudo vi /etc/ssh/sshd_config
sudo systemctl restart sshd
ssh root@172.16.238.11

# App Server 3
sudo vi /etc/ssh/sshd_config
sudo systemctl restart sshd
````

The following configuration was set in the SSH daemon configuration file:

```
PermitRootLogin no
```

## Verification

After restarting the SSH service on each server, attempts to log in directly as the root user via SSH were denied, confirming that root SSH access was disabled.

## Issues Faced

No issues faced.

## What I Learned

* How to disable direct root login via SSH.
* Why disabling root SSH access improves system security.
* How to apply and verify SSH configuration changes across multiple servers.