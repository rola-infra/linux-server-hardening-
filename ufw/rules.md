# UFW Firewall Rules

## Status
Active — default deny all incoming

## Allowed Ports

| Port | Protocol | Purpose |
|------|----------|---------|
| 22 | TCP | SSH (OpenSSH) |
| 80 | TCP | HTTP (Nginx) |
| 443 | TCP | HTTPS (Nginx + SSL) |
| 51820 | UDP | WireGuard VPN |

## Default Policy
- Incoming: DENY all (whitelist only)
- Outgoing: ALLOW all
- IPv4 + IPv6 both configured

## Commands Used
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow OpenSSH
sudo ufw allow 80
sudo ufw allow 443
sudo ufw enable
```
