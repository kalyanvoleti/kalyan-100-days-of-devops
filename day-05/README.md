# Day 05 – Disable SELinux in config

## Task Summary
The task was to install required SELinux packages and set SELinux to disabled in the configuration file on App Server 2 without rebooting.

## What I Did
```bash
# Install SELinux packages
yum install -y selinux-policy selinux-policy-targeted libselinux-utils policycoreutils

# Disable SELinux permanently in config
sed -i 's/^SELINUX=.*/SELINUX=disabled/' /etc/selinux/config

# Verify SELinux config change
grep "^SELINUX=" /etc/selinux/config
````

## Verification

The configuration file was updated to `SELINUX=disabled`, confirmed using grep.

## Issues Faced

No issues faced.

## What I Learned

* How to install SELinux packages using yum.
* How to disable SELinux by editing the config file.
* Final SELinux status after reboot depends on `/etc/selinux/config`, not runtime state.