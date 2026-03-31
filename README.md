# 🦉 OEntropy

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux%20%2F%20Windows-informational?style=flat-square&logo=linux&logoColor=white&color=0a0c10"/>
  <img src="https://img.shields.io/badge/Category-OCipher%20%2F%20Cryptography-cyan?style=flat-square"/>
  <img src="https://img.shields.io/badge/Interface-GUI%20%28Tkinter%29-blueviolet?style=flat-square"/>
  <img src="https://img.shields.io/badge/No%20Dependencies-Stdlib%20Only-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OEntropy** is a dark-themed GUI entropy and randomness analyser — measure Shannon entropy, run chi-square and Monte Carlo tests, visualise byte frequency distribution, entropy sliding-window timeline, bigram heatmap, and grade cryptographic key quality from A+ to F.

---

## 📌 Overview

OEntropy accepts files, hex keys, pasted text, or synthetic data and applies four statistical randomness tests simultaneously. Results are displayed across five visual tabs and graded on an entropy scale — making it easy to assess whether data is encrypted, compressed, structured, or weak.

---

## 🖥️ Interface Tabs

| Tab | Contents |
|-----|---------|
| **OVERVIEW** | Full text report: source, size, all four test results, grade, classification |
| **BYTE DISTRIBUTION** | 256-bar frequency canvas (bar chart or heat row mode) for all 0x00–0xFF byte values |
| **ENTROPY TIMELINE** | Sliding-window entropy line chart across the full data — colour-coded (green > 7.5, cyan > 6, yellow > 4, red ≤ 4) with mean line |
| **BIGRAM HEATMAP** | 16×16 high-nibble pair heatmap — uniform grid = random, diagonal bias = structured |
| **HISTORY** | Treeview of all session analyses — timestamp, source, size, entropy, grade, chi verdict, classification |

---

## 📊 Statistical Tests

| Test | What It Measures |
|------|-----------------|
| **Shannon Entropy** | Information density in bits/byte — max 8.0 for perfectly random data |
| **Chi-Square** | Uniformity of byte distribution across all 256 values — deviations flag structured patterns |
| **Monte Carlo π** | Estimates π from byte pairs as 2D coordinates — error % indicates how random the data is |
| **Serial Correlation** | Measures linear dependency between adjacent bytes — near 0 means no sequential patterns |

---

## 🏆 Grade Scale

Grades are assigned by Shannon entropy (bits/byte):

| Grade | Threshold | Description |
|-------|-----------|-------------|
| **A+** | ≥ 7.90 | Excellent — cryptographically strong randomness |
| **A** | ≥ 7.50 | Very Good — high entropy, likely encrypted/compressed |
| **B** | ≥ 7.00 | Good — above average entropy |
| **C** | ≥ 6.00 | Fair — moderate entropy, structured data |
| **D** | ≥ 4.00 | Low — low entropy, repetitive patterns detected |
| **F** | ≥ 0.00 | Very Low — near-zero entropy, highly predictable |

---

## 🔍 File Classification

OEntropy automatically classifies data based on entropy and test results:

| Entropy Range | Classification |
|---------------|---------------|
| > 7.9 | Encrypted / Compressed — very high entropy |
| > 7.0 | Likely compressed or high-entropy binary |
| > 5.0 | Binary executable or structured binary data |
| > 3.5 | Text / source code / structured data |
| > 1.5 | Repeated patterns — low-entropy text |
| ≤ 1.5 | Highly repetitive or sparse data |

---

## 🎛️ Sidebar Controls

| Section | Controls |
|---------|---------|
| **INPUT SOURCE** | Analyse File (binary) · Analyse Key/Hex · Generate Random · Paste Text/Hex |
| **RANDOM GENERATOR** | Size (64–1,048,576 bytes) · Source: `os.urandom` / `hashlib chain` / `XOR pattern` / `Zero bytes` / `Alternating 0xAA` / `Repeating text` |
| **ANALYSIS OPTIONS** | Window size (64–4,096 bytes) for timeline · Block size (512–65,536 bytes) for file scan |
| **LIVE METRICS** | Shannon Entropy · Grade · Chi-Square · Monte Carlo π · Serial Corr. · Data Size — plus entropy progress bar |
| **EXPORT** | Export Report JSON · Export Report TXT · Clear History |

---

## 🎲 Random Generator Sources

The built-in generator produces synthetic data for benchmarking the analysis engine:

| Source | Expected Result |
|--------|----------------|
| `os.urandom` | A+ grade — true OS randomness |
| `hashlib chain` | A grade — hash-derived pseudorandomness |
| `XOR pattern` | B–C grade — patterned but varied |
| `Zero bytes` | F grade — all 0x00 |
| `Alternating 0xAA` | D–F grade — two-value alternation |
| `Repeating text` | F grade — near-zero entropy text |

---

## 📤 Export

Session history exported via native file-save dialog:

| Format | Contents |
|--------|----------|
| **JSON** | Tool metadata + all session records: source, size, entropy, grade, chi-square, Monte Carlo π, serial correlation, classification |
| **TXT** | Human-readable report of the last analysis |

---

## ⚙️ Requirements

- **Linux or Windows** with a display
- **No Python installation needed** — runs as a standalone executable
- **No external dependencies** — Tkinter and stdlib only

---

## 🚀 Usage

```bash
./OEntropy
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
