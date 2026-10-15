# 🛡️ Cybersecurity Python Toolkit

**Practical security tools that demonstrate the fundamentals — entropy, breach-checking, and network reconnaissance — with production-minded engineering.**

![lang](https://img.shields.io/badge/language-Python-blue)
![focus](https://img.shields.io/badge/focus-security%20%C2%B7%20automation-success)
![design](https://img.shields.io/badge/design-modular%20%C2%B7%20JSON%20%C2%B7%20API--ready-informational)

## Tools
- **Password Strength & Entropy Analyzer** — estimates entropy from length and character pool (`E = L·log₂(R)`), then penalises what makes human passwords guessable: dictionary words (incl. leetspeak), sequences and keyboard walks, years and repeats. `Password123!` rates *Very Weak*. Converts the estimate to a time-to-crack under a stated offline-attack assumption, and checks **Have I Been Pwned** using **k-anonymity**: only the first 5 hex characters of the password's SHA-1 hash leave the machine (SHA-1 because the API requires it). Covered by pytest tests with the API mocked.
- **Port Scanner** — class-based TCP scanner designed to be imported into a larger monitoring dashboard.

## Engineering principles
- **Modular architecture** — input/output is decoupled from the security analysis engines.
- **Structured JSON output** — every tool returns dictionaries, ready to drop behind a FastAPI/Flask endpoint.
- **Defensive programming** — input validation and edge-case handling throughout.
- Applies real concepts: entropy estimation and its limits on human-chosen passwords, k-anonymity for privacy-preserving breach checks, and salted password hashing with `scrypt`. A password hash is never printed, because it is password-equivalent.

## Tech stack
Python · `hashlib` (`scrypt` with salt; SHA-1 only for the HIBP lookup) · `re` · `socket` · HIBP API (k-anonymity) · `pytest`

---
© 2026 Alen Trgovcevic. A learning & demonstration toolkit; source overview shown here.
