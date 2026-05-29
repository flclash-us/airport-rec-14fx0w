# AdBlock Rules for Clash 8lsznw

Comprehensive ad-blocking rule sets compatible with Clash, Clash Meta, and OpenClash. Block ads, trackers, malware, and phishing domains.

## Rule Sets

| Rule | Type | Entries | Description |
|------|------|---------|-------------|
| `ad-domain.yaml` | Domain | 500+ | Ad & tracker domains |
| `ad-ip.yaml` | IP-CIDR | 100+ | Ad server IP ranges |
| `malware.yaml` | Domain | 300+ | Malware & phishing domains |
| `tracking.yaml` | Domain | 200+ | Tracking & analytics domains |

## Quick Setup

### Method 1: Rule Provider (Recommended)

Add to your Clash config:

```yaml
rule-providers:
  adblock:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/flclash-us/adblock-rules-clash-8lsznw/main/rules/ad-domain.yaml"
    path: ./ruleset/adblock.yaml
    interval: 86400

  malware:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/flclash-us/adblock-rules-clash-8lsznw/main/rules/malware.yaml"
    path: ./ruleset/malware.yaml
    interval: 86400

rules:
  - RULE-SET,adblock,REJECT
  - RULE-SET,malware,REJECT
  - MATCH,Proxy
```

### Method 2: Direct Rules

```yaml
rules:
  - DOMAIN-SUFFIX,ad.com,REJECT
  - DOMAIN-SUFFIX,adservice.google.com,REJECT
  - DOMAIN-KEYWORD,adservice,REJECT
  - DOMAIN-KEYWORD,analytics,REJECT
  - IP-CIDR,192.168.0.0/16,DIRECT
```

## Auto Update

Rule providers automatically update every 24 hours. You can force update in the Clash dashboard.

## Performance Impact

- Domain rules: Minimal (hash lookup)
- IP-CIDR rules: Low (tree lookup)
- Rule providers: Only loaded once, then cached

## Recommended Tools

- [FlClash](https://flclash.us/) - Best proxy client for Windows/Mac/Linux
- [Clash for Windows](https://clashforwindows.site/) - Most popular Clash GUI
- [ClashMI](https://clashmi.site/) - Lightweight Clash client
- [FlClash](https://flclash.us/) - Modern proxy tool

## License

MIT License
