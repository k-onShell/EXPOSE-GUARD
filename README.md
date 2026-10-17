# EXPOSE-GUARD — External Attack Surface Reconnaissance Tool

**EXPOSE-GUARD** is a professional, high-performance command-line reconnaissance and attack-surface auditing framework built for security teams and system administrators to map, analyze, and monitor their organization's public-facing digital infrastructure.

Featuring a dark cyber-intelligence terminal aesthetic built with `rich` and `typer`, EXPOSE-GUARD discovers subdomains, inspects DNS records, analyzes TLS/SSL certificates, fingerprints public web technologies, and generates comprehensive intelligence reports.

---

## Features

- **Subdomain Enumeration:** Discovers publicly accessible subdomains using certificate transparency logs and safe DNS wordlists.
- **Comprehensive DNS Auditing:** Resolves A, AAAA, MX, NS, TXT, and CNAME records with full syntax validation.
- **TLS/SSL Certificate Inspection:** Analyzes certificate validity, issuer details, SAN (Subject Alternative Names), and expiration dates.
- **Technology Fingerprinting:** Detects open HTTP headers, server banners, and publicly exposed web frameworks.
- **Evidence & Correlation:** Tracks findings with confidence ratings, timestamps, and source attribution.
- **Multi-Format Reporting:** Exports clean, professional reports in JSON, HTML (dark theme), and Markdown.
- **Asynchronous Engine:** Built with `asyncio` and `httpx` for fast, rate-limited concurrent execution.

---

## Project Structure

```text
expose-guard/
├── main.py
├── pyproject.toml
├── README.md
├── config/
│   └── settings.example.toml
├── engine/
│   ├── scanner.py
│   ├── resolver.py
│   ├── tls_checker.py
│   └── reporting.py
├── modules/
│   ├── subdomains.py
│   ├── dns_audit.py
│   ├── cert_intel.py
│   └── tech_stack.py
├── ui/
│   ├── banner.py
│   ├── dashboard.py
│   └── theme.py
├── storage/
│   └── database.py
├── reports/
└── tests/
    ├── test_resolver.py
    └── test_scanner.py
```

---

## Installation

1. **Clone or download the repository:**
   ```bash
   cd expose-guard
   ```

2. **Create a virtual environment & install dependencies:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -e .
   ```

---

## Command-Line Usage

```bash
# Run interactive terminal dashboard
python main.py

# Audit DNS records for a target domain
python main.py dns --target example.com

# Inspect TLS/SSL certificate
python main.py tls --target example.com

# Scan for subdomains via certificate transparency
python main.py subdomains --target example.com

# Fingerprint technology stack
python main.py tech --target example.com

# Generate full attack surface report (JSON & HTML)
python main.py audit --target example.com --html --json

# View past session history
python main.py history
```

*(Note: Always use authorized domains such as `example.com` or your organization's designated assets for testing.)*

---

## License

MIT License — For authorized security testing and defensive auditing only.
