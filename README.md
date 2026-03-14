DNS-Blacklist  
**Compact DNS / Hosts Blacklist for Privacy + Security**

A lightweight, frequently updated blocklist focused on telemetry trackers, Microsoft spying domains, bad/malicious IPs, ads, malware C2, and privacy-invasive hosts.  
Designed for DNS resolvers (Pi-hole, AdGuard, unbound, Technitium), hosts files, or any DNS sinkhole setup.

### Why this list?
- Blocks aggressive telemetry (especially Microsoft Windows/Office/Azure telemetry domains)
- Includes known bad IPs (blackhole style: 0.0.0.0 or NXDOMAIN)
- Minimal breakage — focused on privacy without killing core functionality
- Regularly merged from reliable sources + manual curation
- Compact & fast-loading format

### Features
- **Formats available**:
  - `domains.txt` — plain domain list (one per line) → ideal for unbound, dnsmasq, AdGuard
  - `hosts` — classic hosts file format (0.0.0.0 domain.com)
  - `rpz.db` — BIND RPZ format (optional)
  - `adblock` — AdGuard / uBlock Origin syntax
- **Daily / weekly updates** via GitHub Actions
- Low false-positive rate (tested on real networks)
- Includes Microsoft telemetry from BSI SiSyPHuS, hagezi native, and community sources

### Installation / Usage

#### Pi-hole / AdGuard Home
1. Go to **Group Management → Adlists**
2. Add this URL:  
   `https://raw.githubusercontent.com/yourusername/yourdns-blacklist/main/domains.txt`
3. Update gravity / apply changes

#### Hosts file (Windows / macOS / Linux)
Append or replace your system hosts file:
- Windows: `C:\Windows\System32\drivers\etc\hosts`
- Linux/macOS: `/etc/hosts`

**Note**: On Windows 10/11, add exclusion in Defender for "HostsFileHijack" false positive if needed.

#### Unbound / dnsmasq
Use the `domains.txt` file and include it in your config.

### Sources & Credits
Merged & extended from:
- hagezi/dns-blocklists (native trackers)
- BSI SiSyPHuS Win10 telemetry list
- StevenBlack/hosts
- Community reports + manual additions
- and most important VV

### Contributing
Found a missed telemetry domain or bad IP?  
→ Open an issue or submit a PR — all help appreciated!

### License
MIT License — free to use, modify, distribute.  
No warranty — use at your own risk.

⭐ Star this repo if it helps protect your privacy!
