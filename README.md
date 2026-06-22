# 🛡️ Cybersecurity Python Toolkit

**Practical security tools that demonstrate the fundamentals — entropy, breach-checking, and network reconnaissance — with production-minded engineering.**

![lang](https://img.shields.io/badge/language-Python-blue)
![focus](https://img.shields.io/badge/focus-security%20%C2%B7%20automation-success)
![design](https://img.shields.io/badge/design-modular%20%C2%B7%20JSON%20%C2%B7%20API--ready-informational)

## Tools
- **Password Strength & Entropy Analyzer** — calculates Shannon entropy (`E = L·log₂(R)`), estimates time-to-crack against an offline brute-force model, detects common patterns via regex, and checks **Have I Been Pwned** using **k-anonymity** (SHA-256 prefix) so the password is never sent in clear text.
- **Port Scanner** — class-based TCP scanner designed to be imported into a larger monitoring dashboard.

## Engineering principles
- **Modular architecture** — input/output is decoupled from the security analysis engines.
- **Structured JSON output** — every tool returns dictionaries, ready to drop behind a FastAPI/Flask endpoint.
- **Defensive programming** — input validation and edge-case handling throughout.
- Applies real concepts: information theory (Shannon entropy), k-anonymity for privacy-preserving breach checks, and secure hashing.

## Tech stack
Python · `hashlib` (SHA-256) · `re` · `socket` · HIBP API (k-anonymity)

---
© 2026 Alen Trgovcevic. A learning & demonstration toolkit; source overview shown here.
