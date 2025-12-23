# Day 01 – Create a custom Apache user

## Task Summary
The task was to create a custom Apache user on App Server 1 with a specific UID and a custom home directory for a web application.

## What I Did
```bash
# Connect to App Server 1
ssh tony@172.16.238.10

# Create the home directory
sudo mkdir -p /var/www/kareem

# Create user with specific UID and custom home directory
sudo useradd -u 1265 -d /var/www/kareem -s /bin/bash kareem

# Assign ownership of the home directory to the user
sudo chown -R kareem:kareem /var/www/kareem

# Verify user and directory
id kareem
ls -ld /var/www/kareem
````

## Verification

The user `kareem` was created with UID `1265`, and the directory `/var/www/kareem` existed with ownership set to `kareem:kareem`.

## Issues Faced

No issues faced.

## What I Learned

* How to create a user with a custom UID in Linux.
* How to assign a custom home directory during user creation.
* How to verify user and directory ownership.