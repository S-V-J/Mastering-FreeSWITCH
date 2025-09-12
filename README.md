# README.md - Mastering FreeSWITCH on Ubuntu 24.04/22.04 LTS
## Project Status: Phase 1 - FreeSWITCH Standalone Complete ✅

### System Information
- **Operating System**: Ubuntu 24.04.2 LTS (GNU/Linux 6.14.0-24-generic x86_64)
- **FreeSWITCH Version**: 1.10.12-release (verified running)
- **Installation Date**: September 5, 2025
- **Server IP**: 192.168.1.6
- **GitHub Repository**: [Mastering-FreeSWITCH](https://github.com/S-V-J/Mastering-FreeSWITCH)

## Completed Tasks
### ✅ Phase 1A: System Preparation
- [x] Full system update & upgrade  (`sudo apt update && sudo apt upgrade -y`)
- [x] SSH key generation and GitHub linking
- [x] User "voip_sid" created; systemd ready for FreeSWITCH

### ✅ Phase 1B: FreeSWITCH Installation
- [x] Downloaded and installed FreeSWITCH 1.10.12 from SignalWire / source
- [x] Verified FreeSWITCH version via `freeswitch -version`
- [x] Enabled and started FreeSWITCH with `systemctl`
- [x] Confirmed running state (`systemctl status freeswitch`, `fs_cli` CLI access)

#### FreeSWITCH Running Output
```bash
$ freeswitch -version
FreeSWITCH version: 1.10.12-release... (git d8481a9 2025-01-13 ... 64bit)
$ sudo systemctl status freeswitch
● freeswitch.service - freeswitch
 Active: active (running)
$ fs_cli
# FreeSWITCH CLI appears. Status: running, 0 sessions since startup
```

### 🌟 Phase 1C: Foundation Configuration (SIP)
- [ ] **To Do**: Basic SIP profile and extensions XML setup
  - `/etc/freeswitch/sip_profiles/internal.xml` and `/etc/freeswitch/directory/default/`
  - Secure RTP port range configured in `vars.xml`
  - `fs_cli -x "reloadxml"` for config reload

### 🔒 Security Considerations
- [ ] RTP range customized and firewall rules pending
- [ ] Default extension passwords to be reset to strong values

### 🏗️ Next: Phase 1D - Testing
- [ ] Register two softphones (Zoiper, Linphone) on extensions "1000" and "1001"
- [ ] Test local call and verify audio with `fs_cli -x "show channels"`
- [ ] Troubleshoot logs if needed

## Current Project Phase
- **Focus:** Standalone FreeSWITCH, without FusionPBX
- Use this README to document step-by-step CLI, XML, and troubleshooting for FreeSWITCH

---
## Git Repository Update Instructions
1. Stage edits: `git add README.md docs/ configs/`
2. Commit: `git commit -m "docs: Phase 1 FreeSWITCH standalone installation and verification"`
3. Push: `git push origin main`

## Next Steps
1. Edit XML configs for internal SIP profile and create extension users
2. Add step-by-step CLI for users to register and call
3. Continue documentation in `docs/installation/` and `docs/configuration/`

> **Last Updated:** September 12, 2025