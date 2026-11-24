# Third-Party Notices — OEntropy

This tool is distributed as a single pre-built executable. It bundles the
third-party components listed below. Each component remains the property of
its respective copyright holders and is used under its own license, whose
full text is reproduced in this file.

**Owlsec LLC's own source code is proprietary and is not covered by any of
the licenses below.** Those licenses apply only to the third-party components
named here.

- Tool binary: `OEntropy`
- SHA-256: `62c0e30225faabc065286a22fd5880d2a20b744e0a2ac83772d97cf2640f5fd9`
- Bundled interpreter: CPython 3.11 (PSF License)
- Generated: 2026-11-24
- Machine-readable inventory: see `SBOM.cdx.json` in this repository

## Components

| Component | Version | License |
|---|---|---|
| setuptools | 66.1.1 | MIT License |
| CPython | 3.11 | PSF-2.0 |
| Python standard library | 3.11 | PSF-2.0 |

Shared system libraries from Debian (for example `libssl`, `libz`, `libbz2`) are bundled unmodified by PyInstaller and are governed by their own licenses as shipped by the Debian project. The exact versions are listed in `SBOM.cdx.json`.

---

## Full license texts

### setuptools 66.1.1

- Author: Python Packaging Authority
- Project: https://github.com/pypa/setuptools
- Declared license: MIT License

<details>
<summary><code>LICENSE</code></summary>

```text
Copyright Jason R. Coombs

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to
deal in the Software without restriction, including without limitation the
rights to use, copy, modify, merge, publish, distribute, sublicense, and/or
sell copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS
IN THE SOFTWARE.
```

</details>

---

## Python Software Foundation License

The bundled CPython interpreter and standard library are distributed under the PSF License Agreement: <https://docs.python.org/3/license.html>
