# Day 04 – Grant execute permission to a script

## Task Summary
The task was to update file permissions so that a backup script on App Server 3 could be executed by all users.

## What I Did
```bash
# Checked existing permissions
ls -l /tmp/xfusioncorp.sh

# Updated permissions to allow execution
sudo chmod 755 /tmp/xfusioncorp.sh

# Verified permissions after change
ls -l /tmp/xfusioncorp.sh

# Tested script execution without sudo
sh /tmp/xfusioncorp.sh
./tmp/xfusioncorp.sh
bash /tmp/xfusioncorp.sh
````

## Verification

After updating the permissions, the script executed successfully without sudo and displayed the expected output:
`Welcome To KodeKloud`.

## Issues Faced

No issues faced.

## What I Learned

* Shell scripts require read permission for the interpreter to execute them.
* Execute permission is required when running scripts directly.
* `chmod 755` is a safe and commonly used permission for executable scripts.
* Always verify permissions and test execution as a non-root user.