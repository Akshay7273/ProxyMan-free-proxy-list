# ⚡ ProxyMan - Premium High-Anonymity Proxy Feed

<p align="center">
  <img src="https://img.shields.io/github/last-commit/Akshay7273/ProxyMan-free-proxy-list?style=for-the-badge&logo=github&logoColor=white&label=Last%20Updated" alt="Last Update Status">
  <img src="https://img.shields.io/badge/Update%20Frequency-Every%2030%20Minutes-blue?style=for-the-badge" alt="Update Frequency">
  <img src="https://img.shields.io/badge/Anonymity-Elite%20%26%20Anonymous-orange?style=for-the-badge" alt="Anonymity Level">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2FAkshay7273%2FProxyMan-free-proxy-list%2Fmain%2Fmeta.json&query=counts.total&label=Live%20Proxies&color=brightgreen" alt="Live Proxies">
  <img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2FAkshay7273%2FProxyMan-free-proxy-list%2Fmain%2Fmeta.json&query=counts.elite&label=Elite&color=orange" alt="Elite">
  <img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2FAkshay7273%2FProxyMan-free-proxy-list%2Fmain%2Fmeta.json&query=counts.socks5&label=SOCKS5&color=blue" alt="SOCKS5">
  <img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2FAkshay7273%2FProxyMan-free-proxy-list%2Fmain%2Fmeta.json&query=counts.countries&label=Countries&color=purple" alt="Countries">
  <img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2FAkshay7273%2FProxyMan-free-proxy-list%2Fmain%2Fmeta.json&query=counts.verified&label=Exit-Verified&color=teal" alt="Verified">
</p>

---

## 🚀 Overview

This repository distributes curated feeds of high-anonymity (Elite) and Anonymous proxies. The lists are continuously tested and updated every 30 minutes, ensuring highly responsive, valid connection nodes for scraping, security research, and network request distribution.

---

## 📂 Active Proxy Feeds

All lists are updated dynamically. Click on any link below to query the raw endpoint:

| Feed Type | Description | 📄 Plain Text (TXT) | 📦 Structured JSON | 📊 Spreadsheet CSV |
| :--- | :--- | :--- | :--- | :--- |
| 🌐 **Master Pool** | Entire compiled set of active proxies | [proxies.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/proxies.txt) | [proxies.json](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/proxies.json) | [proxies.csv](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/proxies.csv) |
| ⚡ **Fast Tier** | Sub-second latency (≤ 500 ms) | [fast.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/fast.txt) | [meta.json](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/meta.json) | — |
| 🏠 **Residential** | Non-datacenter IPs (ISP/mobile) — best for scraping | [hosting/residential.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/hosting/residential.txt) | — | — |
| 🏭 **Datacenter** | Cloud/VPS IPs (most targets block these) | [hosting/datacenter.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/hosting/datacenter.txt) | — | — |
| 🎯 **Target-specific** | Proxies that reach a given site (`--target <site>` runs) | e.g. [targets/xvideos.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/targets/xvideos.txt) | — | — |
| 👑 **Best Tier** | Elite + SSL + fast — the cream of the pool | [best.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/best.txt) | — | — |
| 👑 **Elite Anonymity**| High-anonymity nodes (no header leaks) | [anonymity/elite.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/anonymity/elite.txt) | — | — |
| 🛡️ **Anonymous** | Hides IP, but reveals proxy usage | [anonymity/anonymous.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/anonymity/anonymous.txt) | — | — |
| 🌐 **HTTP Protocol**  | HTTP proxy nodes | [protocols/http.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/protocols/http.txt) | — | — |
| 🔒 **HTTPS Tunnel**   | HTTP proxies supporting SSL CONNECT | [ssl_only.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/ssl_only.txt) | — | — |
| ⚡ **SOCKS5 Protocol**| Fast, secure SOCKS5 network proxies    | [protocols/socks5.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/protocols/socks5.txt) | — | — |
| ⚙️ **SOCKS4 Protocol**| Lightweight SOCKS4 network proxies    | [protocols/socks4.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/protocols/socks4.txt) | — | — |

### 🌍 Georegion-Specific Lists
Filter proxies dynamically by geography using these raw feeds:
- **United States (US):** [countries/us.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/countries/us.txt)
- **Germany (DE):** [countries/de.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/countries/de.txt)
- **Russia (RU):** [countries/ru.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/countries/ru.txt)

---

## 🛡️ Anonymity Schema

*   **Elite (High Anonymity)**: The proxy server does not transmit any headers indicating proxy usage. The destination web server sees requests as originating from a direct client.
*   **Anonymous**: Hides the client's real IP, but transmits headers indicating a proxy server is in use.
*   **Transparent**: Exposes the client's real IP directly to target servers. **Transparent proxies are strictly purged from this feed to maintain performance standards.**

---

## 💻 Quick Integration Examples

### cURL
```bash
curl -O https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/anonymity/elite.txt
```

### Python
```python
import httpx

response = httpx.get("https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/protocols/socks5.txt")
proxies_list = response.text.splitlines()

print(f"Loaded {len(proxies_list)} working SOCKS5 proxies.")
```
