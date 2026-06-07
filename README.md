# 🎣 Phishing & URL Threat Analyzer

> Paste a URL or a raw email header — get the indicators a SOC analyst checks, with each one explained.

![Type](https://img.shields.io/badge/type-threat_detection-3fe08f)
![Stack](https://img.shields.io/badge/built_with-vanilla_JS-46d3ff)
![Privacy](https://img.shields.io/badge/privacy-100%25_client--side-7c8bff)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

A single-file, client-side tool that triages **URLs** and **email headers** for phishing indicators and returns a risk score with analyst-grade explanations.

**🔗 Live demo:** `https://staticish.github.io/phishing-url-analyzer/` *(enable GitHub Pages, see below)*

---

## ✨ Features

**URL analysis**
- IP-address hosts, the `@`-in-URL redirect trick, punycode/homoglyph domains (`xn--`)
- Typosquats via **Levenshtein distance** to known brands, brand-in-subdomain lures
- Risky/abused TLDs, URL shorteners, non-standard ports, over-long URLs, credential keywords
- HTTP-vs-HTTPS, and a clear note that *HTTPS ≠ trustworthy*

**Email header analysis**
- Parses `From`, `Reply-To`, `Return-Path`, `Authentication-Results`
- Explains **SPF / DKIM / DMARC** pass/fail and what each actually proves
- Detects **display-name spoofing**, reply-to / return-path mismatches, urgency language

Includes built-in **legit vs phishing samples** to learn from, and a 0–100 risk gauge.

## 🧠 How it works

Each heuristic adds to a weighted risk score and emits a human-readable finding (`bad`/`warn`/`good`/`info`). The same logic a mail gateway or SOAR playbook applies — distilled so you can see *why* a message is flagged, not just *that* it is. The "registrable domain" extraction teaches the single most important phishing skill: read the domain right-to-left from the TLD.

## 🎓 What it demonstrates

**Cyber threat intelligence**, phishing triage, email authentication (SPF/DKIM/DMARC), and turning detection logic into clear stakeholder-ready explanations — core SOC analyst work.

## ▶️ Run locally
Open `index.html` in any browser. No build, no dependencies, fully offline.

## 🚀 Live demo (GitHub Pages)
**Settings → Pages → Source: `main` / root → Save.**

## 📜 License
MIT © 2026 Ismail Olanrewaju
