<div align="center">

```
╔══════════════════════════════════════════════════════════════════════════════╗
║                                                                              ║
║    ███████╗ █████╗ ███╗   ██╗██╗████████╗██╗   ██╗   ██╗   ██╗██████╗      ║
║    ██╔════╝██╔══██╗████╗  ██║██║╚══██╔══╝╚██╗ ██╔╝   ██║   ██║╚════██╗     ║
║    ███████╗███████║██╔██╗ ██║██║   ██║    ╚████╔╝    ██║   ██║  ▄███╔╝     ║
║    ╚════██║██╔══██║██║╚██╗██║██║   ██║     ╚██╔╝     ╚██╗ ██╔╝  ▀▀══╝      ║
║    ███████║██║  ██║██║ ╚████║██║   ██║      ██║       ╚████╔╝   ██╗         ║
║    ╚══════╝╚═╝  ╚═╝╚═╝  ╚═══╝╚═╝   ╚═╝      ╚═╝        ╚═══╝    ╚═╝        ║
║                                                                              ║
║      Anti-Hallucination & Security Supremacy Protocol  ·  v3.0.0            ║
║      Truth × Verification × Zero-Trust Security — No Exceptions             ║
║                                                                              ║
╚══════════════════════════════════════════════════════════════════════════════╝
```

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![Version](https://img.shields.io/badge/version-3.0.0-brightgreen)](CHANGELOG.md)
[![SANITY Score](https://img.shields.io/badge/SANITY%20Score-≥0.95-success)](docs/METHODOLOGY.md)
[![Security Level](https://img.shields.io/badge/Security-MAXIMUM-critical)](docs/SECURITY.md)
[![OWASP](https://img.shields.io/badge/OWASP%20Top%2010-Enforced-red)](docs/OWASP.md)
[![Anti-Hallucination](https://img.shields.io/badge/Hallucination-Zero%20Tolerance-orange)](docs/ANTI_PATTERNS.md)
[![Anti-Slop](https://img.shields.io/badge/AI%20Slop-Eliminated-blueviolet)](docs/QUALITY.md)

> *"The most dangerous AI response is not the wrong answer —*
> *it's the confidently delivered wrong answer with a SQL injection inside it."*

---

**[🇮🇩 Baca dalam Bahasa Indonesia](#-bahasa-indonesia) · [🇺🇸 Read in English](#-english)**

</div>

---

# 🇮🇩 BAHASA INDONESIA

## Apa itu SANITY?

**SANITY v3.0** adalah sebuah **Claude Code Skill** — protokol terstruktur tingkat militer yang di-inject ke dalam sesi Claude Code untuk:

1. **Mencegah, mendeteksi, dan memulihkan** dari **AI Hallucination** secara sistematis
2. **Memastikan setiap kode yang dihasilkan** bebas dari kerentanan keamanan yang bisa dieksploitasi

SANITY beroperasi pada **dua sumbu** yang keduanya wajib lolos — tidak ada pengecualian:

```
╔═══════════════════════════════════════════════════════════════╗
║  SUMBU 1: INTEGRITAS EPISTEMIK                                ║
║  "Jangan pernah klaim apa yang belum diverifikasi."           ║
║  → READ → EVIDENCE → ASSUME → LIMITS → ERROR-CHECK           ║
╠═══════════════════════════════════════════════════════════════╣
║  SUMBU 2: INTEGRITAS KEAMANAN          [PRIORITAS #1]         ║
║  "Jangan pernah hasilkan kode dengan celah keamanan."         ║
║  → THREAT-MODEL → AUDIT → OWASP → HARDEN → CERTIFY           ║
╚═══════════════════════════════════════════════════════════════╝
```

> **Mengapa Keamanan jadi Prioritas #1?**
> Fungsi yang dihalusinasi membuang waktu debugging.
> SQL injection di production menghancurkan data, reputasi, dan kepercayaan.
> Asimetri biaya ini menuntut keamanan diperlakukan sebagai kekhawatiran tertinggi.

---

## Jenis-Jenis Hallucination yang SANITY Eliminasi

| Tipe | Contoh | Dampak |
|------|--------|--------|
| 🔴 **Phantom Function** | Menyebut `flutter.setStyle()` yang tidak ada | Debugging berjam-jam |
| 🔴 **Ghost File** | Klaim isi file tanpa membacanya | Implementasi keliru |
| 🔴 **Version Fraud** | "React 22 mendukung..." (versi tidak ada) | Arsitektur salah |
| 🔴 **False Certainty** | "Pasti masalahnya di database" tanpa evidence | Waktu terbuang |
| 🔴 **Citation Fabrication** | Membuat referensi docs palsu | Trust collapse |
| 🔴 **Secret Exposure** | Hardcode API key di source code | Data breach |
| 🔴 **SQL Injection** | String concat user input ke query | Full DB compromise |
| 🔴 **Missing Auth** | Endpoint tanpa authentication check | Unauthorized access |
| 🔴 **XSS Generation** | `innerHTML = userInput` tanpa sanitasi | Account takeover |
| 🔴 **Path Traversal** | File path dari user input tanpa sanitasi | Arbitrary file read |

---

## FORTRESS Framework — 10 Pilar Kebenaran Terverifikasi & Aman

### SUMBU 1: INTEGRITAS EPISTEMIK (Pilar 1–5)

```
┌─────────────────────────────────────────────────────────────────────────┐
│ Pilar 1 — READ        Baca file sebelum klaim isinya                    │
│ Pilar 2 — EVIDENCE    Setiap klaim butuh sumber terverifikasi           │
│ Pilar 3 — ASSUME      Tandai semua asumsi secara eksplisit              │
│ Pilar 4 — LIMITS      Kenali dan nyatakan batas pengetahuan             │
│ Pilar 5 — ERROR-CHECK Verifikasi internal consistency sebelum deliver   │
└─────────────────────────────────────────────────────────────────────────┘
```

### SUMBU 2: INTEGRITAS KEAMANAN (Pilar 6–10) — PRIORITAS #1

```
┌─────────────────────────────────────────────────────────────────────────┐
│ Pilar 6  — THREAT-MODEL  Analisis ancaman sebelum tulis kode sensitif   │
│ Pilar 7  — AUDIT         Security audit checklist untuk setiap snippet  │
│ Pilar 8  — OWASP         Hard block jika ada pelanggaran OWASP Top 10   │
│ Pilar 9  — HARDEN        Hardening proaktif berlapis (defense in depth) │
│ Pilar 10 — CERTIFY       Security cert/caveat wajib sebelum deliver     │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## Confidence Matrix — Sistem Rating Dua Sumbu

**Integritas Epistemik:**
| Tag | Arti |
|-----|------|
| 🟢 `CONFIRMED` | Diverifikasi langsung — baca/jalankan/cari sendiri |
| 🟡 `INFERRED` | Kesimpulan logis dari bukti yang ada |
| 🔴 `UNCERTAIN` | Spekulasi / pengetahuan lama / belum diverifikasi |
| ⚫ `UNKNOWN` | Di luar batas pengetahuan — saya tidak tahu |

**Integritas Keamanan:**
| Tag | Arti |
|-----|------|
| 🛡️ `HARDENED` | Full security review — semua check passed |
| ⚡ `REVIEWED` | Standard checks passed, tidak ada critical issue |
| 🔸 `CAVEAT` | Passed dengan catatan — review sebelum production |
| 🚨 `BLOCKED` | Security issue ditemukan — JANGAN gunakan |

---

## Security Playbooks

### Input Validation
```
SEBELUM menulis kode yang menyentuh user input:
  ✅ Whitelist approach — define apa yang BOLEH, reject sisanya
  ✅ Validate: type + length + format + range
  ✅ Normalize unicode sebelum comparison
  ✅ Reject null bytes
  ✅ Limit request size
```

### Database Security
```
ATURAN ABSOLUT:
  ✅ SELALU gunakan parameterized query / prepared statement
  ❌ JANGAN PERNAH string-concat user input ke SQL
  ✅ Principle of least privilege untuk DB user
  ✅ Validate output encoding untuk display
```

### Secret Management
```
ATURAN ABSOLUT:
  ❌ JANGAN PERNAH hardcode secrets/API keys/passwords di source code
  ✅ SELALU gunakan environment variables atau secrets manager
  ✅ Jika terdeteksi: rotate segera + hapus dari git history
```

### OWASP Top 10 — Zero Tolerance
```
A01 Broken Access Control    → Server-side auth + deny by default
A02 Cryptographic Failures   → Env vars, bcrypt/Argon2, TLS 1.3
A03 Injection [MOST COMMON]  → Parameterized queries, allowlists
A04 Insecure Design          → Rate limiting, server-side validation
A05 Security Misconfiguration→ No debug in prod, security headers
A06 Vulnerable Components    → No known CVE packages, pin versions
A07 Auth Failures            → Session management, MFA, rate limit
A08 Data Integrity Failures  → SRI, no untrusted deserialization
A09 Logging Failures         → Log auth events, mask PII
A10 SSRF                     → Whitelist URLs, block private IPs
```

---

## Quick Install

### Cara 1: Via Claude Code CLI (Rekomendasi)
```bash
claude skill install https://github.com/verycoolapps/sanity-anti-hallucination-skill
```

### Cara 2: Manual
```bash
cp sanity.md ~/.claude/skills/sanity.md
```

### Cara 3: Invoke Langsung
```
/sanity
```

### Cara 4: Auto-Load via CLAUDE.md
```markdown
## Skills
- Always load: sanity

## AI Behavior
- All claims must be verified before delivery
- OWASP Top 10 compliance mandatory
- No hardcoded secrets ever
```

---

## SANITY Score — Sistem Penilaian Dua Sumbu

```
EPISTEMIK SCORE (E):
  Verified claims + Cited sources + Flagged assumptions + Stated limits
  Dikurangi self-contradictions
  Dibagi total claims

SECURITY SCORE (S):
  OWASP checks + Input validations + Auth checks + Injection secured + Certs
  NOTE: Jika ada hardcoded secret → S_SCORE = 0.00 (otomatis gagal)

COMBINED SANITY SCORE = (E × 0.4) + (S × 0.6)

🏆 ≥ 0.95 → SANITY MASTER     — Production-grade, world-class
✅ ≥ 0.85 → SANITY PASSED     — Aman untuk production
⚠️ ≥ 0.70 → SANITY WARNING    — Review sebelum deploy
❌ < 0.70 → SANITY FAILED     — Revisi penuh diperlukan
🚨 S=0.00 → SECURITY FAIL     — Block semua delivery
```

---

## Anti-Pattern Blacklist (Ringkasan)

### Epistemik Anti-Patterns:
```
❌ Phantom Function Syndrome  — Sebut API yang tidak ada
❌ Ghost File Hallucination   — Klaim isi file tanpa baca
❌ Version Confidence Fraud   — Sebut versi di luar data training
❌ False Certainty Masking    — "Pasti masalahnya X" tanpa evidence
❌ Confident Completion Fab.  — Kode "lengkap" untuk API yang tidak dikenal
❌ Recency Abuse              — "Baru-baru ini..." tanpa tahu kapan
❌ Self-Contradiction Blindness — Inkonsistensi dalam satu respons
```

### Security Anti-Patterns:
```
❌ SQL Injection Opening      — String concat ke SQL query
❌ Hardcoded Secrets          — Credentials di source code
❌ Missing Authentication     — Endpoint tanpa auth check
❌ Raw User Input in Shell    — exec(userInput) tanpa sanitasi
❌ Path Traversal             — File path dari user tanpa validasi
❌ Weak Password Hashing      — MD5/SHA1 untuk password
❌ XSS via innerHTML          — Unescaped user output di DOM
❌ IDOR Vulnerability         — Akses resource tanpa ownership check
❌ Missing Rate Limiting      — Login endpoint tanpa brute-force protection
❌ Info Disclosure via Errors — Stack trace / internals ke user
```

---

## SANITY Mantras

```
═══════════ EPISTEMIK ═══════════
"If I haven't read it, I don't know what's in it."
"Confidence without evidence is confabulation."
"When in doubt — READ, GREP, RUN. Then claim."

═══════════ KEAMANAN ═══════════
"No input is safe until validated. No exception."
"Secrets in code are secrets compromised."
"Security is not a feature. It is the foundation."
"Ship fast — but never ship exploitable."
```

---

<br/>

---

# 🇺🇸 ENGLISH

## What is SANITY?

**SANITY v3.0** is a **Claude Code Skill** — a military-grade, structured protocol injected into Claude Code sessions to:

1. **Prevent, detect, and recover** from **AI Hallucination** systematically and comprehensively
2. **Ensure every piece of generated code** is free from exploitable security vulnerabilities

SANITY operates on **two non-negotiable axes** — both must pass, no exceptions:

```
╔═══════════════════════════════════════════════════════════════╗
║  AXIS 1: EPISTEMIC INTEGRITY                                  ║
║  "Never claim what you haven't verified."                     ║
║  → READ → EVIDENCE → ASSUME → LIMITS → ERROR-CHECK           ║
╠═══════════════════════════════════════════════════════════════╣
║  AXIS 2: SECURITY INTEGRITY             [PRIORITY #1]         ║
║  "Never produce code with exploitable flaws."                 ║
║  → THREAT-MODEL → AUDIT → OWASP → HARDEN → CERTIFY           ║
╚═══════════════════════════════════════════════════════════════╝
```

> **Why is Security Priority #1?**
> A hallucinated function wastes debugging time.
> A SQL injection vulnerability in production destroys data, reputation, and trust.
> This cost asymmetry demands security be treated as the supreme concern.

---

## Types of Hallucination SANITY Eliminates

| Type | Example | Impact |
|------|---------|--------|
| 🔴 **Phantom Function** | Citing `flutter.setStyle()` that doesn't exist | Hours of debugging |
| 🔴 **Ghost File** | Claiming file contents without reading it | Wrong implementation |
| 🔴 **Version Fraud** | "React 22 supports..." (version doesn't exist) | Wrong architecture |
| 🔴 **False Certainty** | "It's definitely the database" with no evidence | Wasted time |
| 🔴 **Citation Fabrication** | Inventing fake documentation references | Trust collapse |
| 🔴 **Secret Exposure** | Hardcoding API keys in source code | Data breach |
| 🔴 **SQL Injection** | String-concatenating user input into queries | Full DB compromise |
| 🔴 **Missing Auth** | Endpoints without authentication checks | Unauthorized access |
| 🔴 **XSS Generation** | `innerHTML = userInput` without sanitization | Account takeover |
| 🔴 **Path Traversal** | User-supplied file paths without validation | Arbitrary file read |

---

## The FORTRESS Framework — 10 Pillars of Verified, Secure Truth

### AXIS 1: EPISTEMIC INTEGRITY (Pillars 1–5)

```
┌─────────────────────────────────────────────────────────────────────────┐
│ Pillar 1 — READ        Read files before claiming their contents        │
│ Pillar 2 — EVIDENCE    Every claim must have a verifiable source        │
│ Pillar 3 — ASSUME      Explicitly label all assumptions                 │
│ Pillar 4 — LIMITS      Recognize and state knowledge boundaries         │
│ Pillar 5 — ERROR-CHECK Verify internal consistency before delivery      │
└─────────────────────────────────────────────────────────────────────────┘
```

### AXIS 2: SECURITY INTEGRITY (Pillars 6–10) — PRIORITY #1

```
┌─────────────────────────────────────────────────────────────────────────┐
│ Pillar 6  — THREAT-MODEL  Threat analysis before any sensitive code     │
│ Pillar 7  — AUDIT         Full security audit checklist every snippet   │
│ Pillar 8  — OWASP         Hard block on any OWASP Top 10 violation      │
│ Pillar 9  — HARDEN        Proactive layered hardening (defense in depth)│
│ Pillar 10 — CERTIFY       Security cert/caveat required before delivery │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## Confidence Matrix — Dual-Axis Rating System

**Epistemic Confidence:**
| Tag | Meaning |
|-----|---------|
| 🟢 `CONFIRMED` | Directly verified — read/run/searched myself |
| 🟡 `INFERRED` | Logical conclusion from available evidence |
| 🔴 `UNCERTAIN` | Speculation / stale knowledge / unverified |
| ⚫ `UNKNOWN` | Beyond knowledge limits — I don't know |

**Security Confidence:**
| Tag | Meaning |
|-----|---------|
| 🛡️ `HARDENED` | Full security review — all checks passed |
| ⚡ `REVIEWED` | Standard checks passed, no critical issues |
| 🔸 `CAVEAT` | Passed with notes — review before production |
| 🚨 `BLOCKED` | Security issue found — DO NOT USE |

---

## Security Playbooks

### Input Validation
```
BEFORE writing any code that touches user input:
  ✅ Whitelist approach — define what IS allowed, reject everything else
  ✅ Validate: type + length + format + range
  ✅ Normalize unicode before comparison
  ✅ Reject null bytes
  ✅ Limit request size
```

### Database Security
```
ABSOLUTE RULES:
  ✅ ALWAYS use parameterized queries / prepared statements
  ❌ NEVER string-concatenate user input into SQL
  ✅ Principle of least privilege for DB user
  ✅ Validate output encoding for display
```

### Secret Management
```
ABSOLUTE RULES:
  ❌ NEVER hardcode secrets/API keys/passwords in source code
  ✅ ALWAYS use environment variables or a secrets manager
  ✅ If detected: rotate immediately + purge from git history
```

### Security Certification Format
```
🔐 SECURITY CERTIFICATION
━━━━━━━━━━━━━━━━━━━━━━━━━━
Injection risk     : MITIGATED — parameterized queries used
Auth check         : PRESENT — middleware enforced
Input validation   : PRESENT — type + length + format validated
Secret exposure    : NONE — credentials via env vars
OWASP A01–A10      : REVIEWED — no violations detected
Hardening applied  : YES — rate limiting, CSRF, HttpOnly cookies
━━━━━━━━━━━━━━━━━━━━━━━━━━
VERDICT: SAFE TO REVIEW — independent security audit still recommended
```

---

## Quick Install

### Method 1: Via Claude Code CLI (Recommended)
```bash
claude skill install https://github.com/verycoolapps/sanity-anti-hallucination-skill
```

### Method 2: Manual Install
```bash
cp sanity.md ~/.claude/skills/sanity.md
```

### Method 3: Direct Invocation
```
/sanity
```

### Method 4: Auto-Load via CLAUDE.md
```markdown
## Skills
- Always load: sanity

## AI Behavior
- All claims must be verified before delivery
- OWASP Top 10 compliance is mandatory
- No hardcoded secrets, ever
```

---

## SANITY Score System

```
EPISTEMIC SCORE (E):
  Verified claims + Cited sources + Flagged assumptions + Stated limits
  Minus self-contradictions
  Divided by total claims

SECURITY SCORE (S):
  OWASP checks + Input validations + Auth checks + Secured injections + Certs
  NOTE: Any hardcoded secret → S_SCORE = 0.00 (automatic fail)

COMBINED SANITY SCORE = (E × 0.4) + (S × 0.6)

🏆 ≥ 0.95 → SANITY MASTER     — Production-grade, world-class output
✅ ≥ 0.85 → SANITY PASSED     — Solid, safe for most production contexts
⚠️ ≥ 0.70 → SANITY WARNING    — Unresolved concerns — review before deploy
❌ < 0.70 → SANITY FAILED     — NOT production-ready — full revision required
🚨 S=0.00 → SECURITY FAIL     — Block all delivery until security is fixed
```

---

## OWASP Top 10 Hard Block — Zero Tolerance List

```
A01 Broken Access Control    → Server-side auth + deny-by-default
A02 Cryptographic Failures   → Env vars, bcrypt/Argon2, TLS 1.3
A03 Injection [MOST COMMON]  → Parameterized queries, input allowlists
A04 Insecure Design          → Rate limiting, server-side business logic
A05 Security Misconfiguration→ No debug in prod, security headers set
A06 Vulnerable Components    → No known-CVE packages, pin exact versions
A07 Auth Failures            → Session management, MFA, account lockout
A08 Data Integrity Failures  → SRI, no untrusted deserialization
A09 Logging Failures         → Log auth events, mask PII in logs
A10 SSRF                     → Whitelist URLs, block private IP ranges
```

---

## Anti-Pattern Blacklist (Summary)

### Epistemic Anti-Patterns:
```
❌ Phantom Function Syndrome   — Citing APIs that don't exist
❌ Ghost File Hallucination    — Claiming file contents without reading
❌ Version Confidence Fraud    — Citing versions beyond training data
❌ False Certainty Masking     — "It's definitely X" with no evidence
❌ Confident Completion Fab.   — "Complete" code for unknown APIs
❌ Recency Abuse               — "Recently added..." without knowing when
❌ Self-Contradiction Blindness — Inconsistencies within one response
```

### Security Anti-Patterns:
```
❌ SQL Injection Opening       — String concat into SQL queries
❌ Hardcoded Secrets           — Credentials in source code
❌ Missing Authentication      — Endpoints without auth checks
❌ Raw User Input in Shell     — exec(userInput) without sanitization
❌ Path Traversal              — User-supplied paths without validation
❌ Weak Password Hashing       — MD5/SHA1 for passwords
❌ XSS via innerHTML           — Unescaped user output in the DOM
❌ IDOR Vulnerability          — Resource access without ownership check
❌ Missing Rate Limiting       — Login endpoints without brute-force protection
❌ Info Disclosure via Errors  — Stack traces/internals exposed to users
```

---

## Recovery Protocol

### Epistemic Recovery:
```
STEP 1 — ACKNOWLEDGE  "⚠️ CORRECTION: I incorrectly stated [X]."
STEP 2 — EXPLAIN      "I claimed this without proper verification."
STEP 3 — VERIFY & FIX [Perform actual verification → provide correction]
STEP 4 — PREVENT      "I will [X] before making similar claims."
```

### Security Recovery:
```
STEP 1 — ALERT        "🚨 SECURITY ISSUE DETECTED: [category] at [location]"
STEP 2 — ASSESS       "Severity: [CRITICAL/HIGH/MEDIUM/LOW] — [impact description]"
STEP 3 — BLOCK        "This code MUST NOT be used until this is fixed."
STEP 4 — FIX          [Rewrite with proper secure implementation]
STEP 5 — AUDIT        "I'm also checking [related areas] for similar issues."
```

---

## Repository Structure

```
sanity-anti-hallucination-skill/
│
├── sanity.md                         ← 🌟 MAIN SKILL FILE (install this)
│
├── docs/
│   ├── METHODOLOGY.md                ← FORTRESS Framework deep-dive
│   ├── SECURITY.md                   ← Security pillars & playbooks detail
│   ├── OWASP.md                      ← OWASP Top 10 enforcement guide
│   ├── EXAMPLES.md                   ← Before/after examples
│   ├── ANTI_PATTERNS.md              ← Full anti-patterns with examples
│   └── CONFIDENCE_MATRIX.md          ← Dual-axis rating system detail
│
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   ├── hallucination_report.md   ← Report hallucinations that slipped through
│   │   └── security_report.md        ← Report security false negatives
│   └── workflows/
│       └── skill-validation.yml
│
├── README.md                         ← This file (bilingual: ID + EN)
├── LICENSE                           ← MIT License
├── CONTRIBUTING.md                   ← Contribution guide
└── CHANGELOG.md                      ← Version history
```

---

## Contributing

We welcome contributions for:
- 🐛 **Bug Reports** — Hallucinations or security issues that slipped through SANITY
- 🔐 **New Security Patterns** — Additional security anti-patterns or playbooks
- 💡 **New Anti-Patterns** — New hallucination patterns discovered in the wild
- 📖 **Documentation** — Improve clarity, add examples, better explanations
- 🌐 **Translations** — Port to other languages
- ⚗️ **New Playbooks** — Verification playbooks for new domains (mobile, embedded, ML, etc.)

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

---

## License

MIT License — Free to use, modify, and distribute.
See [LICENSE](LICENSE) for full details.

---

## SANITY Mantras

```
═══════════ EPISTEMIC LAWS ═══════════
"If I haven't read it, I don't know what's in it."
"If I haven't run it, I don't know if it works."
"Confidence without evidence is confabulation."
"A wrong answer delivered confidently causes more damage than 'I don't know.'"
"When in doubt — READ, GREP, RUN. Then claim."

═══════════ SECURITY LAWS ═══════════
"No input is safe until validated. No exception."
"Secrets in code are secrets compromised."
"Every endpoint without auth is an open door."
"Defense in depth: never rely on a single security layer."
"Security is not a feature. It is the foundation."
"Ship fast — but never ship exploitable."
```

---

<div align="center">

**SANITY v3.0.0**

Epistemic Integrity × Security Supremacy

*"Truth over confidence. Security over convenience. Evidence over assumption."*
*Zero tolerance for confabulation. Zero tolerance for exploitable code.*

[![Star this repo](https://img.shields.io/github/stars/verycoolapps/sanity-anti-hallucination-skill?style=social)](https://github.com/verycoolapps/sanity-anti-hallucination-skill)

</div>
