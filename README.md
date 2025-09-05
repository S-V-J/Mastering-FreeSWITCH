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
2. Ran pre-install script: `sudo wget -O - https://raw.githubusercontent.com/fusionpbx/fusionpbx-install.sh/master/ubuntu/pre-install.sh | sudo sh`
3. Navigated to directory: `cd /usr/src/fusionpbx-install.sh/ubuntu`
Note: Install as per the OS: centos  debian  devuan  freebsd  ubuntu  windows
4. Ran install script: `sudo ./install.sh`
## Notes
- System restart was required and applied.
- GitHub linked via SSH key.
- Add updates here as you proceed (e.g., configuration changes).

## Post-Installation Verification Steps

1. Check FreeSWITCH status:
   ```
   sudo fs_cli -x 'version'
   ```

2. Access the FusionPBX web interface:
   - Open a web browser and go to `http://192.168.1.6` (replace with your server IP).
   - Log in with the administrator credentials set during installation.

3. Check logs for troubleshooting:
   - FreeSWITCH log: `tail -f /var/log/freeswitch/freeswitch.log`
   - Nginx error log: `tail -f /var/log/nginx/error.log`

4. Secure your installation:
   - Enable HTTPS with Let's Encrypt or another certificate provider.
   - Configure the firewall to allow necessary ports:
     ```
     sudo ufw allow 80,443,5060/tcp
     sudo ufw enable
     ```
   - Consider installing and configuring Fail2Ban to prevent brute-force attacks.

## GitHub Repository Linking Notes

- Installed and configured Git.
- Generated SSH key and linked to GitHub account.
- Initialized Git repository in installation directory.
- Resolved conflicts with remote repository during push.
- Successfully pushed README.md with installation documentation and updates.