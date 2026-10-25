# 🦉 OEntropy

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCipher-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.1-cyan?style=flat-square"/>
</p>

> **OEntropy** — Entropy & Randomness Analyzer ║

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OEntropy measures randomness quality of files, text, byte streams, and cryptographic key material. It helps analysts spot compressed/encrypted regions, weak keys, and low-entropy secrets during forensics or crypto review. Headless file/text modes and optional GUI cover both automation and interactive inspection.

---

## ✨ Features

- Entropy analysis for files and UTF-8 text strings
- Headless --file / --text modes for pipelines
- JSON report emission for machine-readable results
- Optional GUI for interactive randomness inspection
- Useful for spotting encrypted/compressed blobs in artefacts
- Supports defensive crypto and forensics triage

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OEntropy --file sample.bin --json
./OEntropy --text 'password123'
./OEntropy --gui
./OEntropy --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
