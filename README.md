## [[简体中文]](README-CN.md)

# Alice’s Adventures in Wonderland — LaTeX Edition

## Overview

This repository contains the complete LaTeX source code for a refined typesetting of Lewis Carroll’s Alice’s Adventures in Wonderland. The entire book is set in **EB Garamond**, a graceful revival of the historic Garamond typeface. **It is a text‑only edition with no illustrations.**

The design focuses on a clean book layout, offering both a pleasant on‑screen reading experience and a high‑quality printed output.

## How to Build

**Prerequisites:**

- A modern TeX distribution (e.g. TeX Live 2024+, MiKTeX)

- The `ebgaramond` package (typically part of texlive-fonts-extra in TeX Live)

- **Compilation must be done with LuaLaTeX (required for fontspec and proper font handling)**

**Build instructions:**

1. Clone the repository

```bash
git clone https://github.com/your-username/alice-latex.git
cd alice-latex
```

2. Compile with LuaLaTeX

```bash
lualatex alice.tex
```

Important: To generate the table of contents and all cross‑references correctly, you must compile at least twice. For example:

```bash
lualatex alice.tex
lualatex alice.tex
```

Or use latexmk for automatic cycles:

```bash
latexmk -lualatex alice.tex
```

The final PDF is `alice_in_wonderland.pdf`.

A `Makefile` is also provided for convenience; simply run `make`.

## Repository Structure

```text
.
├── alice_in_wonderland.aux
├── alice_in_wonderland.log
├── alice_in_wonderland.pdf                # Main document
├── alice_in_wonderland.synctex.gz
├── alice_in_wonderland.tex                # Final PDF
├── alice_in_wonderland.toc
├── LICENSE                                # CC BY‑SA 4.0
├── README-CN.md
└── README.md
```

No image files are included – the project is entirely text‑based LaTeX code.

## License

- Original English text: Public domain (Lewis Carroll, 1865)

- LaTeX typesetting code (.tex files, style definitions, etc.):
[Creative Commons Attribution‑ShareAlike 4.0 International (CC BY‑SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/legalcode.en)

- [EB Garamond](https://github.com/georgd/EB-Garamond) font: [SIL Open Font License 1.1](https://openfontlicense.org/open-font-license-official-text/)

- You may freely share and adapt the typesetting code provided that appropriate credit is given and any derivative work is distributed under the same license.

## Credits

- Original story: Lewis Carroll

- Typesetting & LaTeX implementation: klkjkj-a

- Typeface: EB Garamond by Georg Mayr-Duffner & Octavio Pardo

---

> “We’re all mad here.” — Cheshire Cat
