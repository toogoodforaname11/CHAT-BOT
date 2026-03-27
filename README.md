# CHAT-BOT

Chat bot application deployed to Hostinger at [kairo.support](https://kairo.support).

## Hostinger Deployment Setup

This project auto-deploys to Hostinger hosting via GitHub Actions on every push to `main`.

### Setup Steps

1. **Add GitHub Secrets** — Go to your repo **Settings > Secrets and variables > Actions** and add:
   - `HOSTINGER_FTP_SERVER` — Your Hostinger FTP hostname (e.g., `ftp.kairo.support` or find it in hPanel > Files > FTP Accounts)
   - `HOSTINGER_FTP_USERNAME` — Your Hostinger FTP username
   - `HOSTINGER_FTP_PASSWORD` — Your Hostinger FTP password

2. **Connect Domain in Hostinger hPanel**:
   - Log in to [hPanel](https://hpanel.hostinger.com)
   - Go to **Domains > kairo.support**
   - Under **DNS / Nameservers**, make sure nameservers point to Hostinger (ns1.dns-parking.com, ns2.dns-parking.com) or configure the A record to point to your hosting IP
   - Under **Hosting > Manage**, ensure the domain is linked to your hosting plan

3. **Push to `main`** — The GitHub Action will automatically deploy your files to `/public_html/` on Hostinger.
