# Linux Server Hardening

SSH and basic security hardening applied on a live Ubuntu VPS.

## SSH Hardening

| Setting | Value | Why |
|---------|-------|-----|
| PermitRootLogin | no | Blocks direct root access |
| PasswordAuthentication | no | Forces key-based login only |
| PubkeyAuthentication | yes | SSH key is the only way in |

## Fail2Ban
- Installed and configured SSH jail
- Automatically bans IPs after failed login attempts
- Protects against brute force attacks

## UFW Firewall
- Enabled and configured
- Only ports 80, 443 and SSH allowed
- All other ports blocked by default

## Stack
Ubuntu Linux · OpenSSH · Fail2Ban · UFW
