
# Mastering-FreeSWITCH
Setup guide for FreeSWITCH, FusionPBX and projects
=======

# FusionPBX Installation Documentation

## System Details
- Ubuntu 24.04.2 LTS (GNU/Linux 6.14.0-24-generic x86_64)
- Date: Fri Sep 5 01:30:13 PM UTC 2025
- IP: 192.168.1.6

## Installation Steps
1. Updated and upgraded system: `sudo apt update && sudo apt upgrade -y`
2. Ran pre-install script: `sudo wget -O - https://raw.githubusercontent.com/fusionpbx/fusionpbx-install.sh/master/debian/pre-install.sh | sudo sh`
3. Navigated to directory: `cd /usr/src/fusionpbx-install.sh/ubuntu`
4. Ran install script: `sudo ./install.sh`

## Post-Installation Verification
- Check FreeSWITCH version and status:
  ```
  sudo fs_cli -x 'version'
  ```
- Access the FusionPBX web UI at `http://192.168.1.6` and log in using the admin credentials created during installation.
- If errors occur, check logs:
  ```
  tail -f /var/log/freeswitch/freeswitch.log
  tail -f /var/log/nginx/error.log
  ```
- Secure the server:
  - Enable firewall rules:
    ```
    sudo ufw allow 80,443,5060/tcp
    sudo ufw enable
    ```
  - Consider installing and configuring Fail2Ban for security.

## GitHub Setup
- Installed and configured Git.
- Generated SSH key and added it to GitHub.
- Cloned repository and managed readme file.

## Git Troubleshooting
- Encountered conflicts when pushing due to remote changes.
- Resolved conflicts with `git pull --rebase` and manual merges.
- Successfully synchronized local README.md with remote repository.

## Notes
- System restart was required and applied.
- Keep this README updated with further configuration and usage notes.