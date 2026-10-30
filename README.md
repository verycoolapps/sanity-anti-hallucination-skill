# ⚡ SANITY — Anti-Hallucination Supremacy Protocol

<div align="center">

```
╔═══════════════════════════════════════════════════════════════╗
║                                                               ║
║   ███████╗ █████╗ ███╗   ██╗██╗████████╗██╗   ██╗           ║
║   ██╔════╝██╔══██╗████╗  ██║██║╚══██╔══╝╚██╗ ██╔╝           ║
║   ███████╗███████║██╔██╗ ██║██║   ██║    ╚████╔╝            ║
║   ╚════██║██╔══██║██║╚██╗██║██║   ██║     ╚██╔╝             ║
║   ███████║██║  ██║██║ ╚████║██║   ██║      ██║              ║
║   ╚══════╝╚═╝  ╚═╝╚═╝  ╚═══╝╚═╝   ╚═╝      ╚═╝              ║
║                                                               ║
║         Anti-Hallucination Supremacy Protocol                 ║
║                    for Claude Code                            ║
║                                                               ║
╚═══════════════════════════════════════════════════════════════╝
```

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![Version](https://img.shields.io/badge/version-2.0.0-brightgreen)](CHANGELOG.md)
[![SANITY Score](https://img.shields.io/badge/SANITY%20Score-≥0.90-success)](docs/METHODOLOGY.md)
[![Anti-Hallucination](https://img.shields.io/badge/Hallucination-Zero%20Tolerance-red)](docs/ANTI_PATTERNS.md)

> *"The most dangerous AI response is not the wrong answer —*  
> *it's the confidently delivered wrong answer."*

</div>

---

## 🧠 Apa Itu SANITY?

**SANITY** adalah sebuah **Claude Code Skill** — sebuah protokol terstruktur yang di-inject ke dalam sesi Claude Code untuk mencegah, mendeteksi, dan memulihkan dari **AI Hallucination** secara sistematis dan menyeluruh.

Hallucination dalam AI bukan sekadar "salah jawab." Ini mencakup:

| Tipe Hallucination | Contoh | Dampak |
|---|---|---|
| 🔴 **Phantom Function** | Menyebut `flutter.setStyle()` yang tidak ada | Debugging berjam-jam |
| 🔴 **Ghost File** | Mengklaim `lib/config/auth.dart` berisi X tanpa membacanya | Implementasi salah |
| 🔴 **Version Fraud** | "React 22 mendukung..." (versi tidak ada) | Keputusan arsitektur keliru |
| 🔴 **False Certainty** | "Pasti masalahnya di database" (tanpa evidence) | Waktu debugging terbuang |
| 🔴 **Citation Fabrication** | Membuat referensi docs yang tidak ada | Trust collapse |
| 🔴 **Confident Completion** | Mengisi kode "lengkap" untuk API yang tidak dikenal | Silent bugs di production |

**SANITY** memotong semua ini di akarnya dengan 5 pilar verifikasi, confidence matrix, dan playbook kategori spesifik.

---

## 🚀 Quick Install

### Cara 1: Install ke Claude Code (Rekomendasi)

```bash
# Install SANITY skill ke Claude Code
claude skill install https://github.com/verycoolapps/sanity-anti-hallucination-skill

# Atau manual — copy sanity.md ke direktori skills kamu:
cp sanity.md ~/.claude/skills/sanity.md
```

### Cara 2: Invoke Langsung di Sesi

```
/sanity
```

Ketik `/sanity` di prompt Claude Code untuk mengaktifkan protokol di sesi aktif.

### Cara 3: Auto-Load via CLAUDE.md

Tambahkan ke `CLAUDE.md` projekmu agar SANITY aktif di setiap sesi:

```markdown
## Skills
- Always load: sanity (Anti-Hallucination Protocol)

## AI Behavior
- All claims must be verified before delivery
- Use REALE Framework for every factual assertion
- Confidence labels are mandatory on unconfirmed claims
```

---

## ⚡ Core Architecture

### The REALE Framework

```
┌─────────────────────────────────────────────────────────────────┐
│                     REALE FRAMEWORK                             │
│                                                                 │
│   R ─── READ        Baca file sebelum klaim isinya             │
│   E ─── EVIDENCE    Setiap klaim butuh sumber terverifikasi    │
│   A ─── ASSUME      Tandai semua asumsi secara eksplisit       │
│   L ─── LIMITS      Kenali dan nyatakan batas pengetahuan      │
│   E ─── ERROR-CHECK Verifikasi internal consistency            │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Confidence Matrix

```
🟢 CONFIRMED   ── Diverifikasi langsung (Read/Run/Grep)
🟡 INFERRED    ── Kesimpulan logis dari bukti yang ada
🔴 UNCERTAIN   ── Spekulasi / pengetahuan lama / belum diverifikasi  
⚫ UNKNOWN     ── Di luar batas pengetahuan — saya tidak tahu
```

### Verification Playbooks

| Kategori | Trigger | Protokol |
|---|---|---|
| 📁 **File Content** | "berisi...", "ada di..." | Read → Quote dengan baris |
| ⚙️ **Function Exist** | "ada function...", "gunakan..." | Grep → Konfirmasi path:baris |
| 📦 **Package/Version** | "ter-install...", "versi..." | Read lock/manifest file |
| 🌐 **External API** | "API ini melakukan...", "endpoint..." | Read docs/source |
| 🧮 **Math/Logic** | kalkulasi, inferensi | Step-by-step dengan checks |
| 📚 **Training Facts** | fakta tentang library/framework | Label cutoff + recommend docs |

---

## 🎯 Mengapa SANITY Berbeda?

### vs. Prompt Biasa
```
❌ "Jangan hallucinate" — terlalu abstrak, tidak ada enforcement mechanism
✅ SANITY — protokol konkret dengan verification steps, confidence labels, recovery protocol
```

### vs. System Prompts Generic
```
❌ "Always be accurate and cite sources" — tidak spesifik, mudah dilupakan
✅ SANITY — 5 pilar, 4 confidence tiers, 7 playbooks, blacklist, recovery steps
```

### vs. Manual Review
```
❌ Mengandalkan user untuk mendeteksi hallucination — butuh expertise
✅ SANITY — AI self-verifies sebelum deliver, koreksi segera saat error dideteksi
```

---

## 📊 The 10 Anti-Patterns SANITY Eliminates

```
1. 👻 Phantom Function Syndrome      — Menyebut API/function yang tidak ada
2. 💀 Ghost File Hallucination       — Mengklaim isi file tanpa membacanya
3. 🕰️ Version Confidence Fraud       — Menyebut versi di luar knowledge window
4. 🎭 False Certainty Masking        — "Pasti masalahnya X" tanpa evidence
5. ✍️ Confident Completion Fab.      — Menulis "implementasi lengkap" API yang tidak dikenal
6. 📰 Recency Abuse                  — "Baru-baru ini..." tanpa tahu kapan "baru"
7. 📚 SO Paraphrase Bug             — Solusi lama yang API-nya sudah berubah
8. 🔗 Citation Fabrication          — Membuat referensi/link/docs yang tidak ada
9. 🧮 Math Confidence Skip          — Memberikan hasil kalkulasi tanpa show work
10. 🔄 Self-Contradiction Blindness  — Menyebut hal berbeda di bagian berbeda respons
```

---

## 📈 SANITY Score System

Evaluasi kualitas setiap respons dengan metric SANITY:

```
SANITY SCORE = (Verified + Cited + Flagged + Limits_Stated - Contradictions) / Total_Claims

🏆 ≥ 0.90  SANITY MASTER    — Standar produksi tertinggi
✅ ≥ 0.75  SANITY PASSED    — Acceptable untuk sebagian besar konteks
⚠️ ≥ 0.60  SANITY WARNING   — Terlalu banyak klaim tidak terverifikasi
❌ < 0.60  SANITY FAILED    — Respons tidak layak deliver, perlu full revision
```

---

## 🔄 Recovery Protocol

Ketika AI menyadari telah hallucinate, SANITY mengaktifkan 4-step recovery:

```
STEP 1 — ACKNOWLEDGE     "⚠️ KOREKSI: Saya tadi salah menyatakan [X]."
STEP 2 — EXPLAIN ERROR   "Saya mengklaim ini tanpa verifikasi yang proper."
STEP 3 — VERIFY & FIX    [Lakukan verifikasi yang benar → berikan koreksi]
STEP 4 — PREVENT RECUR   "Saya akan [X] sebelum klaim serupa di depan."
```

---

## 🗣️ Uncertainty Vocabulary

SANITY mengajarkan AI menggunakan vocabulary yang tepat untuk setiap tingkat kepercayaan:

| Confidence | Vocabulary yang Tepat |
|---|---|
| 🟢 High | "Berdasarkan `file:baris` yang baru saya baca..." |
| 🟡 Medium | "Kemungkinan besar...", "Pattern ini mengindikasikan..." |
| 🔴 Low | "Per data training saya...", "Saya tidak yakin 100%..." |
| ⚫ None | "Ini di luar batas pengetahuan saya.", "Saya butuh lihat X dulu." |

---

## 📁 Repository Structure

```
sanity-anti-hallucination-skill/
│
├── sanity.md                    ← 🌟 SKILL FILE UTAMA (install ini)
│
├── docs/
│   ├── METHODOLOGY.md           ← Deep-dive REALE Framework
│   ├── EXAMPLES.md              ← Before/after hallucination examples
│   ├── ANTI_PATTERNS.md         ← 10 anti-patterns dengan contoh nyata
│   └── CONFIDENCE_MATRIX.md     ← Confidence rating system detail
│
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   └── hallucination_report.md  ← Report hallucination yang lolos
│   └── workflows/
│       └── skill-validation.yml
│
├── README.md                    ← File ini
├── LICENSE                      ← MIT License
├── CONTRIBUTING.md              ← Cara berkontribusi
└── CHANGELOG.md                 ← Version history
```

---

## 🤝 Contributing

Kami menerima kontribusi untuk:
- 🐛 **Bug Reports** — Hallucination yang lolos dari SANITY Protocol
- 💡 **New Anti-Patterns** — Pattern hallucination baru yang ditemukan
- 📖 **Documentation** — Improve clarity, add examples
- 🌐 **Translations** — Port ke bahasa lain
- ⚗️ **New Playbooks** — Verification playbook untuk kategori baru

Lihat [CONTRIBUTING.md](CONTRIBUTING.md) untuk detail.

---

## 📜 License

MIT License — Bebas digunakan, dimodifikasi, dan didistribusikan.  
Lihat [LICENSE](LICENSE) untuk detail lengkap.

---

## 🌟 SANITY Mantras

```
"If I haven't read it, I don't know what's in it."
"If I haven't run it, I don't know if it works."
"If I haven't searched for it, I don't know if it exists."
"Confidence without evidence is confabulation."
"A wrong answer delivered confidently causes more damage than 'I don't know.'"
"My training cutoff is real. Time passes. Libraries change. Check the source."
"Every phantom function I invent wastes the user's debugging time."
"Uncertainty, stated clearly, is more valuable than false certainty."
"When in doubt — READ, GREP, RUN. Then claim."
```

---

<div align="center">

**SANITY v2.0.0**  
Built for zero tolerance of confabulation.

*"Truth over confidence. Evidence over assumption. Clarity over fluency."*

[![Star this repo](https://img.shields.io/github/stars/verycoolapps/sanity-anti-hallucination-skill?style=social)](https://github.com/verycoolapps/sanity-anti-hallucination-skill)

</div>
