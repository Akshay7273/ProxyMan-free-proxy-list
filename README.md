# ⚡ ProxyMan - High-Performance Free Proxy Pools

<p align="center">
  <img src="https://img.shields.io/github/last-commit/Akshay7273/ProxyMan-free-proxy-list?style=for-the-badge&logo=github&logoColor=white&label=Last%20Updated" alt="Last Update Status">
  <img src="https://img.shields.io/badge/Harvester%20Frequency-Every%202%20Hours-blue?style=for-the-badge&logo=cron" alt="Scrape Frequency">
  <img src="https://img.shields.io/badge/Recheck%20Frequency-Every%2015%20Minutes-red?style=for-the-badge" alt="Checker Frequency">
  <img src="https://img.shields.io/badge/Anonymity-Elite%20%26%20Anonymous-orange?style=for-the-badge" alt="Anonymity Level">
</p>

---

## 🚀 Overview

**ProxyMan** is a next-generation, serverless proxy harvesting and validation engine powered by global OSINT databases (Shodan, Censys, ZoomEye, Criminal IP) and custom HTML table crawlers. 

To ensure maximum availability and production-grade stability, we use a **Double-Workflow System**:
- **Harvester Engine (Every 2h)**: Aggregates fresh hosts from security search APIs and performs deep double-pass handshakes. Shodan and Criminal IP limits are managed via query rotation to consume strictly <= 90 credits/month.
- **Checker Engine (Every 15m)**: Runs an ultra-fast parallel TCP ping and reflector connection check on the active pool, purging dead nodes in under 20 seconds. This maintains pool dead-rates below **5%** at any given time.

---

## 📂 Active Proxy Lists (Clickable API Endpoints)

All files are dynamically updated every 15 minutes. Click on any format link below to access the raw data endpoint directly.

| Protocol / Level | Description | 📄 Plain Text (TXT) | 📦 Structured JSON | 📊 Spreadsheet CSV |
| :--- | :--- | :--- | :--- | :--- |
| 🌐 **Master Pool** | Full compiled set of active proxies | [proxies.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/proxies.txt) | [proxies.json](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/proxies.json) | [proxies.csv](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/proxies.csv) |
| 👑 **Elite Anonymity**| High-anonymity nodes (no header leaks) | [anonymity/elite.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/anonymity/elite.txt) | — | — |
| 🛡️ **Anonymous** | Hides IP, but reveals proxy usage | [anonymity/anonymous.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/anonymity/anonymous.txt) | — | — |
| 🌐 **HTTP Protocol**  | HTTP proxy nodes | [protocols/http.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/protocols/http.txt) | — | — |
| 🔒 **HTTPS Tunnel**   | HTTP proxies supporting SSL CONNECT | [ssl_only.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/ssl_only.txt) | — | — |
| ⚡ **SOCKS5 Protocol**| Fast, secure SOCKS5 network proxies    | [protocols/socks5.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/protocols/socks5.txt) | — | — |
| ⚙️ **SOCKS4 Protocol**| Lightweight SOCKS4 network proxies    | [protocols/socks4.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/protocols/socks4.txt) | — | — |

### 🌍 Georegion-Specific Lists
You can also fetch country-specific text lists dynamically from the `countries/` directory by appending the ISO country code. Examples:
- **United States:** [countries/us.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/countries/us.txt)
- **Germany:** [countries/de.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/countries/de.txt)
- **Russia:** [countries/ru.txt](https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/countries/ru.txt)

---

## 🛡️ Anonymity Classification Schema

We test client headers reflection dynamically to classify proxy anonymity:

*   **Elite (High Anonymity)**: The proxy server does not transmit any headers indicating proxy usage (e.g., `Via`, `X-Forwarded-For` are absent). The target web server sees the request as originating from a direct client.
*   **Anonymous**: The proxy hides the client's real IP, but transmits headers revealing it is a proxy server.
*   **Transparent**: Exposes the client's real public IP directly to the destination web server. **Transparent proxies are strictly discarded by our engine to maintain premium quality.**

---

## 💻 Quick Integration Example

### Fetching via cURL
```bash
# Get elite proxies
curl -O https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/anonymity/elite.txt
```

### Python Integration
```python
import httpx

# Fetch SOCKS5 proxy list
response = httpx.get("https://raw.githubusercontent.com/Akshay7273/ProxyMan-free-proxy-list/main/protocols/socks5.txt")
proxies_list = response.text.splitlines()

print(f"Loaded {len(proxies_list)} working SOCKS5 proxies.")
```
