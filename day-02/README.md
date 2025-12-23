# Day 02 – Create a temporary user with expiry date

## Task Summary
The task was to create a temporary user account on App Server 1 with a defined expiry date to provide time-limited access.

## What I Did
```bash
# Create the user with an expiry date
sudo useradd -e 2024-02-17 jim

# Verify account expiry details
sudo chage -l jim

# Confirm user creation
getent passwd jim
````

## Verification

The user `jim` was created successfully, and the account expiry date was confirmed as `2024-02-17` using `chage -l`.

## Issues Faced

No issues faced.

## What I Learned

* How to create a Linux user with an account expiry date.
* How to verify user expiry information using `chage`.
* Why expiry dates are important for temporary access control.